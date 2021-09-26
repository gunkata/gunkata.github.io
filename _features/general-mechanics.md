---
title: Gameplay Mechanics
order: 1
---

Gun Kata is a survival game. It is played until the player runs out of lives. Their goal is to either: Kill the most enemies or have the highest score.

### Scoring

There are two scores for the player to keep track of: The number of enemies they've killed and an overall point score. The points are gained by killing enemies but will vary based on the combos.

#### Combos

A combo begins after the player gets 10 consecutive kills in a row. This means that the correct bullet has been used to kill the enemy. An incorrect bullet used to hit an enemy results in a failed combo and will therefore reset the combo counter. The combo is a direct multiplier when calculating your score,  starting at x1 when the combo begins (begins after 5 kills) and adding up per kill. E.g. A grey enemy is worth 1 point and with a combo of 20, the kill will yield 20 points for single grey enemy. Combos will also reset if the player shoots down a lane with no enemies.

### Global Game Speed

The Global Game Speed is an overall modifier to all things that move. As the game progresses, the Global Game Speed increases making it more difficult for the player. There will be effects in the game that decrease the Global Game Speed, however, these effects will only be temporary and the game will resume at the speed that it was previously before the effect.

### Hit-Stop

When a bullet kills an enemy, all enemies will stop moving for a brief moment. Hit Stop will help the player set the pace for the multitude of enemies that approach the player at once. The small amounts of time that each kill gives will add to the player's advantage. If the player is fast enough, the Hit Stop may overlap, resulting in a longer period in Hit Stop.

### Bullet Time

Bullet Time is similar to _Hit Stop_ but occurs randomly and slows down the enemies rather than fully stop their movement. This will be another tool that is activated by killing an enemy. The speed will be fixed meaning that regardless of the _Global Game Speed_ the Bullet Time will set the Global Game Speed to a set value rather than reduce it by a set amount. Bullet Time lasts longer than Hit Stop but should not overlap in time, meaning you cannot activate another Bullet Time whilst it's already active.

### Camera

The camera is at a fixed position placing the character in the center of the screen. The camera will zoom out under certain effects such as when a player wields a _Sniper Rifle_, but will return to its previous position afterwards.

### Knockback

When a player is hit, all enemies are pushed away from the player. This is to give the player time to re-adjust if the number of enemies approaching becomes overwhelming. The enemies are pushed back a certain distance, keeping the order that they've spawned. There will be a brief moment that the enemies have fully stopped before the enemies begin move again. They will gradually increase speed until they have returned to their original speed. This gradual increase is exponential rather than linear.
