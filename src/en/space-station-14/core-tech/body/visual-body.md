# Visual Body Component

A.K.A building a sprite out of organs!

## Top-Level Overview

Most entities a player interacts with have a sprite, defined by its sprite component. 

These sprites can either be coded directly in YAML or be dependent on other entities or components.

An entity with the VisualBodyComponent, designates that much of its sprite is determined by its organs.

For most species, this means that their "body sprite" is actually a bunch of sprites from their organs added to them as layers.

As with BodySystem, there is no distinction between "internal" and "external" organs for the purposes of sprite layering.

```admonish note "Example"
- This entity is a human by technicality, but its organs are from a variety of different species.
- These changes to its organs are reflected in its sprite.
- Changes to the character's skin color through zombification are applied to its organs.
```

![visualized body](../../../assets/images/medical/peak-performance.png)

## How does Visual Body Component work?

As with BodySystem, i