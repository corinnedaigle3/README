# README
What I did in every project.

## Game Design: ##


### AllHailSewerRat: (GameJam) ###

**Itch:** https://ghost-knights.itch.io/all-hail-sewer-rat

**Github:** https://github.com/corinnedaigle3/AllHailSewerRat

<br>
Code:

<br>PatrolRat –

•	Sets waypoints and states depending on player location/detection.

•	Lose condition (caught)

<br>RatKing –

•	Controls the Rat King boss AI.

•	Handles movement toward/away from the player.

•	Detects player sight, attack, and text ranges.

•	Plays music and sound effects based on game state.

•	Shows dialogue/text during the fight or cutscene.

•	Lose Condition (collisions with projectiles) 

<br>PresentRatKing (for testing)–

•	Rotates the object to face the player.

•	When player in range:

o	Show UI text

o	Win Screen

<br>RatProjectileWCheese –

•	No effect on player.

<br>HPBars –

•	Controls the Rat King boss HP bar UI.

•	Checks the RatKing script for:

o	talkingDone → whether the cutscene/dialogue has finished.

o	DoorWithCheese → whether the player has cheese, which affects HP bar behavior.

<br>RatProjectile – 

•	Detects collisions with any object.

•	Destroys player and projectile on collision w/ player.

<br>Projectile –

•	Fires a projectile in the forward direction of the LookAtPoint object.

•	Detects collisions with:

o	Enemies ("Enemy" tag) → destroys both projectile and enemy.

o	Rat King ("RatKing" tag) → destroys both projectile and boss.

<br>MainCreditsUI –

•	Controls the Main Menu UI. 

•	Handles visibility of main menu and credits panels.

•	Unlocks the cursor so the player can click UI buttons.

<br>PauseMenu –

•	Pauses/Unpauses the Game

<br>
Music / SFX:

•	Picked out the music


<br><br>
### BedtimeRebellion: (GameJam) ###

**Itch:** https://ghost-knights.itch.io/bedtime-rebellion

**Github:** https://github.com/corinnedaigle3/BedtimeRebellion


<br><br>
### Dating-Roguelike: ###

**Itch:** None

**Github:** https://github.com/popoyo07/dating-roguelike

<br>Code:

DeckUIManager – 

•	Handles instantiating a card in the UI for every card in player deck.

DeckManager – Helped by setting reffs

•	Referencing/Hookup to DeckUIManager.

<br>AllCardsOfCharacter –

•	Database for storing card images and names.

<br>MusicManager – 

•	Connects and controls all music and SFX to volume slides.

<br>Rewards – 

•	Handles adding and showcasing rewards after player defeats an enemy.

<br>MenuButtons –

•	Sets UI elements active or inactive

<br>CanvasMainMenu –

•	Sets UI elements active or inactive

<br>ChooseRoom –

•	This script handles room selection in a game, where the player chooses between two rooms. 

•	Each room has a corresponding enemy, and sometimes a boss room overrides the normal enemy visuals. 

•	It updates UI buttons to show which enemies are in each room and queues the chosen enemy to spawn.

<br>MoveRoomA –

•	Initializes the variables

•	Triggers movement when BattleState is WON

•	Teleports to starting position once destination is reached (for “endless rooms” effect)

<br>MoveRoomB –

•	Initializes the variables

•	Triggers movement when BattleState is WON

•	Teleports to starting position once destination is reached (for “endless rooms” effect)

<br>EnemySpawner – (Helped, only did part of Boss Code, Rest Done by Me)

•	Enemy & Boss Selection

o	Randomly selects an enemy type list (sirenList, vampireList, or idkList).

o	Tracks rooms visited to determine when to spawn a boss (roomsSpawnBoss).

•	Spawning Logic

o	Normal enemies spawn randomly from the active list.

o	Players can queue a specific enemy to spawn next.

o	Bosses spawn in specific rooms (6, 12, 18) and override normal enemies.

•	Music Control

o	Stops all music and plays the appropriate boss track when a boss spawns.

o	Resumes default music when boss is defeated or skipped.

•	Cleanup

o	DestroyEnemy() removes normal enemies.

o	DestroyBoss() removes boss and resets flags.

•	Integration with BattleSystem

o	Works closely with BattleSystem.state to trigger spawns after a battle is won.

o	Tracks which room the player is in to increment boss room counters.


<br>
Music SFX:

•	I picked and set up all the music and SFX for the game


<br><br>
### FatesoftheFallen: ###

**Itch:** https://ghost-knights.itch.io/fates-of-the-fallen-byghostknights

**Github:** https://github.com/corinnedaigle3/FatesoftheFallen

<br>
Code:

<br>TeleportPlayerWaterE – 

•	Handles teleporting the player when entering a trigger (for example, falling into water)

•	Also notifies the level manager if the player has fallen.

<br>Inventory – 

•	Handles storage and management of items the player owns.

•	Supports stackable and non-stackable items and triggers events when the inventory changes.

<br>Item –

•	Represents an individual item that can exist in the player's inventory.

•	Each item has a type, an amount, and a way to get its visual representation (sprite).

<br>Item Assets –

•	Holds all the sprites for the inventory.

<br>UI_Inventory –

•	It takes the list of Item objects from your Inventory class and creates button slots for each one on the screen.

<br>Cam – 

•	Makes the player’s movement direction follow the camera’s facing direction.

•	Smoothly rotates the player model toward the direction of input.

•	Uses camera orientation to calculate movement relative to where the player is looking.

<br>PlayerMovement – 

•	Handles the movements and abilities of the player.

<br>ImageFade – 

•	Handles the visual icon that tells the player that they can dodge.

•	Unlocks when player is in enemy range. 

<br>UI – Helped with this one by setting things active and inactive.

•	Handles all UI logic for the game:

o	Menu activation per scene

o	Pause / resume control

o	Scene transitions

o	Cursor visibility and navigation

o	Button navigation through EventSystem

<br>
Music / SFX:

•	I picked and set up all the music and SFX for the game minus the music for Elysium. 

•	Created one of the screams in Tarturus.

<br>
Cut Scenes / Video: 

Created, co-wrote the scripts, and animated all the cut scenes.

Created the marketing video


<br><br>
### Group-Proj-2-Hallway (The Flamebound Gem): ###

**Itch:** https://antro55.itch.io/flameboundgem

**Github:** https://github.com/kingkaue/Group-Proj-2-Hallway


<br><br>
### PATCHED: ###

**Itch:** None

**Github:** https://github.com/corinnedaigle3/PATCHED


<br><br>
### SummerJam (Purr Summer): (GameJam) ###

**Itch:** https://ghost-knights.itch.io/purr-summer

**Github:** https://github.com/popoyo07/SummerJam


<br><br>
### Small Coding Projects: ###

**Itch:** None

**Github:**
