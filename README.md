# README
My contributions to every project.

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

<br>
Code:

<img width="975" height="376" alt="image" src="https://github.com/user-attachments/assets/b5bbe767-2d94-4c56-8861-e941b9804303" />

<img width="975" height="251" alt="image" src="https://github.com/user-attachments/assets/4d7889e0-1fd9-4f3e-8b3d-3e60826c70c6" />

<img width="975" height="677" alt="image" src="https://github.com/user-attachments/assets/bc0352e4-3b3e-497f-a730-d876ac87ad8a" />

<img width="975" height="206" alt="image" src="https://github.com/user-attachments/assets/fd1345ee-f65e-4b2c-8a5e-25f3167119c2" />

<img width="975" height="366" alt="image" src="https://github.com/user-attachments/assets/17906f6c-e77a-4b11-a46d-bac0f4f7a373" />

<img width="975" height="206" alt="image" src="https://github.com/user-attachments/assets/9f00a1d3-0eb4-4791-a46d-a088e289095f" />

<img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/40d4b50d-142a-471c-b9d6-c46ba731c462" />


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

<br>pSpawn - 

•	Sets the spawn location of the player after they teleport

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

<br>
Code:

Visibility – 

•	Sets sprites visible or invisible based on player distance from object(s). 

<br>GameOverScreen – 

•	Shows when player is caught

o	Restart

o	Back to menu

<br>WinScreen –

•	Shows when player retrieves item

o	Restart

o	Back to menu

<br>MainMenu –

•	Play game

•	Quit application

•	Show Credits

<br>DragonAttack – 

•	If collision with the player, end game.

<br>DragonFollow –

•	The dragon actively chases the player.

•	If the player is gazing upon the dragon, teleport it to safe space, then continue following.

<br>DragonVisibility –

•	Checks if player is in line of sight.

<br>
Music / SFX:

•	I picked and set up all the music and SFX for the game.


<br><br>
### PATCHED: ###

**Itch:** None

**Github:** https://github.com/corinnedaigle3/PATCHED


<br><br>
### SummerJam (Purr Summer): (GameJam) ###

**Itch:** https://ghost-knights.itch.io/purr-summer

**Github:** https://github.com/popoyo07/SummerJam

<br>
Code:

Saving -

- Handles saving scores both during runtime and when exiting the application.

- Handles updating new high scores and the latest score.

- Handles tickets.

<br>CatTower (SandCastle) -

- Dragging Sprites
- Correct sprite handling
- Timer

<br>LitterBox (Dig Sand) -

- Clicking buttons
- Randomizing numbers


<br><br>
## Small Coding Projects: ##

**Github:** https://github.com/corinnedaigle3?tab=stars

<br><br>
### Coding2_Lab1: ###

Github: https://github.com/corinnedaigle3/Coding2_Lab1

<br>
ChessBoard – 

•	Draws an eight by eight grid using Gizmos.DrawLine.

<br>HandlePiece – 

•	Draws a custom Scene view gizmo for GameObjects with the script

<br>ColorPiece – 

•	Allows user to change the pawns color in the inspector in reatime

<br><br>
### Coding2_Lab2: ###

Github: https://github.com/corinnedaigle3/Coding2_Lab2/blob/main/Assets/Runtime/CubeBehaviour.cs

<br>
CubeBehaviourEditor– 

•	Handles the size of cubes, selection of cubes, and button for cubes

<br>SphereBehaviourEditor– 

•	Handles the size of spheres, selection of spheres, and button for spheres

<br>CubeBehaviour– 

•	Holds the variable for the size of cubes

<br>SphereBehaviour– 

•	Holds the variable for the size of spheres

<br><br>
### Coding2_Lab3: ###
Github: https://github.com/corinnedaigle3/Coding2_Lab3

<br>
Targeting – 

•	Handles enemy movement (rotating around the player, while never hitting the player)

<br>PlayerMovement – 

•	Basic player movement

<br><br>
### DIG4778C_Lab4: ###

Github: https://github.com/corinnedaigle3/DIG4778C_Lab4

<br>
Player – 

•	Handles player movement with the new input system

<br>Meteor – (Updated)

•	Updated the meteor script so it will rotate around the player

<br><br>
### Lab5: ###

Github: http://github.com/LilyW3865/Lab5/tree/main

<br>
Avoider – 

•	Handles when the avoider sees the avoided, select new poissin point until hidden.

<br><br>
### Coding2_Lab6: ###

Github: https://github.com/corinnedaigle3/Lab6TextAdv

<br>
DLL – 

•	Text Adventure tutorial 

<br><br>
### Coding_Lab7: ###

Github: https://github.com/Sze0921HY/Coding_Lab7

<br> 
DLL Native – 

•	function to test how long it takes to sort an array

<br>Test DLL – 

•	function to test how long it takes to sort an array

<br><br>
### Coding2_Lab9/10: ###

Github:  https://github.com/corinnedaigle3/Coding2_Lab9

<br>
Target –

•	Sets the rigidbody velocity to move right * speed from TargetBuilder.cs to the spawned targets in TargetSpawner.cs 1-3

•	Destroys target after 5 seconds for optimization.

<br>TargetBuilder –

•	TargetBuilder class holds the variables 

•	The Builder class sets values and retuns the builder

•	Build function is where the GameObjects are created

<br>TargetSpawner(1-3) –  

•	Spawns’ random targets constructed targets from TargetBuilder.cs at set intervals

•	Sets the variables from TargetBuilder.cs

•	Returns the Build function

<br>SaveManager – 

•	Implements the saving/loading when the respective keyboard buttons are pressed and destroys the save when it is loaded.

<br>ISaveable – (Helped)

•	An interface that defines the saved data using an Id. It has a saving class that manages the actual saving and loading of objects.

<br><br>
### Coding2_Lab11: ###

Github: https://github.com/corinnedaigle3/Coding2_Lab11

<br>
Pathfinding – 

•	Sets the NavMeshAgent's target destination to the goal position

•	Draw the calculated path in blue, start cell in green, and goal cell in red

•	Check if grid coordinates are within the grid

<br>LevelGenerator –

•	Set grid width and height

•	Spawns in player

•	Generates grid
