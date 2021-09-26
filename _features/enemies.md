---
title: Enemies
order: 5
---

Enemies will be the main threat to the player as they approach from all directions. There are different enemy types that will require different ways to kill them. Enemies only require one shot to be killed provided that they are killed correctly. Enemies all move at the same pace.

### Enemy Types

- Grey
- Red/Blue
- Purple
- Yellow/Green

#### Grey

The grey is the most common enemy the player will encounter. Grey enemies can be killed with any bullet.

#### Red/Blue

Red and Blue enemies are a level above grey enemies in that they require one shot to kill but also require the correct gun to kill them. Red enemies with the red gun, blue enemies with the blue gun. _Purple Bullets_ still follow the same rule as previously stated where purple bullets shot from a red gun count as red bullets and purple bullets shot from the blue gun count as blue bullets.

#### Purple

Purple enemies can only be killed with purple bullets shot when both guns are pointed down the same lane. This is to force the player to sync both joysticks in the same direction which will require a little more coordination.

#### Yellow/Green

Yellow and green enemies can be killed with any bullet (Red, Blue, Purple), however, once killed they rotate their _Spawn Instance_, either clockwise when a green enemy is killed or anti-clockwise when a yellow enemy is killed. the rotation of the _Spawn Instance_ should happen almost instantly - synced with _Hit Stop_ time. If there are no enemies left on the same _Spawn Instance_ as these types of enemies, then there will be no rotation.

### Spawning

An enemy spawns in one of 8 lanes around the player. Multiple enemies can spawn at once, called a _Spawn Instance_, and enemies in the spawn instance can be of any type. The time between spawn instances will be random and the lanes the enemies spawn in will also be random. The spawn time also increases and decreases depending on the _Global Game Speed Modifier_. E.g. If the game slows down due to a skill effect or other effect, the time between spawn instances will be longer and vice versa.

### Spawn Instance

A _Spawn Instance_ are a group of enemies that spawn at the same time. These enemies are grouped via the time they spawned and not the lane they spawned in. Each enemy within the Spawn Instance will be in a different lane. Enemies within the same lane **cannot** be in the same spawn instance.
