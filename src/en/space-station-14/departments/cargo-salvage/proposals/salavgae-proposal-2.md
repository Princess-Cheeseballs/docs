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
- The GPS should be given a UI that displays GPS signals in a circle around you with a distance to them, or in a big list with coordinates (undecided on which I prefer)
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

Contuining with Navigation, Salvage actually needs a way to get to the VGRoid as well as derelict debris scattered throughout space. Currently Salvagers use mini-jetpacks, typically filled with liquid oxygen. This works well for their job however there is one thing I would change and it doesn't involve mini-jetpacks. 
Void Jetpacks are the best salvage loot in the game hands down. If there is a derelict that has a guaranteed spawn it is genuinely worth dropping everything to go and get it before someone else does. This isn't a major issue because Salvage should have good jetpacks and I wouldn't want the void jetpack removed. 
Rather, I would make it a necessity that any debris that spawns with a void jetpack should have a genuine danger preventing you from just walking in and taking it. Perhaps include a couple VGRoid spawns, or a Syndicate simplemob with a viper, or something to make it a genuine risk to rush without a team or without being prepared.
Additionally, the Void Jetpack should be added to the VGRoid loot pool, it's dangerous enough to justify it spawning very rarely. And you'll already have a jetpack by the time you get there so the other jetpack spawns are functionally worthless.
That aside, salvagers using jetpacks to get to the Roid and eventually upgrading to liquid oxygen is fine as is. No changes necessary. The jetpack in its current state, including the bug that lets you go faster by tapping keys perpendicular to your movement, works very well.

### Inventory
This is the big one. There's not really a point to going to places with more loot if you can't carry that loot back anyways. Especially if those places are significantly more dangerous.
The jump from carps to Goliaths is big and doesn't really matter a whole lot when a debris will fill an entire locker anyways. Same goes from literally nothing to Goliaths when mining, if your ore bag is going to be full.

On the inverse, getting stuff to you is harder as well. A big benefit of a shuttle is you can stuff all the meds, and lathes, and everything on it you want. If Salvage is going to ditch the shuttle entirely, they will need a way to carry more meds and ammo and other things in a way that doesn't horribly break game balance like a shuttle does. 

// Continue from here...

Give a description of what game mechanics you would like to add or change. This should be a general overview, with enough details on critical design points that someone can directly implement the feature from this design document. Exact numbers for game balance however are not necessary, as these can be adjusted later either during development or after it has been implemented, but mention *what* will have to be balanced and what needs to be considered when doing so.

## Game Design Rationale

Overall, the design of this document is meant to make salvage a deeper, riskier, and more enganging experience to play that rewards you for doing your job you slacker. 

Game design wise, I tried to balance around both salvage working as a team, but also still being possible for a lone salvager, that way an antagonist salvager, the only non-antag salvager, a low-pop salvagr, or a salvager who lost their whole team to a bottomless pit accident, can still do their job reasonably well but with a greater risk. I think salvage should be able to do their job alone, but it shouldn't be the default.

GPS changes specifically are meant to be similar to suit coordinates, but more geared towards space adventurers. Much like suit coordinates, there is plausible deniability in them being off with the added functionality of being able to "fake" them by dropping a GPS signal somewhere with your name to pretend you're on the VGRoid, when you're actually stealing RD's hardsuit. 

Proposed changes to the Void Jetpack, make the arguably best loot in the game still obtainable but there is now an actual risk when trying to get it. 

Consider addressing:
- How does the feature align with our [Core Design Principles](../space-station-14/core-design/design-principles.md) and game philosphy?
- What makes this feature enjoyable or rewarding for players?
- Does it introduce meaningful choices, risk vs. reward, or new strategies?
- How does it enhance player cooperation, competition, or emergent gameplay?
- If the feature is a new antagonist, how does it fit into the corresponding [design pillars](../space-station-14/round-flow/antagonists.md)?

## Roundflow & Player interaction

Consider addressing:
- At what point in the round does the feature come into play? Does it happen every round? How does it affect the round pace?
- How do you wish for players to interact with your feature and how should they not interact with it? How is this mechanically enforced?
- Which department will interact with the feature? How does the feature fit into the [design document](../space-station-14/departments.md) for that department?

## Administrative & Server Rule Impact (if applicable)

- Does this feature introduce any new rule enforcement challenges or additional workload for admins?
- Could this feature increase the likelihood of griefing, rule-breaking, or player disputes?
- How are the rules enforced mechanically by way the feature will be implemented?

# Technical Considerations

- Are there any anticipated performance impacts?
- Does the feature require new systems, UI elements, or refactors of existing ones?
- For required UI elements, give a short description or a mockup of how they should look like (for example a radial menu, actions & alerts, navmaps, or other window types)
