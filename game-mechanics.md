---
layout: default
title: "Game Elements and Mechanics"
---

## Dual Aiming

The character is controlled with both sticks of a controller (Keyboard controls still are still being revised). Each stick corresponds with a gun: Left = Blue, Right = Red. The character can aim each gun in 1 of 8 directions (0, 45, 90, 135, 180, 225, 270, 315 degrees) and can overlap on the same angle. The character will continue to aim down their last angle if they reset the control stick to a neutral position.

<div class="row mb-4">
  <div class="col-md-4"><img src="https://via.placeholder.com/400x300" class="img-fluid"></div>
  <div class="col-md-4"><img src="https://via.placeholder.com/400x300" class="img-fluid"></div>
  <div class="col-md-4"><img src="https://via.placeholder.com/400x300" class="img-fluid"></div>
</div>

<!--
- Each stick will correspond with 1 Gun
  - Left - Blue
  - Right - Red
- The direction the stick is on the controller will be the direction they aim with that gun
  - The guns can only aim in 8 directions around the character (Up, Up-Left,Left, Down-Left,Down, Down-Right, Right, Up-Right)
- Each stick is independent of each other and can overlap (aim exactly in the same direction.
- A line will indicate which lane each gun is aiming down.
- If using a controller, the player will be able to set the dead zones and the angles for the straight and diagonal lanes. In general, the angles for the diagonal lanes should be wider than the straight lanes\
	_Insert Controller Circle Diagram_ -->

## Shooting
When the character shoots, a single bullet travels down the lane. If the bullet hits an enemy:

- If the enemy can be hit by that bullet: Enemy dies and bullet disappears.
- If the enemy cannot be hit by that bullet: The enemy continues to rush towards the player, the bullet disappears.
- If the bullet reaches the end of the screen,

- Each bumper/trigger on the controller will shoot the corresponding gun (left bumper/trigger for the left gun and vice versa).
  - The guns will only shoot 1 bullet at a time
- The bumpers cannot be held to constantly shoot bullets
- Bullets
  - travel in straight lines and at a constant speed (speed may be modified based on the in-game effects E.g. Slow motion)
  - When hitting an enemy will destroy the bullet (does not travel through enemies)
- Successfully killing an enemy will enable Hit Stop

### Hit Stop
- After successfully killing an enemy, all spawned enemies will stop for a short amount of time.

### Missing a shot
- Missing a shot happens when
  - A player hits the wrong enemy with the wrong gun
  - Bullet reaching the border before hitting an enemy

## Scoring
- There are 2 scores:
  - Points
  - Player Kills
- Points are given when a player kills an enemy
- Points are multiplied by the player’s combo
  - For every 10 units, the multiplier will increase by 1
  - Player kills record how many enemies the player has killed before dying
- Player kills are not affected by combo

## Lives
- The character has 10 lives
- When the character’s lives reach 0, the game is over
- The character loses a life when they let an enemy get too close to them
- The player can gain a life if they shoot a White enemy

## Combos
- Combos begin as soon as the player kills X enemies
- Combos will continue to add on for every enemy they kill
- Combos are a multiplier for your score
- Multiplier begins at 1.0
- Every unit will increase the multiplier by 0.1
- Combos will reset back to 0 when the player is hit or the player misses a shot

### Combo Ability (Kata Mode)
The Combo Ability, Kata Mode, is an ability that puts the player in an autopilot state. The character will begin killing the closest enemies when the combo ability is activated. To activate the combo, the player can activate it at any time with an assigned button. Losing the combo to a hit or miss will not activate Kata Mode. The length of the ability will build up as the player gains a larger combo. Kata Mode increases by X amount every Y kills in the combo.

_E.g. The length of Auto will increase by 0.2s every 20 kills. Kata Mode will last 1 second if the combo ends at 100._

The speed that the character kills enemies needs to be set and the value needs to be affected by the overall game speed. The length of Kata Mode will also be affected by the game speed as the faster the game, shorter Kata Mode will be active.

## Game Speed
Game Speed is the speed at which enemies spawn and move and the player’s bullets move
The Game Speed will be modified depending on the current special effect happening during combat
For Survival, Timed, Endless, the Game Speed will start at 100% and gradually increase the more kills the player gets.
The global game speed will increase by 1% every X units killed
For Story Mode, the levels will begin at a set Game Speed and increase from that point

## Enemies

- Enemies run straight towards the player character
  - Enemy’s run speed is affected by the Game Speed
- Enemies deal 1 life of damage when reaching the player character in the center of the screen.
  - When they collide with the character, the enemy disappears
  - When the enemy collides with the player, ALL OTHER enemies are pushed back. The Game Speed will begin at 0% and then gradually increase back to the current game speed before the player got hit.
  - If there are multiple enemies in the same spawn instance they will reach the player at the same time. In this case, the damage dealt will be equal to:

```
number of enemies / 2 rounded up
1 enemy = 1
2 enemies = 1
3 enemies = 2
4 enemies = 2
8 enemies = 4
```

### Types of Enemies
- Grey - Can be shot by any gun (red or blue)
- Blue - Can only be shot by the blue gun (Left)
- Red - Can only be shot by the red gun (right)
- White - Can be shot by any gun and the player will gain a life when shot
- Purple - Needs to be shot by both guns in quick succession.
- Shielded - Shielded enemies require an extra shot to kill. The rules of the enemy will apply to the shield. E.g Red enemy with a shield requires 2 shots from a red gun. One to destroy the shield, and another to destroy the enemy.

## Player

### Levels
The player level will dictate what special abilities and poses the player will experience through their runs.

### Poses
The player will have a chance to unlock different poses when aiming down angles.

### Special Abilities
These are abilities that the player can use once obtained. The abilities will be obtained after killing a certain number of enemies in a level. The skill needs to be unlocked in story mode to be used in other single player games.
- **Armor Piercing Bullet** - Clear one lane of its enemies. The player can choose which gun shoots the bullet. Only one gun can be used per APB
- **Screen Wipe** - Clear the map of all enemies.
- **Shield** - Give the player a shield and prevent the next hit.
- **Adrenaline Rush** - Slow down the enemy’s movement speed
- **Grey Out** - All enemies will become normal enemies
- **Priority Shot** - Being able to target a specific enemy within the middle of the lane

## Game Special Effects
On occasion, certain special effects will occur to switch up the pace and give the player some breathing room.

## Game Stats
