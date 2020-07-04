---
layout: default
has_children: false
parent: Guides
title: Boot-Params
nav_order: 5
---

# Boot Params

## What are boot params?

A boot param is a special number which allows you (if used appropriately, see below) to go directly to a specific part of a game. These boot params are mostly useful for debugging and playtesting a game; you get teleported to a certain situation in a game, with some of the items appropriate for it. It is not always possible to continue and complete a game from this, because you may lack important items. But for us developers, it's very helpful, because we can quickly get to trouble spots in a clean state, and try to reproduce any bugs you report to us.

These boot params do not exist by chance or magic: they were put into the game data by the original developers of the games, and were meant for exactly the same purpose we use them for: to help in debugging the game. Of course, they also make a nice cheat system (with some caveats, as I tried to outline above).

Note: In some SCUMM games, the boot params can produce a room with music and the cursor, but without actual graphics. This was known to happen with the original executables as well.

### How do I use a boot param?

Pick a game from the list below, and choose a boot param for it. Then, specify it on the command line like this:

```./scummvm -d0 -b BOOTPARAM TARGET```

Or on MacOS like this:

```open /Applications/scummvm.app --args -d0 -b BOOTPARAM TARGET```

The TARGET in the above command should typically be the ScummVM ID value of the game you are targeting. This means that you should have already added this game successfully in ScummVM and looked up its specific ID (eg. via the Edit Game dialogue for the specific game entry).

Please use the ```--list-targets``` command line option first to list available configured and valid targets to use with the boot parameter command.

To be a bit more specific: Let's say you want to get into the hut of the cannibals in Monkey Island 1. Well, the table below tells us that this is boot param 5555, and the target is "monkey". So, enter this on the command line:

```./scummvm -d0 -b 5555 monkey```

(By the way, this would also work with monkey, monkeyvga etc.).

### How did we generate these tables?

Some of these lists are based on the output of ./scummvm -d1 -b1 TARGET; some information is also from this article. These may contain some mistakes. Ultimately we plan to correct these and maybe enhance the descriptions a bit...

### I see a lot of question marks in some of the tables, why?

Some of the games contain descriptions for the boot params; some don't. In the latter case, we have to manually fill in the descriptions. This hasn't been done in all cases yet, as you can see.

Help here is welcome -- if you want, feel free to fill in some of the gaps and send us your work, we'll be happy to integrate it here.

---

## Games

### The Secret of Monkey Island

Some of the boot params listed in the following table only work in the CD/Mac version of Monkey Island (and not in 'monkeyega' and 'monkeyvga'). Those are marked with an asteriks (_*_) symbol (except for the cases we overlooked ;-).

In addition to the boot params listed below, you can use values greater than 900 to be teleported to specific rooms. To be precise, if you give the number x, then you get sent to room (x-700).

Furthermore, in the CD/Mac versions of Monkey (target 'monkey', not 'monkeyvga' or 'monkeyega), you can specify a boot param between 3000 and 3777 (including both numbers). It's currently not documented what those boot params do precisely.

Finally, boot params not covered by the list below will be interpreted as raw room numbers and cause the game to start in that room.

```

Param	Description
1	Monkey Island
2	Monkey Island Map Bottom - By Crack
3	Monkey Island Map Centre Left - By Fort
4	Monkey Island Map Centre
5	Monkey Island Map Centre Right - By Monkey Head Clearing
6	Monkey Island Map Top - By Cannibal Village
7	Cabin on Ship - Before ship intro
110	Outside Sword Master's with sword and LeChuck's note
111	Melee lookout point with sword
112	Outside swordmasters with sword (different number of insults known?)
113	Outside swordmasters with sword (different number of insults known?)
114	Outside swordmasters with sword (different number of insults known?)
115	Outside swordmasters with sword (different number of insults known?)
213	Outside cannibal hut with voodoo root
321	Govenors mansion with sword file and idol
332	Underwater at Melee dock
333	Close-up end cutscene
334	Close-up end cutscene
353	Stans with credit note
408	Cannibal Village, outside hut with monkey head key, leaflet, wimpy little idol
415	Melee Island lookout point with breath mints and rubber chicken
444	Outside governors mansion with meat and yellow petal
456	Jail with breath mints and melting mug of grog
501	Ship Kitchen
555	Melee Island Bridge
666	Scumm Bar -empty
707	Store - storekeeper away
759	Melee Dock
777	Circus tent with pot and hunk of meat
789	Monkey Island Map Bottom - By Crack with 2x rope
800	Melee Island Forest
878	Monkey Island River Fork
888	Outside Smirk's with sword and 50 pieces of 8
900	Monkey Island Upper Beach
999	Caverns Under Monkey Island by ship with magnetic compass, head of naviagator, necklace of navigator
1111	Ship Intro
1212	Melee Dock with Navigator Head, Navigator Necklace, Root Beer Seltzer
1436	Monkey Island - Bottom of crack with magnetic compass, pamphlet, leaflet, brochure, 3 bananas, oars
2221	Ship Kitchen with spell ingredients
2222	Ship deck with breath mints and rubber chicken
2299*	Ship Deck with Pamphlet, leaflet, brochure, rope, gunpowder, flaming mass and pot
3777*	Melee Island lookout with 2x 300 pieces of eight, sword, shovel, breath mints, rubber chicken
4313	Cannibal Village, outside hut with monkey head key, oars, magnetic compass, pamphlet, leaflet, brochure, navigator head, navigator necklace
4444	Monkey Island - By Monkey with 5 bananas and monkey head key
5555	Inside Hut in Cannibal Village
6342*	Ghost Ship Main Deck, outside hut with monkey head key, oars, magnetic compass, pamphlet, leaflet, brochure, navigator head, navigator necklace
6565	Monkey Island beach by banana
6666	Outside Monkey Head with monkey head key
6767	Ship Intro
7777	Monkey Island beach by banana, Guybrush and Rowboat invisible
7981	Monkey Island River Fork after dam blown with 3 bananas, magnetic compass, pamphlet, leaflet, brochure
8742	Cannibal Village, outside hut with monkey head key, oars, magnetic compass, pamphlet, leaflet, brochure
8888	Caverns Under Monkey Island by Bob after ship has sailed (escape with Toothrot)
8889	Caverns Under Monkey Island by Bob after ship has sailed (escape with crew)
8989	Melee Island Church during wedding
9432*	Monkey Island Beach, with magnetic compass, pamphlet, leaflet, brochure
```

### Monkey Island 2: LeChuck's Revenge

Target: monkey2. Parts of the following table were contributed by Ben Gorman and John Gamble. Thanks, Ben and John!

```
Param	Description
123	Men of Low Moral Fiber, laundry claim
213	won drinking contest, telescope, mirror, bottle near-grog
300	governor phatt
323	call box in forest
332	booty island overhead, invitation
333	booty island overhead, invitation dress
353	booty island outhouse
400	forest?
408	scabb island swamp with crate
409	stans with hammer and nails
415	costume shop with invitation
456	woodtick
459	Scabb Island Hill in back of cemetery, Carrying: Shovel
494	captain dredd's ship, heap of stuff
495	woodtick, gold, monacle, shovel
498	woodtick hotel, voodoo doll, pins
500	hotel with mud
501	Scabb Island Inside Largo's Hotel Room, On Ground: Laundry Ticket, Toupee
550	outside drinking contest house
596	Phatt Island Pump, Carrying: Jojo
598	The Bloody Lip with banana and library card
600	elevator
619	Booty Island Shop, On Ground: Map Piece, Horn, Mirror, Saw, Feather Pen, Collector's Plate. Carrying: 420 Pieces o' Eight, Monkey head, Parrot Chow, Spit Plaque
666	Phatt Island arrest
667	Phatt Island
668	Phatt Island Roulette Wheel
669	Phatt Island Back Alley, Carrying: 4 map pieces, toupee, spit, bone, bra, straw, drinks (red, green, blue), shovel, nails, hammer, paper, monocle, rat, voodoo doll (Largo), pins, oar
675	Booty Island, On Ground: Plank. Carrying: (same as 669)
676	Phatt Island Warf, Carrying: Fish
677	Phatt Island Warf, Carrying: Fish
704	Phatt Island Governor's Bedroom, On Ground: Famous Pirate Quotations. Carrying: Useless Library Book
707	Booty Island Cliff Side, Carrying: Fishing Rod, Horn, String, Paper, Spit Encrusted Paper, Map
714	Phatt Island Outside Cottage, Carrying: Telescope, Near-Grog, Mirror, Map
726	Booty Island Upstairs in Marley's Mansion, Movie: Busted stealing map piece
800	card catalog
818	Bloody Lip kitchen
819	The Bloody Lip
820	Woodtick
850	map
878	Phatt Island with small key
887	Scabb Island Woodsmith's Hut, Carrying: 420 Pieces o' Eight, Broken Oar
888	Scabb Island Pirates, On Ground: Rat. Carrying: Saw, Squigglies, Stick, String
890	Booty Island 6112 pieces o' eight
897	Scabb Island Map
898	Phatt Island with Kate leaflet
899	Booty Island 276 pieces o' eight
900	scabb island overhead, with crypt key, pirate quotes, ash-2-life
906	Scabb Island Peninsula, Carrying: 420 Pieces o' Eight, Monocle, Shovel, Knife, String, Stick, Voodoo Doll (Largo), Pins, Spit Encrusted Paper
907	Dread's Boat (On Sea), On Ground: Parrot Chow. Carrying: Dread's Map
908	Dread's Boat (On Sea), On Ground: Parrot Chow. Carrying: Dread's Map
909	Dread's Boat (On Sea), On Ground: Parrot Chow. Carrying: Dread's Map
910	Dread's Boat (On Sea), On Ground: Parrot Chow. Carrying: Dread's Map
989	Booty Island 6112 pieces o' eight and shipwrecks book
993	Dinky Island Inside Hole With Treasure Chest, Carrying: Crowbar & Rope
994	Dinky Island Beach, Carrying: 2 Crackers
995	Dinky Island Jungle (Pile of Rocks), Carrying: Shovel
996	Dinky Island Beach, Carrying: 3 Crackers
997	Dinky Island Beach
998	Dinky Island 'Big X', Carrying: Shovel, Dynamite, Matches, Crowbar & Rope
999	Dinky Island Beach, Carrying: Shovel
1000	scabb island outside shack, heaps of stuff
1001	Phatt Island Movie: Initial Entry (Wanted + Arrested)
1050	phatt island overhead
1100	wally hanging on chains in lechucks dungeon
1297	Scabb Island Wally's Room, On Ground: Monocle. Carrying: 4 Map Pieces
1298	Scabb Island Wally's Room, On Ground: Monocle. Carrying: 3 Map Pieces
1300	scabb island swamp
1350	lechuck's fortress docks
1550	Men of Low Moral Fiber
1600	fish?
1700	underground tunnels
1800	wally at desk
1850	cliff side
1967	Booty Island Treehouse Pile of Maps, Carrying: Dog
1968	Phatt Island Outside Cottage, Carrying: Telescope, Drinks (Green, Blue, Yellow, Red, Purple, Brown, Orange, Empty), Straw, Near-Grog
1974	Beach with paper
1976	Scabb Island Inside Crypt, Carrying: Famous Pirate Quotations, Ash-2-Life
1977	Captain Kate's Ship, Movie: unsuccessful Dive
1978	Scabb Island Inside Crypt, Carrying: Famous Pirate Quotations, Ash-2-Life, Key
1984	Beach cutscene
1985	Scabb Island Voodoo Hut, Carrying: Toupee, Bra, Spit, Bone
1989	Booty Island Marley's Party, On Ground: Map Piece
1990	Carpenters
1991	Scabb Island Swamp, On Ground: Crate. Carrying: 4 Pieces o' Eight, Telescope, Fishing Pole, Crypt Key, Hammer, Green Drink, Straw, Near-Grog, Jojo, Library Card, Lens, Organ, Stick, Small Key, Ash-2-Life, Juju Bag, Shovel, Knife, String, Stick, Doll (Largo), Pins, Spit Encrusted paper, Map, Sign, Horn, Saw, Wreath, Cap, Plate, Hat, Quill, Books (Shipwrecks, Pirate Quotes, Joy of Hex)
1992	Dinky Island Dark Room With Lightswitch, Carrying: 4 Pieces o' Eight, Telescope, Fishing Pole, Crypt Key, Hammer, Green Drink, Straw, Near-Grog, Jojo, Library Card, Lens, Organ, Small Key, Ash-2-Life, Juju Bag + Contents, Shovel, Spit Encrusted paper, Map, Sign, Horn, Wreath, Cap, Plate, Hat, Quill, Books (Shipwrecks, Pirate Quotes, Joy of Hex), Hankie, Glass, Broken Bottle, Rope, Box
1993	LeChuck's Fortress Movie: Hanging in torture chamber
1998	Booty Island Shop, Carrying: 500 Pieces o' Eight (x2), straw, Drinks (Green, Red, Blue), Shovel, Hammer, Nails, Bra, Paper, Monocle, Rat, Doll (Largo), Pins
1999	LeChuck's Fortress Movie: Escaping (Explosion)
2001	Booty Island Outside Marley's Mansion
2010	Woodtick pre-largo intro
2061	Booty Island Ville De La Booty, Carrying: Horn, Drinks (Green, Red, Empty), Straw
3383	Scabb Island Map With Dread's Ship Available
4478	Movie: Part II Four Map Pieces
6711	LeChuck's Fortress Maze Junction With Lots of Signs, Carrying: Spit Encrusted paper (Although when selected it is called 'Spit Dripping Down Wall)
8811	Booty Island Big Tree, On Ground: Plank. Carrying: Spit Encrusted Paper, Oar
9000	Dinky Island Underground in Elevator, Carrying: Helium Balloon, 2 Helium-Filled Surgical Gloves
9065	Phatt Island Outside Jail, Carrying: Dread's Map, hand & Map
9066	Booty Island Ville De La Booty, Carrying: 2 Map Pieces, Dread's Map
9090	Dinky Island Underground Lightswitch Room, On Ground: Ticket. Carrying: Syringe, Voodoo Doll (LeChuck)
9898	Dinky Island Underground Lightswitch Room, On Ground: Ticket.
9999	Dinky Island Underground Lightswitch Room (Dark), Carrying: Juju bag, Hankie
10001	Start game without rolling demo, easy mode
11111	Beach
```

### Indiana Jones and the Fate of Atlantis

Target: atlantis. The following list was contributed by Laura Abbott. Thanks a lot, Laura!

(TODO)