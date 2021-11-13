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

Bullet Time is similar to _Hit Stop_ but occurs randomly on kill and slows down the enemies rather than fully stop their movement. When Bullet Time activates, the effect can be extended by killing more enemies before the time runs out. Each kill will reset the time, but will increase the rate at which the Bullet Time depletes. A bar will represent the time you have in Bullet Time and should deplete overtime. Bullet time will continue until the bar is empty. Afterwards, the enemies should immediately start moving as before.

### Camera

The camera is at a fixed position placing the character in the center of the screen. The camera will zoom out under certain effects such as when a player wields a _Sniper Rifle_, but will return to its previous position afterwards.

### Knockback

When a player is hit, all enemies are pushed away from the player. This is to give the player time to re-adjust if the number of enemies approaching becomes overwhelming. The enemies are pushed back a certain distance, keeping the order that they've spawned. There will be a brief moment that the enemies have fully stopped before the enemies begin move again. They will gradually increase speed until they have returned to their original speed. This gradual increase is exponential rather than linear.
