# CS-2110-Android-Project
Software Development Methods

Ghost Hunter
Your task is to develop a game for the Android… let your creativity run wild…!

Project Manager should ask “(how) does this fit into our product?”
Software Architect should ask “(how) will this fit into our code design?”
User Interface Designer should ask “(how) will the user see this?”
Quality Assurance Manager should ask “(how) do we know it doesn't break something?”
Note, a person as responsibility to see X is done well (X is one of the roles above), NOT that this person does all of X. Everyone codes! If your team consists of 5 members, two people can take on the same role (but not the Project Manager role - only one person should be responsible for this role.) If your team consists of 3 members, one person should take on two roles.

Required Functionality
Have a splash screen noting at least
All teammate names
The university (University of Virginia), course (CS 2110), and semester (Fall 2014)
Some kind of identifying logo, image, or name
If someone gave you unusually major assistance, acknowledge them too
See the user/character on the screen (relative location to onscreen elements) and see the user/character move. Suggestions on implementing movement are as follows (this is by no means a complete list):
Buttons (e.g. up, down, left, right) to move the user/character
Use the android accelerometer (tilting to move the user/character)
Use touch (touching the screen or draging your finger across the screen to cause movement)
(Do NOT use the GPS feature with Google maps! Try to find alternative ways to implement movement)
Auto-generate ghosts at locations relatively near the user
note: this does not mean the ghosts then dynamically move after being spawned. If you want this functionality see the "move" optional item below)
Have a view of the world (e.g. a room, some scenery, dungeon, …) where the user and ghosts are both seen on screen relative to one another
note: this does not need to have a map background; user + ghost on a blank background is fine
Have some technique for "killing" ghosts
Keep track of some sort of progress statistics (points, number of kills, etc.)
and be able to display that information
Optional Functionality and Product Grading
There are many possible games you can make within these constraints. Maybe yours is all about running around faster than the ghosts; maybe it's more of a scavenger hunt trying to find how to vanquish each ghost; maybe it's about tricking or trapping or otherwise disabling them. The details are up to you.

Points	Tag	Functionality
50	 	Required functionality (see above).
7	move	Ghosts move on their own.
5	dangerous	Getting too close to a ghost is dangerous (harms user in some way if the user collides with the ghost).
5	front	(requires move and dangerous): Their front is dangerous (harms user in some way if the user collides with the ghost's front).
3	back	(requires move): Their back is vulnerable (harms the ghost in some way if the user collides with the ghost's back).
5	proximity	If the user gets within a predetermined distance from a ghost, a proximity alert appears (you can implement this alert any way you choose, e.g. sound, toasts, other text, use of images, use of colors, etc.)
5-20	objects	There are objects lying about the environment that can be collected. A greater variety of objects or including objects that have more significant effects on gameplay will result in more points awarded.
5	loot	A slain ghost leaves behind some loot that can be collected.
7	special item	Each ghost may have a special item hidden somewhere; there is some action on this item that can kill the associated ghost. Note: this item is separate from "objects."
5–15	steps	(optionally requires special item): Killing a ghost involves several steps, collecting items and/or information to find the special item that can be used to kill the ghost. Note: you may choose not to involve a special item in these steps.
3	ignore	(requires proximity): When a proximity alert appears, the user can chose to ignore the ghost in some way.
5	discover	(requires special item): When a proximity alert appears, the user can chose to discover how this particular ghost can be killed.
5	money	There is some kind of money system: you earn by staying alive and/or killing ghosts and can spend to get extra features or powers.
5	costview	(requires money): Features that cost money dynamically appear/disappear or become selectable/not selectable as sufficient funds are/are not available.
5	ongoing	(requires money): Some feature has an ongoing cost, consuming money while it is active. If funds run out while it is active, it automatically shuts off.
5	bombs	You can find/buy ghost bombs that clear out all nearby ghosts.
5	detectors	(requires special item): You can find/buy detectors that let you find the special items more easily.
5	wildcard	(requires steps): You can find/buy some kind of wildcard item that lets you bypass usual kill steps.
5	repellent	(requires move): You can find/buy ghost repellent that causes ghosts to flee from you for a time.
5	barriers	(requires move): You can lay ghost barriers, lines that ghosts cannot cross.
3	limited	(requires barriers): Barriers are limited in some way: temporary, hard to find, or cost something.
5	enclosed	(requires barriers): An enclosed ghost dies (eventually or immediately.)
10	saved	Progress is saved between distinct runs of the app.
10	restore	(requires saved and dangerous): On restore, a similar danger level is restored.
10	background	Background mode: when the app is paused, it updates everything less often to conserve battery.
10	intersection	(requires background, move, and dangerous): in background mode, updates infrequent enough that special intersection code is needed (and present) to detect intervening collisions.
5	self-enclosed	(requires barriers and intersection): You could choose to enclose yourself in a barrier; this way no ghosts can attack or harm you. You may want to do this before you pause the app (see background): so you do not have to worry about being attacked.
30	shared	Game state is shared between multiple devices simultaneously.
10	trade	(requires shared and something to trade): Users can trade with one another.
5–15	difficulty	The difficulty can be adjusted either in a settings menu or by having it increase over time.
0+	friendly	There are friendly ghosts that either don't interact at all (0 pt), offer a minor annoyance or assistance (5–10 points), or play a more major role of some sort (more points).
1–10	befriend	(requires friendly): There is some action needed to befriend a ghost and make it friend, ranging from something almost automatic (1 points) to several non-trivial things that must all be done correctly (10 points).
1–10	sidekick	(requires befriend and perhaps objects): Once you befriend a ghost you can choose to turn it into your side kick (if you possess a particular object, reach a particular level, etc.)
0–5	visual	Your app is visually impressive (in the sole discretion of your TA; do NOT ask the TA if it is impressive in advance of the final presentation.)
3+	variable movement	Implement some different ways for the user to move around. More points will be awarded for more complex/visually stimulating effects.
5+	sound	Include sound effects/background music. More points depending on the quality/number of different effects.
5	animation	Objects and/or the player have some kinds of animation. For example: spinning coins, collectible items that bounce up and down.
3-5	high scores	There is some way to remember previous scores and play statistics.
Items with variable point values will be weighed by your TA according to their estimation of the difficulty of the feature and the value of the feature in the game. If you go above and beyond on a particular item, you might get more than the listed point value.

You are welcome to add things not on the above list if you have a different idea of where your game is going. Run these by a TA during lab meeting first, then put a short description in your progress report so we can assign it points.

There are over 200 points in the above list, and more possible with creativity. If you earn more than 100, the excess will count at 10% of their listed value:

if (optionalPoints > 50) 
    score = requiredPoints + 50 + (optionalPoints - 50) * 0.1;
else
    score = requiredPoints + optionalPoints;
