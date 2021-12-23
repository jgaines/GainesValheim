# Gaines Valheim Server Mods

This repo contains all the config settings and this file which is a list of the mods and where to get them (most are from Nexus, but a few are only available on Thunderstore).

Just an FYI, since I'm running linux and the server is also a linux machine, I end up having to manually download and install all this stuff by hand because there are no good plugin managers that handle both Nexus and Thuderstore and run on Linux.  Thunderstore has a linux mod manager, but it doesn't talk to Nexus.

You guys will probably end up using Vortex as it runs on Windows and talks to Nexus, you might end up having to manually install a few mods from Thunderstore as there are a few authors who don't like Nexus but put out some pretty neat mods.

Any mod marked (client) is a client-side only mod and is optional.  They don't need installation on the server and you can change up their settings however you like.

## Configuration Notes

### Carry Weight

For carry weight, I'm using standard 300 and 150 for belt.  Backpacks add carry weight and the later two add slots but must be worn to get carry weight benefit.  Skills Give More Carry Weight can add up to 300 if you max out 15 skills (0.2 per skill point for 15 skills).  Also all items weigh 70% of original weights.

Heh, just tested out the above settings and I think even Sam will be happy with the results.  I move like a tortoise with bronze armor and backpack on (25% speed reduction, 35% with sword and buckler out).  Total carry capacity is less than with a cart, but a lot more managable over rough terrain.

## Framework/Lib Mods

These mods don't do anything by themselves, but are framework/libs for other mods.

### BepInEx 5.4.17.0

https://valheim.thunderstore.io/package/denikson/BepInExPack_Valheim/

This is the framework that allows all the other mods to work.  I'm pretty sure any mod manager will be smart enough to install this correctly with the unstripped_corlib files and all.

### Extended Item Data Framework 1.0.5

https://www.nexusmods.com/valheim/mods/281

Needed by a few mods, not really sure what it does as I haven't bothered to read the readme file. :)

### Hookgen Patcher 0.0.3

https://www.nexusmods.com/valheim/mods/505

Not really sure what this does, just that Terraheim needs it.  Also in the logs, I see `Loaded 1 patcher method from [BepInEx.MonoMod.HookGenPatcher 1.2.0.0]`, which sort of looks like it comes from this mod, but the version on the download page is 0.0.3.

### Jotuun 2.4.5 (The Valheim Library)

https://www.nexusmods.com/valheim/mods/1138

This is shared library that is the result of some really awesome collaboration between modders (it's the merging of two older now deprecated libraries).  Any time you see a mod that talks about JVL, that's this.


## Challenge/Difficulty

These are mods that alter the difficulty of the game.  Creature Level and Loot Control makes it harder, while Terraheim and Valheim Legends make us tougher, so in theory they'll balance out.  (Fingers crossed.)

### Atos Arrows JVL 1.0.0

https://www.nexusmods.com/valheim/mods/1301

Adds a bunch of new arrows including bone ones (Use for bones beyond the stone age!).  Has arrows with blunt attack (for crystal golems in mountains).  Also has heavy arrows made from core wood for higher level mobs.  For example, it took me 50 heavy fire arrows to take down a 3 star regenerating Fuling Brute.  Normal arrows could barely keep up with his regen, and my bow would have probably broken before I got him down.

### Better Stamina 1.2.0.0

https://www.nexusmods.com/valheim/mods/153

Tweaks stamina use, regen, etc.

### Creature Level and Loot Control 4.4.5 aka CLLC or simply Creature Leavel

https://valheim.thunderstore.io/package/Smoothbrain/CreatureLevelAndLootControl/

Super configurable mod that lets you tweak stars and other stats on mobs based on all sorts of criteria.  Default config isn't too bad as it just ups the stars chances the further from spawn you go.  (Though a 5 star Fuling Berserker could be scary.)  One other thing that it does is repopulate dungeons and camps so you can revisit them a few days (3 by default) later and they won't be empty.

I turned on Affixes and Infusions for normal mobs (not bosses, a 3 star Moder was enough without her being regenerating too).

I also enabled creature sectors, which basically makes creatures ramp up in an area as you kill more creatures in that area.  I'm not sure I fully understand how this works, but I did manage to trigger it clearing a Fuling camp.  I enabled it for all zones (the 1-5 rings).  Good or bad news: It appears that kills by your pets don't count.  I was sort of hoping they did, so the area around my camp would become a crazy battle zone.

### Forgotten Biomes 0.0.15

https://www.nexusmods.com/valheim/mods/1128

Adds already existing structures, plants, rocks and other formations of things to many biomes.  It definately makes the world feel less barren so far.  Doesn't really affect the difficulty much, but does make it harder to tell the difference between meadows and black forest.

### Terraheim - Weapons Tools and Armor 2.2.0

https://www.nexusmods.com/valheim/mods/803

This is a major overhaul of the armor system.  Every set can be used to end game through reforging with higher tier materials.  Each armor set has perks that favor a specific play style.  Also fills in a lot of the gaps in the weapons and tools (for example: blackmetal picks and actual flametal weapons).  Log also shows a "TerraheimItems 2.1.0" mod being loaded, not sure why that version differs from main mod.

### Valheim Legends 0.4.2

https://www.nexusmods.com/valheim/mods/796

Adds a class system with each class getting three special abilities and ocassionaly a passive.  Seems to work well with Terraheim as that makes armor more role specific.


## Quality of Life

### Anti Slip Shoes 1.0.0 (client)

https://valheim.thunderstore.io/package/nearbear/AntiSlipShoes/

Increases the slope angle (from 30 to 50) you can walk up without sliding.

I'm pretty sure this is purely client side, I was using it with our unmodded server and it was functioning just fine.

### Beasts of Burden 1.0.3

https://www.nexusmods.com/valheim/mods/545

The main purpose of this is to allow attaching carts to boar, wolves and lox.  That part seems somewhat broken in that I was finding the animals would disconnect at the slightest restance like pulling a cart uphill.  The main reason I keep this loaded is that it lets me command boar and lox to follow which is way easier than pushing them around.

### Better Ladders 0.2.0 (client)

https://www.nexusmods.com/valheim/mods/1054

Makes ladder climbing smoother, just like stairs.  Shows up in logs as "kgladder".

### Better Networking 1.2.2

https://www.nexusmods.com/valheim/mods/1570

If you've been experiencing lag or desync when playing with your friends, this is the solution!

### Cartography Skill and Spyglass 2.1.0

https://www.nexusmods.com/valheim/mods/394

The more you explore the larger your mapping radius becomes, eventually you'll get past that point where you can see the shore, but your map isn't showing it.  Spyglass is fun too.

### Change Forsaken Power 0.0.3 (client)

https://valheim.thunderstore.io/package/CakeBlood/Change_Forsaken_Power/

Hotkey cycle through your known forsaken powers.  I disabled the reset feature and remapped the swap hotkey to F4 to avoid other key use by other mods.

Hoping there's a fix for this some day.  It is a bit broken.  So far, I've unlocked deer, tree and blob.  If I activate deer or tree, I can toggle between those two.  If I activate blob, the other two drop off and I'm just stuck with blob.  Appears to work again once I activated Modor, can cycle between all four now.

### Craft Build Smelt Cook Fuel Pull From Containers 2.2.1

https://www.nexusmods.com/valheim/mods/40

I opted to use this rather than the similar features from Valheim+ because this one has a feature that I really want: If you hold left ctrl and use the hammer to craft an item, it will instead pull the mats for that item into your inventory.  So for those things like portals, boats, carts that you might want to load up the mats for, this is the answer.

### Crafty Carts Remake 2.1.0

https://valheim.thunderstore.io/package/OdinPlus/CraftyCartsRemake/

Crafting stations on carts, has normal workstation, forge and stone cutter (all at base level).  The idea is that rather than keep making and breaking these all around, just drag the cart to next work site.

Also available on Nexus but uploaded by someone other than author so verify latest version is available there before relying on this link: https://www.nexusmods.com/valheim/mods/1576

### Creature Level And Loot Control Fix

https://valheim.thunderstore.io/package/FixItFelix/CreatureLeveLAndLootControl_fix/

Based on the description: Delete the default YAML provided inside the plugins folder to avoid misconfiguration in single player use.  I'm not sure if we'll need this.  But if we do, you'll need to make sure the paths specified in the config file it contains are correct for your installation of CLLC.  Also it requires the additional Thunder Store only mod This Goes Here (listed below).

### Digitalroot Valheim Slope Combat Fix 2.0.0 (client)

https://www.nexusmods.com/valheim/mods/1658

Make sure you get this one as there are others that don't work quite right.  Allows attacking up/down slopes.  Doesn't seem to bugger up bow aim like the original mod did.

### Extended Player Inventory 0.3.1

https://www.nexusmods.com/valheim/mods/1356

Larger inventory and extra slots for armor and 3 extra hotkeyed slots.  With all the extra build tools and food drops extra slots are really needed.

### Faster Boats 0.0.1

https://www.nexusmods.com/valheim/mods/349

Makes ships faster.  Probably going to need this to counter some of the hopped up serpents from Creature Level and Loot Control.  A Quick (from CLLC) sea serpent may not be able to be outrun even with this.

### Floating Items 1.0.0

https://www.nexusmods.com/valheim/mods/241

Makes all drops float.  No more "Oh shit! There goes that loot into the deep water.".  I also considered a mod that lets you dive, but thinking that's more likely to break something and finding crap under water doesn't sound like fun.

### Gathering Skill 2.0.2 and Skill Injector 1.1.1

https://www.nexusmods.com/valheim/mods/342
https://www.nexusmods.com/valheim/mods/341

Gathering Skill makes late game gathering less tedious by giving greather yields.  Needs Skill Injector.  I nerfed the heck out of this by dropping the max skill modifier from 4 to 2, so at max skill you get double drops not quadruple.  I also made the skilling up from 1 per pick to 0.1 per pick so you'll have to pick a lot to get the bonus.  Terraheim adds a belt that gives +1 extra on domesticated plants and +2 extra on wild plant so if you really want to collect a lot you have to wear the belt.

I switched it from Linear to PartialRandom so that there's a benefit to the skill prior to maxing it out.  With the default of Linear and max of 2, you get no benefit until it's maxed.  Now if your skill is 25, it's a 25/75 chance of getting 1 or 2.

### Golden Judes Equipment 1.4.0

https://valheim.thunderstore.io/package/GoldenJude/Judes_Equipment/

I decided to add this in because it offers a number of alternate armor sets, but mostly because I wanted the backpack, which is the tier 0 backpack in this modpack.  It simply adds 100 carry weight, goes in the cloak slot and adds no extra slots.  It's atainable before you get any metal as it only takes deer hide and leather scraps.  It only has a 5% speed reduction.

### Handy Portals 1.0.0.7

https://disk.yandex.com/d/sL-KLbai_Cupig

Makes it so entering a portal brings up the map then you click on desired destination portal.  No need to have portal hubs anywhere.  Also auto map pins portals with a config setting (which I turned on because it also seems to disable the portal pin on map).

This has a Nexus page at https://www.nexusmods.com/valheim/mods/471, but based on a discussion thread there about some excessive log spam, which we were seeing, I've downloaded a patched version from the weird disk.yanex.com location above.  It appears to have gotten rid of the log spam.

I used to use [AnyPortal](https://www.nexusmods.com/valheim/mods/170) in the past, but it's broken since H&H.  I found it a little easier since you could set a portal to a fixed location and leave it.  Changing it only when needed.

### Jotunn Backpacks 2.0.0

https://www.nexusmods.com/valheim/mods/1416

Adds two backpacks, one made with bronze/deerhide and a second made with silver/wolfhide.  I've configured them so they add carry weight only when worn.  They both add extra slots and go in the cloak slot and slow you down by 15%.

### Mount Up 3.2.5

https://www.nexusmods.com/valheim/mods/1091

Ride boars and wolves.

### PressurePlate for Doors 0.6.0

https://www.nexusmods.com/valheim/mods/498

Basically works like player only pressure plates from Minecraft.  Comes in two ugly textures: wood and stone, that don't really match anything.  Author added a crystal one at my suggestion. :)

### Teleport Wolves 0.2.2

https://www.nexusmods.com/valheim/mods/217

This appears to also allow teleporting of boars and lox.  Moving livestock around without this is as we saw not very feasible.  Though smaller animals might fare better on ships than a lox.  ValheimRaft might be an alternate solution as you could build a pen on the raft to stick the animals in.  Though a raft doesn't solve the issue of getting animals out of trenches.  (Ringing your camp in a raised earth wall instead of a trench does though. ;)

### This Goes Here 1.2.0

https://valheim.thunderstore.io/package/ASharpPen/This_Goes_Here/

This is a weird little mod that allows some basic file operations to be encoded in config files.  It's purpose in this pack is to run the Creature Level and Loot Control Fix script to clean up some config files that get installed by CLLC into the plugins folder.

### Triple Bronze JVL 1.1.0

https://www.nexusmods.com/valheim/mods/1463

Makes bronze produce proper number of ingots based on number of ingots input.  This makes bronze easier to make which is good because the bronze armor is not actually a viable set with Terraheim (also bronze is used to reforge leather/trollhide in their progression to end-game).

### Valheim Plus 0.9.9

https://www.nexusmods.com/valheim/mods/4

The original Kitchen-Sink mod.  This thing has **lots** of options and tweaks to the game.  I normally turn off about half of it, but the automation bits alone are worth it.  This also has auto-repair, dodge key mapping, and sleep without resetting spawn point.

Just an FYI if you're mucking about with mods: If you've turned on a lot sections in this mod and are getting weird behaviour from other mods, there's a good chance that some setting in valheim+ is breaking your other mod.  Like turning on the [Inventory] section can wreak havoc with any other mod that extends ANY inventory space.  Even turning off individual settings within the [Inventory] section won't fix the issue, you have to turn off the whole section.

### Valheim Recycle 2.0.0 (client)

https://www.nexusmods.com/valheim/mods/425

Lets you recycle most things at the appropriate crafting station.


## Building and Decorations

### Black Metal Build Pieces 0.0.3

https://www.nexusmods.com/valheim/mods/1605

Adds black metal versions of all the iron pieces including the support beams.  Really nice to have a use for all the black metal that piles up late game.

### Build It 1.3.1

https://www.nexusmods.com/valheim/mods/1385

Has some really cool stuff and its own build hammer.  It has an outhouse and toilet seat, plus some nice alternative storage solutions.  (There's still a visual bug with rain/snow and their roofs, but they function properly, you just see the rain coming through.)

### Clutter 0.1.0

https://www.nexusmods.com/valheim/mods/1350

Lots of knick-knacks to decorate the home with custom "hammer" in the form of a bucket.  More of this sort of stuff is what I was expecting from H&H.

### Moar Build IDs 1.0.8

https://valheim.thunderstore.io/package/OdinPlus/MoArBuIlDs/

The whole goblin village can now be built you also can build the iron gate from the crypts now.  Some items are missing snap points.

### More Gates 1.0.10

https://www.nexusmods.com/valheim/mods/1087

 Windows, doors, gates, a drawbridge and various other pieces.

### OdinArchitect 0.1.3

https://valheim.thunderstore.io/package/OdinPlus/OdinArchitect/

More alternate build pieces and its own hammer.  Some functional ones like compost heap which turns neck tails/boar meat into fish bait, which can then be used in an auto fisher (turns fish bait into fish) and a bird house (turns fish bait into feathers).  To automate two annoying gathering processes.

### Pageable Build Hud 1.0.2

https://www.nexusmods.com/valheim/mods/1516

Adds a next/prev button to bottom of build pages.  Some of the build mods will eventually fill up some of the build pages, so while you won't need it to start, by black metal level, you'll need it.

### Plant Everything 1.9.1

https://www.nexusmods.com/valheim/mods/1042

This is semi-functional in that it allows planting of most of the pickables as well as a number of purely decorative plants.

### Plant It 0.1.2

https://www.nexusmods.com/valheim/mods/1251

Adds a bunch of decorative plants and a build hammer that looks like a shovel.  Nexus link is a repost, original post is https://valheim.thunderstore.io/package/OdinPlus/PlantIt/

### Rune Magic 1.1.3

https://www.nexusmods.com/valheim/mods/1359

A lot of the rune powers relate to building, including restore terrain, level terrain and numerous rocks that you can summon in.  The rune focus itself functions like a hammer in that you select which rune spell to cast using a hammer like interface.  Also includes some utility things like a sense surrounding critters ability.

Heh, be really really sure about wanting one before placing a Megalith.  They're a bitch to tear down.

### Seed Totem 4.1.0

https://www.nexusmods.com/valheim/mods/876

Adds two seed totems, both of which sem-automate the farming process.  The basic totem plants in a circle around it, I've fixed the size to 3 radius so it only manages about 30-40 plants at a time.  The advanced totem manages plants in a rectangle behind it that is adjustable.

### Use Equipment in Water 0.2.1.0 (client)

https://www.nexusmods.com/valheim/mods/121

Allows you to use your Equipment while swimming in water.

### Useful Paths 1.0.5.0

https://www.nexusmods.com/valheim/mods/438

Players run, jog, and walk faster and use less stamina when traversing leveled ground, paths, paved roads, wood, stone, iron, or hardwood. The movement boost and stamina drain decrease values can also be configured.


## Offbeat/Fun

### Hallowheim 1.0.1

https://www.nexusmods.com/valheim/mods/1602

Adds a bunch of silly halloween themed items to game.

### Steamheim Airships 1.1.3

https://www.nexusmods.com/valheim/mods/1322

Adds two airships to the game one honking big one and a wee scout ship.  Looks like they can be individually enabled, so maybe just the wee one for shits and giggles.


## Optional (client)

These are all optional client-side things that I run so you'll see configs for them.  I'm leaving off versions on these as they shouldn't matter, I usually update them in my client plugins whenever I see a new version.

### Build Camera (client)

https://www.nexusmods.com/valheim/mods/226

Lets you float the camera view to eliminate the need for scaffolding and allowing you to build in cramped areas and from angles unobtainable without it.  Like snapping a post to the underside of another post under water under a bridge you're standing on.

I know, Sam considers the challenge of building to be fun.  I personally find the ability to snap items to the underside of things to be way too convenient to not use this.

### Clock (client)

https://www.nexusmods.com/valheim/mods/85

Using this in fuzzy mode gives a nice display in the form of Morning, Evening, Midnight, etc.  Just how you'd expect someone without a watch to describe time.

### Configuration Manager (client)

https://www.nexusmods.com/valheim/mods/740

Adds an in-game config manager to most mods.  Just hit Esc to bring up menu (to free cursor) then F1 to bring up Config Manager.  Can also be accessed at main menu before starting a game.

### Custom Audio (client)

Lets you muck with audio in game.  After installing this, I installed [Realistic Animal Sounds](https://www.nexusmods.com/valheim/mods/574).  Might be why my tamed wolves bark, though not sure since I haven't run pure vanilla setup with latest game update.

### Custom Textures (client)

Lets you muck with textures in game.  It just alters the texture of whatever crap you load into it.  I loaded [Ivy's Texture Pack](https://www.nexusmods.com/valheim/mods/115) and [Woad Warrior Skin](https://www.nexusmods.com/valheim/mods/219) into it.  Ivy's makes a lot of things look way less crappy and the Woad one adds nice but not overwhelming tattoos.

### Death Tweaks (client)

https://www.nexusmods.com/valheim/mods/1068

This is the mod I use to eliminate corpse runs.

### Farm Grid (client)

https://www.nexusmods.com/valheim/mods/449

Helps lay out plants/trees in a properly spaced grid.  With Seed Totems, I mostly use this for laying out large tree farms.

### First Person View (client)

https://www.nexusmods.com/valheim/mods/44

I mostly use this to get close in when cooking.  It apparently has issues if you run around a lot in first person view.  Also the mod's files are confusingly named CameraMod.

### Golden Judes Blacksmith's Tools (client)

https://valheim.thunderstore.io/package/GoldenJude/Blacksmiths_tools/

This is a client-side mod to make the armors from Golden Judes Equipment look better.  If you don't install it, you may see body parts poking through if you wear armor from that mod.

### Improved Dverger Circlet (client)

https://www.nexusmods.com/valheim/mods/79

Makes Dverger light white and lets you adjust the beam.  Between this and Invis Helm below makes Dverger ciclet worth having.

### Inventory HUD (client)

https://www.nexusmods.com/valheim/mods/1089

Adds a little bag icon with slots used/total and weight used/total.

### Invis Helm (client)

https://www.nexusmods.com/valheim/mods/192

Lets you hide helmet but still have it on.  Also allows using Dverger while wearing helmet, put on dverger, then put on helmet and light remains.  I mapped it to F3 because I pretty much never toggle it (toggling it has seemed a little glitchy).

### Map Teleport (client)

https://www.nexusmods.com/valheim/mods/251

Allows you to teleport by shift-clicking on the map.

### Mass Farming (client)

https://www.nexusmods.com/valheim/mods/527

Makes farming and harvesting easier.  IMO goes hand in hand with extended pickup range (from Valheim+).

### Minimal Status Effect (client)

https://www.nexusmods.com/valheim/mods/75?tab=bugs

Shrinks the status effect list and puts it in a vertical list below the minimap. Position and size are customizable.

### Movable Inventory Windows (client)

https://www.nexusmods.com/valheim/mods/577

You'll probalby want this to move chest/container window down below backpack window.

### Nexus Update Check

https://www.nexusmods.com/valheim/mods/102

Alerts you to updated mods on Nexus.  Unfortunately there's nothing like this for ThunderStore.  It should be safe to update any client side mods, but anything server side will probably have to be a coordinated upgrade along with the server.

### Overhead Axe Swing (client)

https://www.nexusmods.com/valheim/mods/465

Adds a secondary attack to all the basic axes that swings like a pickaxe.  With the slope fix, it seems you can do without this, but I still run it because I like the animation.

### Quick Stack (client)

https://www.nexusmods.com/valheim/mods/29

Press a configured key (` by default) to quickly stack items from your inventory into a currently opened or nearby containers.

### Recipe X (client)

https://www.nexusmods.com/valheim/mods/1636

Lets you add multiplied recipes for vanilla recipes, basically like the 15 bronze bars vs. the 3 bronze bars recipes.  I'm pretty sure this is client side only.

### Show Container Contents (client)

https://www.nexusmods.com/valheim/mods/829

Shows container contents when you hover over them.

### Simple Sort (client)

https://www.nexusmods.com/valheim/mods/584

As the name implies, sorts container contents when you access a chest.

### Skills Give More Carry Weight (client)

https://www.nexusmods.com/valheim/mods/462

Configured to allow 15 skills to add 0.2 per skill point increase to carry weight.  Skills that affect carry weight: Axes, Blocking, Bows, Clubs, Jump, Knives, Pickaxes, Polearms, Run, Sneak, Spears, Swim, Swords, Unarmed, and WoodCutting.  Total if you max out all those  skills is an extra 300 carry weight.

### Split Stack Text Input (client)

https://valheim.thunderstore.io/package/DeekyJay/SplitStackTextInput

Configured so that right clicking on the stack split scrollbar opens a text input window where you can type in a number.

### Take Me Home (client)

https://www.nexusmods.com/valheim/mods/187

Adds two teleport hotkeys.  One takes you to your spawn point the other returns you to where you where last time you returned to spawn.  Quite cheaty, allows teleporting with anything.

### Valheim Configuration Manager (client)

https://www.nexusmods.com/valheim/mods/740

I'm pretty sure this is editing your local configs.  Be somewhat careful about what you edit, as editing some configs like certain sections of Valheim Plus configs can make it so you can't log in.

### Valheim Veinmine (client)

https://www.nexusmods.com/valheim/mods/556

Allows whole ore/rock mining with a hotkey.


