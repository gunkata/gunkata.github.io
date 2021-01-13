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
- If the bullet reaches the end of the screen: The bullet disappears and the player is stunned.

The guns that the player holds are single shot firearms. Multiple bullets can be fired at a time as long as the player is not **stunned**.

<!-- - Each bumper/trigger on the controller will shoot the corresponding gun (left bumper/trigger for the left gun and vice versa).
  - The guns will only shoot 1 bullet at a time
- The bumpers cannot be held to constantly shoot bullets
- Bullets
  - travel in straight lines and at a constant speed (speed may be modified based on the in-game effects E.g. Slow motion)
  - When hitting an enemy will destroy the bullet (does not travel through enemies)
- Successfully killing an enemy will enable Hit Stop -->

### Hit Stop
- After successfully killing an enemy, all enemies that have spawned will stop for a short amount of time. The enemies will gradually return to the current game speed.

### Missing a shot
Missing a shot will end the player's combo. Missing a shot happens when:

  - A player hits the wrong enemy with the wrong gun
  - Bullet reaching the border before hitting an enemy

When the player misses, the character is momentarily stunned being unable to shoot or aim.

## Scoring

There is a score for each game that is based around the performance of the player during that game. The player is awarded points for each kill he gets during the game and those points are multiplied by the combo the player has.

## Lives
The player has begins the game with X amount of lives each game. The player loses life when an **Enemy Instance** reaches the player. The player can gain lives if they shoot a White Enemy. The player cannot exceed the amount of life that they started with at the beginning of the game. If the player has 0 life, the game ends.

## Combos
A player begins a combo by killing enemies consistently without missing a hit or getting hit by an enemy.  The combo is also a multiplier that grows with every kill starting at 1 and increasing by 0.1 per kill. Combos begin after the player's 10th consecutive kill.

<!-- - Combos begin as soon as the player kills X enemies
- Combos will continue to add on for every enemy they kill
- Combos are a multiplier for your score
- Multiplier begins at 1.0
- Every unit will increase the multiplier by 0.1
- Combos will reset back to 0 when the player is hit or the player misses a shot -->

### Combo Ability (Kata Mode)
The Combo Ability, Kata Mode, is an ability that puts the player in an autopilot state. The character will begin killing the closest enemies when the combo ability is activated. To activate the combo, the player can activate it at any time with an assigned button. Losing the combo to a hit or miss will not activate Kata Mode. The length of the ability will build up as the player gains a larger combo. Kata Mode increases by X amount every Y kills in the combo.

_E.g. The length of Auto will increase by 0.2s every 20 kills. Kata Mode will last 1 second if the combo ends at 100._

The speed that the character kills enemies needs to be set and the value needs to be affected by the overall game speed. The length of Kata Mode will also be affected by the game speed as the faster the game, shorter Kata Mode will be active.

## Game Speed
Game Speed is a factor that speeds up all elements of the game. The game begins at the set Game Speed assigned and gradually increases as the game goes on. The Game Speed caps at it's _starting value plus 300%_. E.g. A level that begins with a Game Speed of x2 and caps at x5. A level that begins with a Game Speed of x1.5 caps at x4.5.

### Player Game Speed
The **Player Game Speed** is a separate factor that can be changed at any time: Browsing through the menu or In-Game. This value is multiplicative to the **Game Speed** and ranges between x1 - x3. Starting the Player Game Speed at x1 is equal to _1 x Game Speed_, Starting at x2.2 is equal to _2.2 x Game Speed_.

## Enemies

Enemies spawn around the player in one of eight directions and run straight towards the player. Enemies run at a constant pace who's movement speed is affected by the Game Speed.

Enemies that spawn at the same time are part of the same Spawn Instance. Spawn Instances should not be able to overtake each other. The order of the Spawn Instances need to kept the same as when they were spawned.

An enemy that reaches the player deals damage based on the number of enemies in the Spawn Instance. The damage dealt is equal to:
```
Damage = number of enemies / 2 rounded up

1 - 2 enemies = 1 Damage
3 - 4 enemies = 2 Damage
5 - 6 enemies = 3 Damage
7 - 8 enemies = 4 Damage
```
<!-- - Enemies run straight towards the player character
  - Enemy’s run speed is affected by the Game Speed
- Enemies deal 1 life of damage when reaching the player character in the center of the screen.
  - When they collide with the character, the enemy disappears
  - When the enemy collides with the player, ALL OTHER enemies are pushed back. The Game Speed will begin at 0% and then gradually increase back to the current game speed before the player got hit.
  - If there are multiple enemies in the same spawn instance they will reach the player at the same time. In this case, the damage dealt will be equal to: -->

The enemies are killed when shot with the correct gun. There are multiple types of enemies which will be listed below:

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
