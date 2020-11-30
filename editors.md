---
layout: default
title: "Editors"
---

## Spawn Instance Editor

### Spawn Instance Patterns

<hr class="my-5">

## Level Editor

The level editor determines what Spawn Instance Patterns are used in each level. Depending on the **Level Type** (See below), a single level consists of two phases split at the half-way mark of each level type.

### Level Types

Each level type has a goal the player has to meet in order to complete the level

- Survival - The Player has to kill X **amount of enemies**
- Timed - The Player has to survive for X **amount of time**
- Multi-round - The Player will need to survive multiple short **Survival** rounds that progressively get faster after each round. The lives get reset each round.
- Perfection - The Player will play either a **Survival** or **Timed** where they are not allowed to miss a shot.
- Endless - The Player will go on until they **run out of lives**.

#### Level Type Phases

Levels will have two phases to change up the pace and keep the player on their toes. Each Level Type will have different points in the level that will exhibit the new level changes.

- Survival - Half of the enemies have been eliminated.
- Timed - Half of the time has passed.
- Multi-round - None. The level type will not have any phases.
- Perfection - Half of the enemies have been elminated (Survival) **OR** Half of the time has passed (Timed).
- Endless - None. The level will progressively get harder the longer the Player stays alive. _More Info Needed_
