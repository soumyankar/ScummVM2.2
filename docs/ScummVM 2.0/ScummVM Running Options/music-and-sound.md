---
layout: default
parent: Advanced Configuration
grand_parent: ScummVM Configuration
title: Music & Sound
nav_order: 1
---

# Music and Sound

ScummVM has an extensive amount of options for Music and Sound.  

On most operating systems and for most games, ScummVM will by default use MT-32 or AdLib emulation for music playback. MIDI may not be available on all operating systems or may need manual configuration. If you want to use MIDI, you have several different choices of output, depending on your operating system and configuration.

```
null       - Null output. Don't play any music.

adlib      - Internal AdLib emulation
fluidsynth - FluidSynth MIDI emulation
mt32       - Internal MT-32 emulation
pcjr       - Internal PCjr emulation (only usable in SCUMM games)
pcspk      - Internal PC Speaker emulation
towns      - Internal FM-TOWNS YM2612 emulation
             (only usable in SCUMM FM-TOWNS games)

alsa       - Output using ALSA sequencer device. See below.
core       - CoreAudio sound, for Mac OS X users.
coremidi   - CoreMIDI sound, for Mac OS X users. Use only if you have
             a hardware MIDI synthesizer.
seq        - Use /dev/sequencer for MIDI, *nix users. See below.
timidity   - Connect to TiMidity++ MIDI server. See below.
windows    - Windows MIDI. Uses built-in sequencer, for Windows users
```
To select a sound driver, select it in the Launcher, or pass its name via the ```-e``` option to scummvm, for example:

```scummvm -eadlib monkey2```

## AdLib emulation

By default an AdLib card will be emulated and ScummVM will output the music as sampled waves. This is the default mode for several games, and offers the best compatibility between machines and games.

## FluidSynth MIDI emulation

If ScummVM was build with libfluidsynth support it will be able to play MIDI music through the FluidSynth driver. You will have to specify a SoundFont to use, however.

Since the default output volume from FluidSynth can be fairly low, ScummVM will set the gain by default to get a stronger signal. This can be further adjusted using the ```--midi-gain``` command-line option, or the ```midi_gain``` config file setting.

The setting can take any value from 0 through 1000, with the default being 100. (This corresponds to FluidSynth's gain settings of 0.0 through 10.0, which are presumably measured in decibel.)

NOTE: The processor requirements for FluidSynth can be fairly high in some cases. A fast CPU is recommended.

## MT-32 emulation

Some games which contain MIDI music data also have improved tracks designed for the MT-32 sound module. ScummVM can now emulate this device, however you must provide original MT-32 ROMs to make it work:

```MT32_PCM.ROM``` - IC21 (512KB) ```MT32_CONTROL.ROM``` - IC26 (32KB) and IC27 (32KB), interleaved byte-wise

Place these ROMs in the game directory, in your extrapath, or in the directory where your ScummVM executable resides.

You don't need to specify ```--native-mt32```with this driver, as it automatically gets turned on.

NOTE: The processor requirements for the emulator are quite high; a fast CPU is strongly recommended.

## MIDI emulation

Some games (such as Sam & Max) only contain MIDI music data. This once prevented music for these games from working on platforms that do not support MIDI, or soundcards that do not provide MIDI drivers (e.g. many soundcards will not play MIDI under Linux). ScummVM can now emulate MIDI mode using sampled waves and AdLib, FluidSynth MIDI emulation or MT-32 emulation using the ```-eadlib```, ```-efluidsynth``` or ```-emt32``` options respectively. However, if you are capable of using native MIDI, we recommend using one of the MIDI modes below for best sound.

## Native MIDI support

Use the appropriate ```-e<mode>``` command line option from the list above to select your preferred MIDI device. For example, if you wish to use the Windows MIDI driver, use the ```-ewindows``` option.

## Using MIDI options to customize Native MIDI output

ScummVM supports a variety of MIDI modes, depending on the capabilities of your MIDI device.

If ```--native-mt32``` is specified, ScummVM will treat your device as a real MT-32. Because the instrument mappings and system exclusive commands of the MT-32 vary from those of General MIDI devices, you should only enable this option if you are using an actual Roland MT-32, LAPC-I, CM-64, CM-32L, CM-500, or GS device with an MT-32 map.

If ```--enable-gs``` is specified, ScummVM will initialize your GS-compatible device with settings that mimic the MT-32's reverb, (lack of) chorus, pitch bend sensitivity, etc. If it is specified in conjunction with --native-mt32, ScummVM will select the MT-32-compatible map and drumset on your GS device. This setting works better than default GM or GS emulation with games that do not have custom instrument mappings (Loom and Monkey1). You should only specify both settings if you are using a GS device that has an MT-32 map, such as an SC-55, SC-88, SC-88 Pro, SC-8820, SC-8850, etc. Please note that ```--enable-gs``` is automatically disabled in both DOTT and Samnmax, since they use General MIDI natively.

If neither of the above settings is enabled, ScummVM will initialize your device in General MIDI mode and use GM emulation in games with MT-32 soundtracks.

Some games contain sound effects that are exclusive to the AdLib soundtrack. For these games, you may wish to specify ```--multi-midi``` in order to combine MIDI music with AdLib sound effects.

## UNIX native, ALSA and dmedia sequencer support

f your soundcard driver supports a sequencer, you may set the environment variable ```SCUMMVM_MIDI``` to your sequencer device -- for example, to /dev/sequencer

If you have problems with not hearing audio in this configuration, you may need to set the environment variable SCUMMVM_MIDIPORT to 1 or 2. This selects the port on the selected sequencer to use. Then start scummvm with the ```-eseq``` parameter. This should work on several cards, and may offer better performance and quality than AdLib emulation. However, for those systems where sequencer support does not work, you can always fall back on AdLib emulation.

## ALSA sequencer [UNIX ONLY]

If you have installed the ALSA driver with sequencer support, then you may set the environment variable ```SCUMMVM_PORT``` or the config file variable alsa_port to specify your sequencer port. If neither is set, the default behavior is to try both "65:0" and "17:0".

Here is a brief guide on how to use the ALSA sequencer with your soundcard. In all cases, to obtain a list of all the sequencer ports you have, try the command aconnect ```-o -l```. This should give output similar to:

```
    client 14: 'Midi Through' [type=kernel]
        0 'Midi Through Port-0'
    client 16: 'SBLive! Value [CT4832]' [type=kernel]
        0 'EMU10K1 MPU-401 (UART)'
    client 17: 'Emu10k1 WaveTable' [type=kernel]
        0 'Emu10k1 Port 0  '
        1 'Emu10k1 Port 1  '
        2 'Emu10k1 Port 2  '
        3 'Emu10k1 Port 3  '
    client 128: 'TiMidity' [type=user]
        0 'TiMidity port 0 '
        1 'TiMidity port 1 '
        2 'TiMidity port 2 '
        3 'TiMidity port 3 '
```

The most important bit here is that there are four WaveTable MIDI outputs located at 17:0, 17:1, 17:2 and 17:3, and four TiMidity ports located at 128:0, 128:1, 128:2 and 128:3.

If you have a FM-chip on your card, like the SB16, then you have to load the SoundFonts using the sbiload software. Example:

```
sbiload -p 17:0 /etc/std.o3 /etc/drums.o3
```

If you have a WaveTable capable sound card, you have to load a sbk or sf2 SoundFont using the sfxload or asfxload software. Example:

```
sfxload /path/to/8mbgmsfx.sf2
```

If you don't have a MIDI capable soundcard, there are two options: FluidSynth and TiMidity. We recommend FluidSynth, as on many systems TiMidity will 'lag' behind music. This is very noticeable in iMUSE-enabled games, which use fast and dynamic music transitions. Running TiMidity as root will allow it to setup real time priority, which may reduce music lag.

Asking TiMidity to become an ALSA sequencer:

```
timidity -iAqqq -B2,8 -Os1S -s 44100 &
```

(If you get distorted output with this setting, you can try dropping the -B2,8 or changing the value.)

Asking FluidSynth to become an ALSA sequencer (using SoundFonts):

```
fluidsynth -m alsa_seq /path/to/8mbgmsfx.sf2
```

Once either TiMidity or FluidSynth are running, use the 'aconnect -o -l' command as described earlier in this section.

## IRIX dmedia sequencer: [UNIX ONLY]

If you are using IRIX and the dmedia driver with sequencer support, you can set the environment variable ```SCUMMVM_MIDIPORT``` or the config file variable ```dmedia_port``` to specify your sequencer port. The default is to use the first port.

To get a list of configured midi interfaces on your system, run "startmidi" without parameters. Example output:

```
  2 MIDI interfaces configured:
          Serial Port 2
          Software Synth
```

In this example, you can configure ScummVM to use the "Software Synth" instead of the default "Serial Port 2" by adding a line

```
dmedia_port=Software Synth
```

to your configuration file in the section [scummvm], or setting ```SCUMMVM_PORT=Software Synth``` in your environment.

## TiMidity++ MIDI server support

If your system lacks any MIDI sequencer, but you still want better MIDI quality than default AdLib emulation can offer, you can try the TiMidity++ MIDI server. See [hhhere](http://timidity.sourceforge.net/) for download and install instructions.

First, you need to start a daemon:

```
timidity -ir 7777
```

Now you can start ScummVM and try selection TiMidity music output. By default, it will connect to localhost:7777, but you can change host/port via the ```TIMIDITY_HOST``` environment variable. You can also specify a "device number" using the ```SCUMMVM_MIDIPORT``` environment variable.

## Using compressed audio files

### Using MP3 files for CD audio

Use LAME or some other MP3 encoder to rip the cd audio tracks to files. Name the files track1.mp3 track2.mp3 etc. ScummVM must be compiled with MAD support to use this option. You will need to rip the file from the CD as a WAV file, then encode the MP3 files in constant bit rate. This can be done with the following LAME command line:

```
lame -t -q 0 -b 96 track1.wav track1.mp3
```

### Using Ogg Vorbis files for CD audio

Use oggenc or some other vorbis encoder to encode the audio tracks to files. Name the files track1.ogg track2.ogg etc. ScummVM must be compiled with vorbis support to use this option. You will need to rip the files from the CD as a WAV file, then encode the vorbis files. This can be done with the following oggenc command line with the value after q specifying the desired quality from 0 to 10:

```
oggenc -q 5 track1.wav
```

### Using Flac files for CD audio

Use flac or some other flac encoder to encode the audio tracks to files. Name the files track1.flac track2.flac etc. If your filesystem only allows three letter extensions, name the files track1.fla track2.fla etc. ScummVM must be compiled with flac support to use this option. You will need to rip the files from the CD as a WAV file, then encode the flac files. This can be done with the following flac command line:

```
flac --best track1.wav
```

Remember that the quality is always the same, varying encoder options will only affect the encoding time and resulting filesize.

### Compressing MONSTER.SOU with MP3

You need LAME, and our ```compress_scumm_sou``` utility from the scummvm-tools package to perform this task, and ScummVM must be compiled with MAD support.

```
compress_scumm_sou monster.sou
```

Eventually you will have a much smaller monster.so3 file, copy this file to your game directory. You can safely remove the monster.sou file.

### Compressing MONSTER.SOU with Ogg Vorbis

As above, but ScummVM must be compiled with OGG support. Run:

```
compress_scumm_sou --vorbis monster.sou
```

This should produce a smaller monster.sog file, which you should copy to your game directory. Ogg encoding may take a considerable longer amount of time than MP3, so have a good book handy.

### Compressing MONSTER.SOU with Flac

As above, but ScummVM must be compiled with Flac support. Run:

```
compress_scumm_sou --flac monster.sou
```

This should produce a smaller monster.sof file, which you should copy to your game directory. Remember that the quality is always the same, varying encoder options will only affect the encoding time and resulting file size. Playing with the blocksize (-b <value>), has the biggest impact on the resulting file size -- 1152 seems to be a good value for those kind of soundfiles. Be sure to read the encoder documentation before you use other values.

### Compressing music/sfx/speech in AGOS games

Use our ```compress_agos``` utility from the scummvm-tools package to perform this task. You can choose between multiple target formats, but note that you can only use each if ScummVM was compiled with the respective decoder support enabled.

```
  compress_agos effects     (For Acorn CD version of Simon 1)
  compress_agos simon       (For Acorn CD version of Simon 1)
  compress_agos effects.voc (For DOS CD version of Simon 1)
  compress_agos simon.voc   (For DOS CD version of Simon 1)
  compress_agos simon.wav   (For Windows CD version of Simon 1)
  compress_agos simon2.voc  (For DOS CD version of Simon 2)
  compress_agos simon2.wav  (For Windows CD version of Simon 2)
  compress_agos mac         (For Macintosh version of Simon 2)

  compress_agos voices1.wav (For Windows 2CD/4CD version of Feeble)
  compress_agos voices2.wav (For Windows 2CD/4CD version of Feeble)
  compress_agos voices3.wav (For Windows 4CD version of Feeble)
  compress_agos voices4.wav (For Windows 4CD version of Feeble)

  compress_agos Music       (For Windows version of Puzzle Pack)
```

For Ogg Vorbis add ```--vorbis``` to the options, i.e.

```compress_agos --vorbis```

For Flac add ```--flac``` and optional parameters, i.e.

```compress_agos --flac```

Eventually you will have a much smaller _*.mp3, *.ogg or *.fla file_, copy this file to your game directory. You can safely remove the old file.

### Compressing speech/music in Broken Sword

The ```compress_sword1``` tool from the scummvm-tools package can encode music and speech to MP3, Ogg Vorbis as well as Flac. The easiest way to encode the files is simply copying the executable into your BS1 directory (together with the lame encoder) and run it from there. This way, it will automatically encode everything to MP3. Afterwards, you can manually remove the SPEECH?.CLU files and the wave music files.

Running ```compress_sword1 --vorbis``` will compress the files using Ogg Vorbis instead of MP3.

Running ```compress_sword1 --flac``` will compress the files using Flac instead of MP3.

Use ```compress_sword1 --help``` to get a full list of the options.

### Compressing speech/music in Broken Sword II

Use our ```compress_sword2``` utility from the scummvm-tools package to perform this task. You can choose between multiple target formats, but note that you can only use each if ScummVM was compiled with the respective decoder support enabled.

```
  compress_sword2 speech1.clu
  compress_sword2 music1.clu
```

For Ogg Vorbis add --vorbis to the options, i.e.

```compress_sword2 --vorbis```

Eventually you will have a much smaller _*.cl3 or *.clg file_, copy this file to your game directory. You can safely remove the old file.

It is possible to use Flac compression by adding the ```--flac``` option. However, the resulting _*.clf_ file will actually be larger than the original.

Please note that compress_sword2 will only work with the four speech/music files in Broken Sword II. It will not work with any of the other _*_.clu files, nor will it work with the speech files from Broken Sword.

### Output sample rate

The output sample rate tells ScummVM how many sound samples to play per channel per second. There is much that could be said on this subject, but most of it would be irrelevant here. The short version is that for most games 22050 Hz is fine, but in some cases 44100 Hz is preferable. On extremely low-end systems you may want to use 11025 Hz, but it is unlikely that you have to worry about that.

To elaborate, most of the sounds ScummVM has to play were sampled at either 22050 Hz or 11025 Hz. Using a higher sample rate will not magically improve the quality of these sounds. Hence, 22050 Hz is fine.

Some games use CD audio. If you use compressed files for this, they are probably sampled at 44100 Hz, so for these games that may be a better choice of sample rate.

When using the AdLib, FM Towns, PC Speaker or IBM PCjr music drivers, ScummVM is responsible for generating the samples. Usually 22050 Hz will be plenty for these, but there is at least one piece of AdLib music in Beneath a Steel Sky that will sound a lot better at 44100 Hz.

Using frequencies in between is not recommended. For one thing, your sound card may not support it. In theory, ScummVM should fall back on a sensible frequency in that case, but don't count on it. More importantly, ScummVM has to resample all sounds to its output frequency. This is much easier to do well if the output frequency is a multiple of the original frequency.