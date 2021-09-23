---
title: Enemies
order: 5
---

Enemies will be the main threat to the player as they approach from all directions. There are different enemy types that will require different ways to kill them.

### Enemy Types

- Grey
- Red/Blue
- Purple
- Yellow/Green

#### Grey

The grey is the most common enemy the player will encounter. Grey enemies can be killed with any bullet

### Spawning

An enemy spawns in one of 8 lanes around the player. Multiple enemies can spawn at once, called a _Spawn Instance_, and enemies in the spawn instance can be of any type. The time between spawn instances will be random and the lanes the enemies spawn in will also be random. The spawn time also increases and decreases depending on the _Global Game Speed Modifier_. E.g. If the game slows down due to a skill effect or other effect, the time between spawn instances will be longer and vice versa.

### Spawn Instance

A _Spawn Instance_ are a group of enemies that spawn at the same time. These enemies are grouped via the time they spawned and not the lane they spawned in. Each enemy within the Spawn Instance will be in a different lane. Enemies within the same lane **cannot** be in the same spawn instance.
