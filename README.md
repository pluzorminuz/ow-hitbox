# owws-scripts

Contains the Workshop scripts I used for the Hitbox project. With other useful scripts maybe.

# Documentation

Before you start, be reminded that this script **does not** show you the hitbox in-game, it just extracts the data.

The syntax used here are the new C-style syntax from 1.48 onwards.

## How the scan works

The enemy bot is spawned at `Global.BOT_POSITION = Vector(0, 0, 0)`, and when you select a hero, you will be placed in-front of the bot for confirmation. The bot is facing towards the **positive z-axis**, so it's left-hand direction is towards **positive x-axis**. For the rest of the document, all directions are in terms of the bot.

The start- and end-point for the ray casts are located in array `Global.RAY_CAST_VECTORS[0]` and `Global.RAY_CAST_VECTORS[1]`. `Global.RAY_CAST_VECTORS[2]` defines the positive **depth** direction and `Global.RAY_CAST_VECTORS[3]` defines the positive **height** direction. By default, the beams are scanning from the front and back of the bot. One beam starts at `[0]` to `[1]` and the other from `[1]` to `[0]`, effectively scanning from both directions.

The `Global.RAY_CAST_VECTORS` can be rotated in order to perform scans from different direction. **Voice line right** rotates the entire scan setup **counterclockwise horizontally** by 90-degrees. To confirm, the top-right HUD **B-R-C** now read 0-**1**-0. Each time it rotate horizontally the **R** value increases by one, therefore it will goes throught the cycle 0,1,2,3. **Voice line left** rotates the entire scan setup **counterclockwise vertically** by 90-degrees. It will update the **B value** in B-R-C, so pressing once will show **1**-0-0. You can combine the rotations freely, but technically only 0-0-0, 1-0-0, and 0-1-0 are useful.
* Example: 0-1-0 will perform a side scan, L is bot's left-to-right and R is bot's right-to-left. Depth
* Example: 1-0-0 will perform a top-down scan, L is bot's foot-to-head and R is bot's head-to-foot. Depth direction is identical to 0-0-0, but positive Height direction is now bot's back-to-front

Each scanline undergoes 2 for loops, first loops the height value, than the depth value, both inclusive. The script first use `Ray Cast Hit Player` to check if the beam hit a player or not, then proceed to call `Ray Cast Hit Position` to obtain the actual data. This is done to avoid large amount of redundant data. Turn this check off if you want to scan building (e.g. Junkrat's Steel Trap).

You can individually scan each direction. Scan directions are indicated by **L** and **R** in the script. By default, **L** is the front-to-back direction, and **R** is the back-to-front direction.
* Pressing **Interact** scans both directions
* Pressing **Ultimate status** scans L only
* Pressing **Group up** scans R only

The position of the hits are stored in **player variable of the player**, in `l_hit_store` and `r_hit_store`. The array is refreshed after each vertical slice, so each **entry** in the debug inspector is effectively 1 vertical slice. Currently, I can store 420 vectors in 1 array without problem, but I'm not sure if it can handle any higher amount. The entire debug entries are copied for furthur processing.

## Variables to set

1. Set the bounds. `Global.SCAN_DEPTH_BASE`, `Global.SCAN_DEPTH_LIMIT`, `Global.SCAN_HEIGHT_BASE`, `Global.SCAN_HEIGHT_LIMIT`
1. Set the hero to spawn. `Global.__FIRST_HERO`
1. Set the resolution. `Global.DELTA_DEPTH_STATIC`, `Global.DELTA_HEIGHT_STATIC`
1. Set the orientation of the scan. `Voice Line Right`, `Voice Line Left` in game

## Notes

1. If you have many data (>30000 in total), the game will freeze after copy. This is completely normal, the copy is processing in the background. The script is only designed to do 1 scan per session.
