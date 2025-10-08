# Metabolism Refactor [DESIGN DOC DRAFT]
This is a design doc for a metabolism refactor, it is a lot more technical in implementation since it is primarily meant to organize a number of things desired from the refactor into a sensible atomizable system such that mutliple people can work on it.
Do not expect this to be a beginner friendly document.

## Kill Metabolism Groups
This goes at the top of the list because there is consensus among those who work with BodySystem that MetabolismGroups are the worst.
Extremely buggy, extremely specific, and required for every single metabolizer they offer basically no benefits and only create problems.
Metabolism Groups section off different effects to different metabolisms, but they don't play nice with eachother and use broad labels like "Toxins" "Medicine" which are extremely subjective per species.
It results in a system where each reagent can only have one metabolism group to work properly, and at that point what is even the point of MetabolismGroups?
If you wanted to have a species that didn't metabolize a certain group it wouldn't work, or would require an extreme amount of combing through every reagent to make it work with a ton of copypasting of effects.
YEARS of MetabolismGroups and yet nearly every effect still checks for species type anyways. It just needs to go. 

## Replacing Metabolism Groups
[TODO] Moony mentioned something about a way to have certain effects be generated per organ which is what we want, but I forgor.
We need a sensible way for organs and species to pick and choose effects without a ton of copypasting. I need to go back and reread what was discussed cause my memory is hazy on that.

## ECS Metabolism
Right now metabolism is handled by the MetabolizerComponent which metabolizes reagents.
This is not great. For one it's extremely rigid in its behavior in that it can only metabolize reagents, and for two, it means it's a self contained system which it fundementally cannot be. Metabolism relied on entityeffects being tied so closely to it that it would relay effects and conditions to organs for it, which is not good behavior. 

### New Components

Instead we need to split these components apart a bit. Metabolizer should be a generic component that is used for entityqueries for metabolism, while the processing should be event based and given to distinct "MetabolizerType" components for things such as "ReagentMetabolizer" and "GasMetabolizer." It being event based means it's easily expandible in case we ever wanted to add something like a "RadiationMetabolizer" but that's getting ahead of ourselves, we only care about two types right now.

Next, metabolizers should need a body of some sort to metabolize in. Either way say "This is BodyComponent" and force BodyComponent on anything which we want to be able to Metabolize, or we add another component which marks an entity as able to Metabolize. 

This Component should store information similar to the MetabolizerComponent in terms of what it can/cannot metabolize. And disagreements between organs and body should be handled in interesting ways if possible. For example, vox lungs in a human body would disagree on how they metabolize oxygen, possibly resulting in both poison and oxygenation applying, or neither applying. 

### Metabolism Structure

Metabolizers should ask their components to do their metabolizing by passing them arguments on what they can/cannot metabolize and what effects are/aren't valid. 

In return these components should return effects which are to be applied to the body above, with any organ specific checks and effects being applied during the metabolic process (i.e. if an effect sets your liver on fire, it happens during the metabolizing process, even if the effect can't apply to your body...)

Having Metabolizers be self contained component systems also gives us the freedom to tweak how organs metabolize things a lot more easily, since metabolizer system effectively becomes a "Hey can I have some effects to apply to the body" system.

#### Reactive 

Smaller data-point but the reagent-effect args can be restructed to be more generic and be used by reactive as well. It should be able to just:

- Take a reagent input
- Consume x of that reagent input (probably best done at organ level not struct level?)
- Optionally spit out a reagent output
- Check reagent/solution specific conditions
- Apply effects

We also would want one of these for gasses, but we ABSOLUTELY DO NOT WANT REACTIVE GASSES due to performance reasons (unless Atmos fellas say it's okay but that's not something we should concern ourselves with, something something microbalance)
