# Solutions Rewrite (DRAFT 1)

| Designers | Implemented | GitHub Links |
|---|---|---|
| Princess Cheeseballs | :x: No | TBD |

## Overview

This design doc purely focuses on solutions and not the reagents stored inside them, aiming to design a comprehensive and modular model of how solutions should work. 

## Background

Solutions, currently, are entities spawned by an entity with the SolutionContainerManangerComponent inside of a container. These entities have a SolutionComponent which stores a Solution class which has all the reagent, heat, and volume data we care about.  

Solutions are usually handled by the SolutionContainerManagerComponent and attached system, Components which modify solutions are attached to the entity with the SolutionContainerManagerComponent and not the solution entity itself.

This means that solutions are an entity, stored inside of a container, attached to another entity that does all the logic for handling them, and are effectively treated as a dictionary of solutions. 

This is an extremely inefficient and rigid system which needs to change, either by turning SolutionContainers back into dictionaries, or giving a reason for solutions to exist as entities. This proposal aims for the latter.

Solutions should be able to have unique properties, both intrinsically and also reactively to the reagents inside of them. In additon we also need to account for the fact that many different entities may need many different unique solutions or ways to store them.

As an example, plushies are a solution that contains fiber, but they can also absorb liquids. This creates conflict when you try to eat the plushie since most solution based APIs only account for one solution existing on an entity, ever. This means you have to choose between eating the plushie, and sucking the liquid out of it and cannot do both at the same time or switch between them. 

It also heavily restricts what you can do with an entity such as this, as an example imagine we wanted to have a machine which has two reagent tanks that are separate. We want both of them to generate some solution every second so long as there is power. 

The components for this exist, but ONLY if we have one solution since they're attached to the machine itself and you have to choose one solution. You would have to create an entirely new component and system just to allow for this specific behavior on this specific machine. This is not very good ECS design, and if you try and do anything creative or generic with solutions this limitation will always cause problems eventually. 

In addition much of the component selection is not great, they are trying to be too generic since instead of using an event based approach for doing behavior it's often done through: 
```
if (HasComp<Comp1>(ent1) && HasComp<Comp2>(ent2))
  do the thing
```

## Goals

The goal of a solution rewrite would be to leverage the strengths of containers and ECS to allow for entities to have multiple interesting and unique solutions stored within them that wouldn't be possible with the previous system. 

Solutions also need to be made event based in some capacity so we don't have to rely on generic supercomponents that try to handle more than they have to. 

In addition many entities that currently exist now should be able to be made in such a way that they make more sense from a interaction standpoint. I.E if I eat a plushie full of poison, I should be consuming the poison too instead of it getting deleted. 

## The How

For starters, Solutions need to be made into proper prototyped entities. This means that entities which have solutions need to be able to create solutions from prototypes on MapInit that are not *just* an entity with a single extra component attached. 

Solution modifying components normally attached to the parent entity will need to be moved down to the solution i.e: RegeneratingSolutionComponent, DumpableSolution, DrainableSolution, SpillableSolution ect.

From there Solutions need to be rethought and redfined. Currently, a SolutionContainerManager holding a solution represents both a complex machine that has multiple different solutions and places they store solutions, a beaker which has one area to store solutions, and a pizza which doesn't really store solutions as much as it is made of solutions. 

This requires making a number of new components on the solution entity itself to define what *type* of a solution it is. If I eat the parent entity, will this get eaten too? If I destroy the parent entity is this destroyed too? Is the parent entity limiting my capacity? Should my max volume change as I'm drained? Can I be removed from my parent entity and placed into another parent entity? 

There's a lot of questions we need to be able to ask and answer with solutions and the best way to do this is through more components. This requires restructing the SolutionContainerManager to be a relay component which relays events and calls to the solutions it is managing. 

Lastly, we can take advantage of the fact solutions exist in containers. It's not called a "SolutionContainerManager" for no reason. This enables a lot of fun and complex behavior if we leverage it, for example: *Why does a SolutionContainer only need to store one solution?*

It doesn't (so long as we don't store a ton of em in a single container as that would have performance concerns) and removing that limitation by allowing solutions to be inserted into solution containers allows for a lot of new and interesting behavior. For example, it allows solutions to be added to containers without replacing the solutions inside. This means a beaker can contain *multiple* solutions, in the same singular container. 

With the current way reagents and solutions work this would have no benefit, but if solutions can exist as physical objects such as, an ice cube, a sheet of steel, or a plushie, you could then have it so beakers can store these items directly and manage the volume at the parent level rather than per solution. This requires removing max volume from the Solution class and componentizing it, but I believe that is fine and allows for better ECS design. 

All this together would redefine solutions as an entity that is made of reagents, and has a SolutionComponent to define which reagents are stored. Everything else can and should be split off into Components to leverage ECS with solutions and allow entities that *are* solutions to exist outisde of a SolutionContainer. 

Solution Containers then properly manage solutions by being a container which imposes limitations or alters solutions inside of it, rather than being a way to hold a reference to an entity. 
