# Burnt Disk/KOTH Nukies (An Optional and Alternative Nukies Gamemode)

| Designers | Coders | Implemented | GitHub Links |
|---|---|---|---|
| Princess Cheeseballs | Princess Cheeseballs | :x: No | TBD |

## Overview

Burnt Disk nukies is intended to be an alternative opt-in game type as part of the Nuclear Operatives game mode, similar to war ops. 
It is intended to replace the current "random bomb" design in the current NukeOps gamemode, replacing it with something that makes rounds more interesting and allows for more unqiue nuke-ops plans.

## Background

Nukies is a gamemode that is currently fairly solid with only a couple of holes. 
Those holes tend to revolve around round stalling and predictability.
For example, a common issue with current Nukies is that the Nuclear Operative's may get the codes to their own nuke, then lose that nuke causing the round to stall.
War Ops in particular has this issue crop up often, with crew sometimes hiding the disk in trapped rooms, hiding the station nuke itself, or covering the station with annoying to navigate mazes.

On top of that, the nuke codes currently choose a random nuclear bomb, making complex planning a crapshoot or otherwise not possible. 
Say you want to ransom the station with a ton of explosives? Or a singularity? Gonna be tough if you need the station's nuke.
Want to do stealth ops and try and sneak in? Better hope it's not your nuke. 

Thinking of unique and interesting plans to try for Nukeops isn't worth it if those plans require one specific nuke to work (trust me I've tried) because you can just get screwed over by RNG. 

## Features to be added

This proposal makes a two major changes to the current nuke ops gamemode.
1. Nuke codes work for all Nuclear Bombs. Instead nuke codes are now tied to disks. So long as you have the right disk and a bomb the bomb will arm. 
2. Instead of getting random codes, the nukies get the choice of getting codes for the station's disk or a burnt disk. (Or it could be random :P idk point is that it's not the same every round)

These two changes are the bread of Burnt Disk Nukies, changing the way the start of NukeOps plays out to allow for a better planning phase.
The goal the nukies have to achieve is clear, kill the captain get the disk or find a spot to arm and hunker down, and how they achieve it is all they have to worry about.

To make the gamemode work however, it requires some more under the hood changes.
Firstly a prototype for a nuke disk which has an extended arm time (already possible) but isn't able to be armed off station or microwaved (requires some additional coding) to avoid cheesing the extended timer.

Secondly, a big part of Burnt Disk Nukies is auto-ERT. This has been a widely suggested feature for nuke-ops to light a flame under the nukies to prevent them from stalling, but it's integral to the balance of KOTH Nukies. 
The big technical challenge of Auto ERT is mostly with shuttle spawning. (Although we might be able to get away with spawning one additional shuttle if it's purely for a specific gamemode since we're already spawning a whole ass map and shuttle anyways...)

## Game Design Rationale

The idea behind KOTH Nukies is to add some additional spice and uncertainty to Nukie rounds.

The issue with tg Nukies is that it's predictable, everyone knows how the round is going to play out so if you know it's coming you can plan around it.

Burnt Disk Nukies operates differently by design. 
Loosely based on goonstation nukies (where they can arm their nuke at any time or choose to go after the captain's disk to reduce arm time) KOTH Nukies aims to flip the gamemode on its head to reduce predictability.

Rather than Nukies taking an offensive role, they take a more defensive role making some strategies better and other worse. 
Given the lack of needing to extend into the station to get the disk, and more defensive role, Nukies are generally benefited from this change so to offset it they are given a number of downsides attached to using the burnt disk: 
- The bomb takes much longer to arm. 5-10 additional minutes (Been testing with 10 additional but I could see an argument for dropping it down to at minimum 5).
- After 5 mins an ERT shuttle with a full ERT team spawns (1 Leader, 1 Medic, 3 Sec with gear and ammo, although this should be adjusted for pop!)

Ideally choosing the Burnt Disk should decrease your odds of success, (same way War Ops should) but in exchange you have more fun. 

The longer timer and additional firepower means that Nukies are going to be significantly more strained in terms of resources which will change how they approach arming.
Maybe it's worth pushing into sci to get a lathe to emag? Maybe you should spend TC on borgs instead of guns? Maybe it's worth getting jug suits since you're going to be stationary?
Sure you've been given a disk but now you have a lot more problems you're going to need to solve! Good planning and resource management becomes crucial. 
