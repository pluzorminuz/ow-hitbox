# ow-hitbox

Contains the Workshop scripts I used for the Hitbox project. As well as the place where everything will be kept up-to-date, instead of updating the Reddit post every time.

# OVERWATCH HITBOXES for EVERY HERO

Thanks KarQ! It features new visualizations made specifically for this video. I hope you enjoyed!

**↓↓↓ Click me! [YouTube Video] ↓↓↓**
[![Play](https://img.youtube.com/vi/0UsX3nborfA/maxresdefault.jpg)](https://youtu.be/0UsX3nborfA)

# Color Coding

Each colour represent something different:

* Green: Normal, body hitbox, fitted
* Red: Critical hitbox, fitted (unless combined with Cyan)
* Blue: Hitbox intersection (with ground) indicator
* Cyan: Manually placed hitbox
* Yellow: Newly added hitbox (in patch comparisons)
* Teal: Shields (e.g. Brig shield)
* Orange: Cannot be shot at at that particular angle (e.g. in Genji's Deflect)

# 1.48 PTR changes (Echo and Reinhardt)

**↓↓↓ Click me! [YouTube Video] ↓↓↓**
[![Play](https://img.youtube.com/vi/JEdYlv4zo2o/maxresdefault.jpg)](https://youtu.be/JEdYlv4zo2o)

## Links

[Click here for the album](https://imgur.com/a/A3Yqjso)

[Click here for an orthographic comparison](https://youtu.be/JEdYlv4zo2o)

## 

Blizzard released [PTR 1.48](https://blizztrack.com/overwatch/ptr/1-48-0-0-68309) today with changes to Echo and Reinhardt's head hitbox. Both hero's head hitbox **volume** was reduced to **78.48%** and **76.93%** of the original respectively. A new hitbox for Echo was made for her obtrusion on her shoulders (highlighted in yellow in the album).

Since these changes could be furthur altered during the PTR cycle, the 360 degree version will be release when these changes hit live.

More detailed numbers (percentage to old model in brackets):

|Hero (%Ana)|Head SA|Body SA|Total SA|Total Vol|Total Vol ^2/3|Head Vol\*\*|Head Vol\*\* ^2/3|
|:--|:--|:--|:--|:--|:--|:--|:--|
|Reinhardt (1.47)|212.2|446.3|427|902|433.3|420.8|260.6|
|Reinhardt (1.48)|158 (74.44)|446.4 (100.02)|422.6 (98.97)|894.9 (99.21)|431 (99.47)|323.7 (76.93)|218.8 (83.96)|
|Echo (1.47)|136.8|152.4|151.1|138.9|124.5|171.2|143.1|
|Echo (1.48)|100.4 (73.38)|154.1 (101.12)|149.6 (99.05)|137.4 (98.97)|123.6 (99.31)|134.3 (78.48)|121.7 (85.08)|

\*\* This number was taken by considering the entire Head hitbox, disregarding the obstructed portion (because it is hard to define the separation between body and head. Take these numbers very carefully

# Current Hitboxes (1.47)

**↓↓↓ Click me! [YouTube Video] ↓↓↓**
[![Play](https://img.youtube.com/vi/KzmIBtG1sf0/maxresdefault.jpg)](https://youtu.be/KzmIBtG1sf0)

## Links

[Click here for the GIF album](https://imgur.com/a/AN33T4F)

[Click here for the YouTube playlist](https://www.youtube.com/playlist?list=PL61EEnh7kA_NEbti6BLQmXEtjzcBKuRdY)

[Click here for an orthographic comparison](https://youtu.be/KzmIBtG1sf0)

[Video commentary](https://youtu.be/xsXvr3Cr5k8)

Feel free to use these resources for whatever you want.

## 

This is a follow-up post to [this back in November 2019](https://www.reddit.com/r/Overwatch/comments/dzzzhh/visualizing_hitboxes_in_overwatch/). This version provides a 360 degree view of the entire hero with hitbox representation at a very high precision, as well as showing the critical areas.

Scans were performed using a Workshop script, and then extracted from the game, converted, and imported to Blender. Capsules and polygons meshes were fitted to the point cloud. The result was then overlayed onto in-game screenshots.

Since the entire process takes time, the scans were performed since December 2019 to March 2020 through many patches, both on Live and PTR. The [detailed list of patch used, and misc. stats are shown here](https://docs.google.com/spreadsheets/d/19t4ftrkYY3IfmQ2YlylAha0VbOfDjiJ4InIKyjwlX70/edit?usp=sharing)

Improvements over the last version:
* Full 360 degree view, can use any angles in the future since the data has already been taken, only new screenshots are needed.
* Very high precision, up to 5 decimal places (±0.000005m or ±0.005mm in error). This allow spheres to be fitted at high accuracy.
* Shows critical area without relying on in-game critical detection.
* Shows hitboxes under ground level. Blue spots indicated hitboxes close to or intersecting the ground. Hitboxes below ground are fainter.

The only drawback is still there is no consistent way of locking the idle animation — freezing a hero does not set its animation to 0. So for heroes like Zenyatta, Sigma, Lucio, Mercy, Mei suffer from a more discrepancy between each screenshot than other heroes.

We can also calculate the size of the hitboxes for comparison. Here I used various metric, including **Surface Area (SA)** and **Volume (Vol)** and **Volume ^2/3**, as pointed out by u/nspr, the third metric may be a better number to represent the size of the hitboxes. All numbers in %Ana.

\*\* This number was taken by considering the entire Head hitbox, disregarding the obstructed portion (because it is hard to define the separation between body and head. Take these numbers very carefully

|Hero (%Ana)|Head SA|Body SA|Total SA|Total Vol|Total Vol ^2/3|Head Vol\*\*|Head Vol\*\* ^2/3|
|:--|:--|:--|:--|:--|:--|:--|:--|
|**Tank**|
|D.Va|114.6|505|472.7|1179.8|518.2|463|277.8|
|D.Va (Pilot)|115.4|97.5|99|105.5|103.6|124.6|115.8|
|Orisa|271.8|504.1|484.9|866.1|421.7|505.3|294.5|
|Reinhardt|212.2|446.3|427|902|433.3|420.8|260.6|
|Roadhog|267.4|361.6|353.8|761.1|386.9|678.9|358.5|
|Sigma|132.7|207.5|201.3|232.7|175.6|204.7|161.2|
|Winston|294.8|449.9|437.1|955.5|450.3|771.2|390.3|
|Winston (Primal)|513.2|737.3|718.8|2155.6|774.6|1678.1|655.4|
|Wrecking Ball|183.1|604|569.2|1181.9|518.9|446.2|271|
|Wrecking Ball (Ball)|0|275.9|253.1|785.9|395.3|0|0|
|Zarya|165.9|152.2|153.4|202.7|160.2|227.9|173.2|
|**Support**|
|Ana|100|100|100|100|100|100|100|
|Baptiste|75.1|136.8|131.7|138.3|124.1|105.3|103.5|
|Brigitte|87.6|123.5|120.5|123.4|115.1|99.4|99.6|
|Lúcio|80.7|114|111.2|126.7|117.1|74.7|82.3|
|Mercy|93.8|112.8|111.3|106.2|104.1|100.5|100.4|
|Moira|116.4|98.8|100.2|121.8|114.1|171.2|143.1|
|Zenyatta|149.7|102|106|152.1|132.3|227.9|173.2|
|Zenyatta (Transcendence)|145.4|114.9|117.4|161.7|137.7|227.9|173.2|
|**Damage**|
|Ashe|156|99.2|103.9|89|92.6|178.2|147|
|Bastion (Recon)|225.2|296.4|290.5|379.2|243.2|321.1|217.7|
|Bastion (Sentry)|79.8|285.9|268.8|372.8|240.4|184.3|150.3|
|Bastion (Tank)|0|368.9|338.4|196|156.6|0|0|
|Doomfist|122.2|234.1|224.8|286.5|201.7|158.6|136|
|Echo|136.8|152.4|151.1|138.9|124.5|171.2|143.1|
|Genji|95.8|115.2|113.6|122|114.2|124.6|115.8|
|Hanzo|91.7|116.9|114.8|121.7|114|93.2|95.4|
|Junkrat|119.2|132.5|131.4|98.8|99.2|128.6|118.3|
|McCree|122.2|152.1|149.7|121.8|114.1|165.7|140.1|
|Mei|73.4|97.7|95.7|101.1|100.8|104.9|103.2|
|Pharah|129.2|206.6|200.2|196.1|156.7|178.2|147|
|Reaper|155.6|143.4|144.5|195|156.1|227.9|173.2|
|Sombra|83.2|92.3|91.6|77.9|84.7|87.3|91.3|
|Soldier: 76|112.4|120|119.4|142.8|126.8|171.2|143.1|
|Symmetra|136.9|114.7|116.5|130.1|119.2|166.1|140.3|
|Tracer|119.6|117.2|117.4|139.9|125.1|124.6|115.8|
|Torbjörn|144.8|166.7|164.9|222.8|170.6|262.1|190.1|
|Widowmaker|148.9|107.7|111.2|131.7|120.1|178.2|147|

## Raw Data

If you want the raw numbers, it’s included in [the spreadsheet](https://docs.google.com/spreadsheets/d/19t4ftrkYY3IfmQ2YlylAha0VbOfDjiJ4InIKyjwlX70/edit?usp=sharing).

## Trivia:

* Total amount of data point extracted: 7279051
* Out of all hitboxes, only 3 are not in form of a sphere/capsule. This is in
  1. Rip Tire model on Junkrat’s back (I believe the actual Tire in his ultimate is the same)
  1. The lid on Hammond’s mech
  1. The treads on Bastion’s Tank form
* A lot of hitboxes have “nice” numbers. For example, capsule with radius or length 0.20000, 0.40000, 0.25600, 0.43200, 0.12800. This is NOT observed in Sigma’s hitboxes
* The camera settings in-game are 103 degrees, with a distance of 3.09m (exception: 3.4m for Wrecking Ball’s Mech Form).
* The outbreak of COVID-19 gave me enormous amount of free time to work on this project
* The Workshop update on patch 1.45 speeds up the scanning process by at least 10 times
* If you looked close enough, one of Winston’s Primal hitbox is coloured cyan, because it wasn’t fitted, it was placed manually
* Mercy holding a pistol is not included because Mercy’s hitboxes alone took me soooo long
* The bonus clip is for Wrecking Ball’s T-Pose / reference pose. Someone found a glitch of [forcing Hammond dummy bot to crouch](https://www.reddit.com/r/Overwatch/comments/fe90um/til_wrecking_ball_has_an_unreleased_crouch/). Turns out there is no hitbox pose that match the ref pose, it just uses its idle pose. Just a funny glitch I’d like to share.

## Workshop Script

[Click here for the Workshop script I used](https://drive.google.com/file/d/1bWv0hWLdb3MbApAp6m0bdPu5kYHsFwGl/view?usp=sharing)

Or just use the code **GBFGK** (for 1.46)

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

## Format of the copied csv

Each line is one entry, the syntax is
`server_tick, variable_target, variable_1, variable_2, ... , variable_26`

Therefore after one scan, you should only see the following types of lines
* `0.016, veriable_target, 0, 0, ...,0` (26 zeroes)
   * The first two lines must be in this format, they contains no data and can be ignored
* `server_tick, variable_target, {}, {}, 0, 0, ... ,0` (24 zeroes)
   * This is no hits in that vertical slice
* `server_tick, variable_target, {(point_1); (point_2); ... ; (point_n)}, {(point_1); (point_2); ... ; (point_n)}, 0, 0, ... ,0` (24 zeroes)
   * This is n hits in both directions
* `server_tick, variable_target, {(point_1); (point_2); ... ; (point_n)}, {}, 0, 0, ... ,0` (24 zeroes)
   * This is L scan only
* `server_tick, variable_target, {}, {(point_1); (point_2); ... ; (point_n)}, 0, 0, ... ,0` (24 zeroes)
   * Similarily, this is R scan only

## Notes

1. If you have many data (>30000 in total), the game will freeze after copy. This is completely normal, the copy is processing in the background. The script is only designed to do 1 scan per session, so expect to get kicked by the server after copying the data.

## Update Log

|Date||
|:--|:--|
|200512|* Added color code explanation|
|200513|* Added Junkrat's Mine, Junkrat's Trap, Genji's Deflect, Training Bot, Brigitte Shield, Mercy Valkyrie to the playlist|
