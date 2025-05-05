# Salvage Proposal 2

| Designers | Implemented | GitHub Links |
|---|---|---|
| Princess Cheeseballs | :x: No | TBD |

## Overview

Enough time has passed between the previous Salvage Proposal and now that Salvage as a whole has changed in terms of its issues and strengths. As a result I feel the original document is outdated and it would be beneficial for a new document to be written with context and hindsight in mind.

## Background

[Mirrorcult's original salvage proposal](https://hackmd.io/@mirrorcult/salbidge)
[Emogarbage's salvage proposal](../proposals/salvage-proposal.md)

To quote the previous proposal: "Salvage right now is in a bit of a weird spot."
Salvage has some of the most content of any department with a genuine gameplay loop and lots to do, arguably more to do than you can reasonably fit into a shift.
Looking at it from a pure quantity perspective, Salvage is doing very well in terms of content. 

However, while the ocean of content for salvage is wide much of it lacks depth and salvage is not given the proper tools to fully explore this ocean. 
In addition, salvage has a lot of undesirable behavior that has only been worsened with some of the moves towards the original design doc. Salvage still very often doesn't mine and focuses on gamer loot instead, and now they will often times abandon their jobs entirely to build shittles leading to a whole new slew of probems. 
Salvage is maligned by many because of this, and for good reason. They spend a good portion of the shift, completely alone disconnected from even their own salvagers, deconstructing escape pods and breaking into engineering to build a shuttle just so they can interact with the crew even less. This also leads to a lot of new salvagers just not getting taught how to do their jobs. It can be worse than engineering in that regard.

Much like the original design document much of this proposal aims towards tying salvage's many systems together with tweaks and balancing over new features. Although new features are definitely needed in some places.

## Features to be added

The most important thing that needs to change is progression. Right now the VGRoid and Expeds are in a weird spot since either hard or soft limitations prevent salvagers from ever getting to them naturally. 
The roid is very far away and salvagers are limited by their inventories such that it's always better to use the magnet, unless they have a shuttle. And expeds, require FTL to reach meaning they need a shuttle. 

There are two extremes you can lean in to solve this issue, bring back the reclaimer or kill the shuttle. I lean heavily towards the latter. Shuttles in the current state of the game are not robust enough and lack content around them to make them interesting. They also take way too many resource and way too long to build to expect salvage to do them as a part of their already busy job even ignoring that you'll need to know engineering better than some station engineers to build them. 

This means that in their place there need to be systems to make up for the strengths of the shuttle: navigation, inventory, and modularity. 

### Navigation
For Navigation, the mass scanner exists but it's not enough. A big strength of the shuttle is you can see it on a mass scanner, meaning you know where your salvage buddies currently are and usually what they're doing just by looking at a map. With the death of the shittle I propose a buff to the GPS in return. 

#### Changes to the GPS
- The GPS should be given a UI that displays GPS signals in a circle around you with a distance to them, or in a big list with coordinates (really depends on how much we want salvage to suffer)
- GPSs should emit GPS signals when turned on, the Astronav should emit these signals too
- GPSs should be able to be named, if they do not have a name they should show up as a dot without a name to avoid clutter
- The Station and Cargo Shuttle should emit GPS signals with appropriate names by default
- All other GPSs should be off by default, including the Astronav
- GPS signals shoud be visible on Mass Scanners with the ability to hide them if needed
- Salvage should be given a GPS beacon, that emits a GPS signal when placed down and powered
- Handhed GPSs should be battery operated like the mass scanner but with a much better battery life

The GPS should be a reliable, albiet non-ideal, way of navigating through space near the station as well as a communication tool for salvagers. Currently the GPS displays coordinates and nothing else. It's basically useless for anything except returning to the station or finding your way to the ship on an exped.

Adding visible signals does a few things, first it allows salvagers to mark locations of importance for them to return to. Such as being able to mark down a room on the Roid with loot, place down a GPS in space where a locker full of goodies is, and most importantly know where their salvage buddies are (if they have their GPS on). The latter is the most important as salvagers without the reclaimer often act independently and trying to rendevous can be a complete genuinely impossible especially if one dies alone in a hole somewhere. This also means that salvagers are less likely to get slammed into by the cargo shuttle because they're completely invisible on the mass scanner which is a bonus.

Additionally, nukies and other ship using antagonists can now avoid salvagers running into them, since they can see where they are. And of course, salvagers can turn their GPSs off to hide their signal if they need to be stealthy when fighting these threats.

This also gives salvagers a way to navigate to the VGRoid in the event they get unlucky with mass scanners, or science explodes too many times, by placing down a GPS beacon with an RTG generator next to it. Or perhaps some kind of new "mini generator" that connects to LV cables like a welding fuel generator, but with far less power output. 

#### Jetpacks

Contuining with Navigation, Salvage actually needs a way to get to the VGRoid as well as derelict debris scattered throughout space. Currently Salvagers use mini-jetpacks, typically filled with liquid oxygen. This works well for their job however there is one thing I would change and it doesn't involve mini-jetpacks. 

Void Jetpacks are the best salvage loot in the game hands down. If there is a derelict that has a guaranteed spawn it is genuinely worth dropping everything to go and get it before someone else does. This isn't a major issue because Salvage should have good jetpacks and I wouldn't want the void jetpack removed. 
Rather, I would make it a necessity that any debris that spawns with a void jetpack should have a genuine danger preventing you from just walking in and taking it. Perhaps include a couple VGRoid spawns, or a Syndicate simplemob with a viper, or something to add any amount of risk to just rushing one.
Additionally, the Void Jetpack should be added to the VGRoid loot pool, it's dangerous enough to justify it spawning very rarely. And since you'll already have a jetpack by the time you get there so the other jetpack spawns are functionally worthless.

That aside, salvagers using jetpacks to get to the Roid and eventually upgrading to liquid oxygen is fine as is. No changes necessary on the jetpack side. The only issue I've seen is the inconsistencies with VGRoid distance to station.

In the case where liquid oxygen damages salvagers though, either jetpacks will need larger capacities, or jetpack tanks will need to be split into two tanks, that way you can wear a jetpack that has one air tank and one fuel tank.

#### Gateway/Dropship

Giving salvage a shuttle is a bad idea and trying to get them to build a shuttle has ended catostrophically. Salvage needs to progress towards a better form of transportation that allows them to more easily get to the far off places they need to go, but also allows other people to go there as well.

A station gateway or dropship (former is easier to implement but I think the latter has more flavor) is a tried and true solution to this problem. Having a stationary "teleporter" that can bring salvage to their destination provided they have the right FTL coordinates is the best solution.

For progression this would put a dropship/gate in salvage and/or in a public place on the station (so anyone can in theory use it) which at round start wouldn't have any destinations available to teleport to.

On the Roid, Salvage can turn on an FTL beacon/gateway somewhere by a dungeon generated dock which allows easy traversal between the roid and the station. This beacon/gateway should be turned off by default and require a little bit of engineering knowledge to set up. It should also be guarded by guaranteed monster spawns of some sort to ensure that if salvage wants to rush it roundstart they have difficulties doing so. 

### Inventory
This is the big one. There's not really a point to going to places with more loot if you can't carry that loot back anyways. Especially if those places are significantly more dangerous.
The jump from carps to Goliaths is big and doesn't really matter a whole lot when a debris will fill an entire locker anyways. Same goes from literally nothing to Goliaths when mining, if your ore bag is going to be full.

On the inverse, getting stuff to you is harder as well. A big benefit of a shuttle is you can stuff all the meds, and lathes, and everything on it you want. If Salvage is going to ditch the shuttle entirely, they will need a way to carry more meds and ammo and other things in a way that doesn't horribly break game balance like a shuttle does. 

Having played with fultons being craftable and researchable, I don't think they are fully the solution we need. Fultons are great once you get there, but getting there is a pain is the issue. Which is why I think most inventory problems have to be addressed as transportation problems. 

If salvage can extend their inventory by storing stuff in a physical location, like on the station, and the station isn't unreasonably far away, the problem is solved.

### THE ROID
The VGRoid should be the mid to endgame for salvage. At least half of their time per shift should be dedicated to either being on the roid, preparing for the roid, coming back from the roid or explaining to QM that the other salvagers died on the roid and you need 40,000 spesos to save them.

The Roid has a very strong interconnected gameplay loop with only a few issues that need to be addressed.

#### Enemy Variety
The Roid's enemy variety is pretty bad and should be increased. This one is tricky because enemies on the Roid should serve a number of functions.

1. Danger!!! They should make the roid dangerous, there's no reward without risk

2. Useful!!! They should all drop something useful to a salvager (Hivelord remains, Goliath Plates, Some other third thing cause there's only TWO enemies)

3. Interesting!!! Each monster should fit the roid's asthetic of creepy, scary, alien, they should also be fun to fight and have a unqiue gimmick to them. (Hivelords rush you and can pile up if you don't deal with their spawn, Goliaths you have to strafe and try not to get tripped up).

4. Fair!!! Putting this down because the monsters should feel fair. This doesn't mean they should be weak, or easy, but if a monster has a big attack that can ruin your day it should be telegraphed. There shouldn't be any moments where you die to an enemy doing something the game did not communicate to you. 

Any new enemies should meet these standards and there should be at least a few.

#### Discs!!!

Discs or Coordinate disks are rare finds on the VGRoid which are incredibly valuable to sell, but far more valuable to use. These discs contain the coordinates to a rare and probably dangerous lost section of space that your quartermaster would be very interested in you going to. These discs should be the only source to some rare forms of gamer loot, but that should never be the focus of them. They should always reward something that is useful to the station as well such that if you don't grab it QM will tattle to HoS about all your contraband.

##### Magnet Discs!!!

Magnet discs are rare disks which pull in unique timed magnet pulls. These pulls can be hand crafted in the same way ruins currently are, but with far less restrictions on danger and loot. 
As well these can be used to facillitate boss fights, especially space boss fights of which our physics engine uniquely allows us to make very epic (if AI can ever pathfind through space that is)

##### Expeds!!!

This is the best solution I could find for expeds. Expeds should be made a roid only loot item in the form of coordinate disks. These disks when inserted into a shuttle or dropship/gateway console will allow salvagers to access a time-limited mission on another planet. 

Mission is the key word, expeds should have a mission modifier applied to them that either adds a goal or a trouble.

A goal would be something like: There is a nuclear bomb on this exped that is going to detonate, if you can find it and disarm it within 5 minutes you will get some sort of prize! Salvage has a clear goal and objective with a reward at the end.

A trouble is more open form but no less difficult and would be something like: There is a dungeon, grab as much loot as you can but be warned, there is a boss in the area who will spawn after X minutes, if you kill them you'll get some extra rewards too! Or there is a dungeon, every minute enemies will spawn outside until you are swarmed, grab as much stuff as you can and get out before you get overwhelmed.

Regardless of mission type all expeds should have hard time limits, where the gate is forced to close or dropship is forced to leave and flavor wise, there should be an in lore reason why you don't just stay on the planet and never return to NT (place is overwhelmed with monsters, NT is moving in to take control of the dungeon, something something unwinnable battle rocks fall).

#### Communication!!!!

The Roid needs to be better communicated to the player.

A lot of salvagers, literally don't even know the roid exists. Nor that it has dungeons on it, nor that it's really fun.

A big piece of the blame comes to it's spawning. It spawns way too far away, sometimes it's 2000 meters away not even close to being on the mass scanner and taking genuine minutes to fly to.

In addition to the magnet having basically everything you need aside from diamonds it's very easy to see why many salvagers just stick to the magnet. It's very easy to just never learn the roid exists and even if you do learn, it may often just be so far out of the way it's not even worth trying to go to. 

Roid needs to consistently spawn closer to the station, simple as. 

### MAGNETS!!!

Fucking mangets, how do they work?

The magnet is not great. It's too good of an all rounder for everything meaning many salvagers just use the magnet exclusively and never move on from it. It's also extremely random, sometimes you get woefully unlucky and never roll gold on asteroids all shift, although that kind of bad luck is never common enough for you to stop using the magnet.

The magnet should be refactored into a early game jumping off point, a place where you do a few pulls, get your gear, get some basic materials for the station and then move on to bigger and better things. 

For this I advocate for a big change, the magnet should only be able to pull debris roundstart.

Now this sounds like a big nerf to the magnet, because it is, but it needs to be balanced out with other changes and a minor buff to the magnet as well for it to work.

#### Space Debris

Space needs to have asteroids and debris floating in it. Once salvage needs/wants gamer loot and ore they should be forced to explore. Go to the roid, check out some of those funny lumps near the station, the baby bird must leave their nest eventually. This would be a dumping ground for most of the magnet content that currently exists and would need a new home. 

For the rest of that content we need something more robust.

#### Space Scanner

A new Science computer that allows you to play a minigame to generate a bit of research points (If you've played Goonstation you know exactly what I'm talking about).

But as an additional reward you can find and upload coordinates to Salvage's magnet (or telesci if we ever get that but that's another design doc) to give them more options!

Over time this means salvage's magnet will gain access to more pulls which will be more consistent, need gold and your team is inbetween roid runs? Check the magnet and see if science found an asteroid with gold! Salvage not mining as usual? Find the asteroid with the materials you want and do their job for them! This also integrates science deeper into salvage and salvage deeper into science. Now if a salvage wants to never mine and just pull medium wrecks all shift in hope of contra-maxxing, they have to ask science to help them do it.

Science could also find wrecks of their interest which could facillitate their research. Perhaps a wreck is the ruins of an old lost space station which was rumored to have discovered how to cook a donk pocket in less than 30 seconds! Only the brave salvagers can go into this deserted wreck and bring home the antique microwave for science to tear apart for research.

However, looking at this computer through the lens of just giving more magnet pulls is a limiting perspective. If you're scanning all of space, who knows what you can find, this computer could be used as a jumping off point for starting space based Events, calling in terrors as an antag, getting vague and cool lore, or interesting roleplaying opportunities. And of course, it could be used as a jumping off point for someone to make a proper telescience department. 

Give a description of what game mechanics you would like to add or change. This should be a general overview, with enough details on critical design points that someone can directly implement the feature from this design document. Exact numbers for game balance however are not necessary, as these can be adjusted later either during development or after it has been implemented, but mention *what* will have to be balanced and what needs to be considered when doing so.

## Game Design Rationale

Overall, the design of this document is meant to make salvage a deeper, riskier, and more enganging experience to play that rewards you for doing your job you slacker. 

Game design wise, I tried to balance around both salvage working as a team, but also still being possible for a lone salvager, that way an antagonist salvager, the only non-antag salvager, a low-pop salvagr, or a salvager who lost their whole team to a bottomless pit accident, can still do their job reasonably well but with a greater risk. I think salvage should be able to do their job alone, but it shouldn't be the default.

GPS changes specifically are meant to be similar to suit coordinates, but more geared towards space adventurers. Much like suit coordinates, there is plausible deniability in them being off with the added functionality of being able to "fake" them by dropping a GPS signal somewhere with your name to pretend you're on the VGRoid, when you're actually stealing RD's hardsuit. 

Proposed changes to the Void Jetpack, make the arguably best loot in the game still obtainable but there is now an actual risk when trying to get it. 

The changes to the magnet are meant to force salvagers to experience a bit more danger while also letting someone take it slow and steady if they're willing to wait around a bit. Plus they can just explore space rocks instead of going to the roid if it's too difficult.

The Space Scanner is meant to add depth to space and tie in salvage closer to the station and science in general.

Consider addressing:
- How does the feature align with our [Core Design Principles](../space-station-14/core-design/design-principles.md) and game philosphy?
- What makes this feature enjoyable or rewarding for players?
- Does it introduce meaningful choices, risk vs. reward, or new strategies?
- How does it enhance player cooperation, competition, or emergent gameplay?
- If the feature is a new antagonist, how does it fit into the corresponding [design pillars](../space-station-14/round-flow/antagonists.md)?

## Roundflow & Player interaction

TODO

Consider addressing:
- At what point in the round does the feature come into play? Does it happen every round? How does it affect the round pace?
- How do you wish for players to interact with your feature and how should they not interact with it? How is this mechanically enforced?
- Which department will interact with the feature? How does the feature fit into the [design document](../space-station-14/departments.md) for that department?

## Administrative & Server Rule Impact (if applicable)

TODO

- Does this feature introduce any new rule enforcement challenges or additional workload for admins?
- Could this feature increase the likelihood of griefing, rule-breaking, or player disputes?
- How are the rules enforced mechanically by way the feature will be implemented?

# Technical Considerations

TODO

There's a lot of technical considerations in this proposal, particularly with the new proposed science computer which will require a new UI, a new minigame, and definitely a number of new components and systems for sending pulls to the station's magnet.

The GPS requiring a new UI as well, and having to add GPS signals to the mass scanner interface is both a technical challenge as well.

Same goes for the gateway/dropship. A lot of it can be done with stuff we already have, but there will need to be an extra layer of polishing and tweaking before it's done.

- Are there any anticipated performance impacts?
- Does the feature require new systems, UI elements, or refactors of existing ones?
- For required UI elements, give a short description or a mockup of how they should look like (for example a radial menu, actions & alerts, navmaps, or other window types)
