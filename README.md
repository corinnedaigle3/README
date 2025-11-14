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

- Controls the Rat King boss AI.

-	Handles movement toward/away from the player.

-	Detects player sight, attack, and text ranges.

-	Plays music and sound effects based on game state.

-	Shows dialogue/text during the fight or cutscene.

-	Lose Condition (collisions with projectiles) 

<br>PresentRatKing (for testing)–

- Rotates the object to face the player.

- When player in range:

- Show UI text

- Win Screen

<br>RatProjectileWCheese –

-	No effect on player.

<br>HPBars –

-	Controls the Rat King boss HP bar UI.

-	Checks the RatKing script for:

-	talkingDone → whether the cutscene/dialogue has finished.

-	DoorWithCheese → whether the player has cheese, which affects HP bar behavior.

<br>RatProjectile – 

-	Detects collisions with any object.

-	Destroys player and projectile on collision w/ player.

<br>Projectile –

- Fires a projectile in the forward direction of the LookAtPoint object.

- Detects collisions with:

-	Enemies ("Enemy" tag) → destroys both projectile and enemy.

-	Rat King ("RatKing" tag) → destroys both projectile and boss.

<br>MainCreditsUI –

-	Controls the Main Menu UI. 

-	Handles visibility of main menu and credits panels.

-	Unlocks the cursor so the player can click UI buttons.

<br>PauseMenu –

-	Pauses/Unpauses the Game

<br>
Music / SFX:

-	Picked out the music


<br><br>
### BedtimeRebellion: (GameJam) ###

**Itch:** https://ghost-knights.itch.io/bedtime-rebellion

**Github:** https://github.com/corinnedaigle3/BedtimeRebellion

<br>Code:

Main Scene Code –

-	Parent Alarm System - which alerts the player if they make too much noise.

-	Score system - Every time the player completes a puzzle, the player's score increases.

-	Random spawn - The teddy bear in the maze randomly picks one of three locations to spawn at the start of the game.

-	Correct item identification - Score will only increase if all the correct items are placed in the proper slots. 

-	Sleep logic - to counteract getting caught by the parents, the player can make their way to the bed to fake sleep, and cancel the end of the game. 

<br>BP_Planets (All planets minus Earth and Jupiter) - 

- Set the speed of the planets
  
- Moves the planets along a predetermined path


<br><br>
### Dating-Roguelike: ###

**Itch:** None

**Github:** https://github.com/popoyo07/dating-roguelike

<br>Code:

DeckUIManager – 

-	Handles instantiating a card in the UI for every card in the player deck.

<br>DeckManager – Helped by setting reffs

-	Referencing/Hookup to DeckUIManager.

<br>AllCardsOfCharacter –

-	Database for storing card images and names.

<br>MusicManager – 

-	Connects and controls all music and SFX to volume slides.

<br>Rewards – 

-	Handles adding and showcasing rewards after player defeats an enemy.

<br>MenuButtons –

-	Sets UI elements active or inactive

<br>CanvasMainMenu –

-	Sets UI elements active or inactive

<br>ChooseRoom –

-	This script handles room selection in a game, where the player chooses between two rooms. 

-	Each room has a corresponding enemy, and sometimes a boss room overrides the normal enemy visuals. 

-	It updates UI buttons to show which enemies are in each room and queues the chosen enemy to spawn.

<br>MoveRoomA –

-	Initializes the variables

-	Triggers movement when BattleState is WON

-	Teleports to starting position once destination is reached (for “endless rooms” effect)

<br>MoveRoomB –

-	Initializes the variables

-	Triggers movement when BattleState is WON

-	Teleports to starting position once destination is reached (for “endless rooms” effect)

<br>EnemySpawner – (Helped, only did part of Boss Code, Rest Done by Me)

-	Enemy & Boss Selection

-	Randomly selects an enemy type list (sirenList, vampireList, or idkList).

-	Tracks rooms visited to determine when to spawn a boss (roomsSpawnBoss).

-	Spawning Logic

-	Normal enemies spawn randomly from the active list.

-	Players can queue a specific enemy to spawn next.

-	Bosses spawn in specific rooms (6, 12, 18) and override normal enemies.

-	Music Control

-	Stops all music and plays the appropriate boss track when a boss spawns.

- Resumes default music when the boss is defeated or skipped.

-	Cleanup

-	DestroyEnemy() removes normal enemies.

-	DestroyBoss() removes the boss and resets flags.

-	Integration with BattleSystem

-	Works closely with BattleSystem.state to trigger spawns after a battle is won.

-	Tracks which room the player is in to increment boss room counters.


<br>
Music SFX:

-	Picked and set up all the music and SFX for the game


<br><br>
### FatesoftheFallen: ###

**Itch:** https://ghost-knights.itch.io/fates-of-the-fallen-byghostknights

**Github:** https://github.com/corinnedaigle3/FatesoftheFallen

<br>
Code:

<br>TeleportPlayerWaterE – 

-	Handles teleporting the player when entering a trigger (for example, falling into water)

-	Also notifies the level manager if the player has fallen.

<br>pSpawn - 

-	Sets the spawn location of the player after they teleport

<br>Inventory – 

-	Handles storage and management of items the player owns.

-	Supports stackable and non-stackable items and triggers events when the inventory changes.

<br>Item –

-	Represents an individual item that can exist in the player's inventory.

-	Each item has a type, an amount, and a way to get its visual representation (sprite).

<br>Item Assets –

-	Holds all the sprites for the inventory.

<br>UI_Inventory –

-	It takes the list of Item objects from your Inventory class and creates button slots for each one on the screen.

<br>Cam – 

-	Makes the player’s movement direction follow the camera’s facing direction.

-	Smoothly rotates the player model toward the direction of input.

- Uses camera orientation to calculate movement relative to where the player is looking.

<br>PlayerMovement – 

-	Handles the movements and abilities of the player.

<br>ImageFade – 

-	Handles the visual icon that tells the player that they can dodge.

-	Unlocks when the player is in enemy range. 

<br>UI – Helped with this one by setting things active and inactive.

-	Handles all UI logic for the game:

-	Menu activation per scene

-	Pause/resume control

-	Scene transitions

-	Cursor visibility and navigation

-	Button navigation through EventSystem

<br>
Music / SFX:

-	Picked and set up all the music and SFX for the game minus the music for Elysium. 

-	Created one of the screams in Tarturus.

<br>
Cut Scenes / Video: 

- Created, co-wrote the scripts, and animated all the cut scenes.

- Created the marketing video


<br><br>
### Group-Proj-2-Hallway (The Flamebound Gem): ###

**Itch:** https://antro55.itch.io/flameboundgem

**Github:** https://github.com/kingkaue/Group-Proj-2-Hallway

<br>
Code:

Visibility – 

-	Sets sprites visible or invisible based on player distance from object(s). 

<br>GameOverScreen – 

-	Shows when the player is caught

-	Restart

-	Back to menu

<br>WinScreen –

-	Shows when the player retrieves the item

-	Restart

-	Back to menu

<br>MainMenu –

-	Play the game

-	Quit application

-	Show Credits

<br>DragonAttack – 

-	If a collision with the player occurs, end the game.

<br>DragonFollow –

-	The dragon actively chases the player.

-	If the player is gazing upon the dragon, teleport it to a safe space, then continue following.

<br>DragonVisibility –

-	Checks if the player is in line of sight.

<br>
Music / SFX:

-	Picked and set up all the music and SFX for the game.


<br><br>
### PATCHED: ###

**Itch:** None

**Github:** https://github.com/corinnedaigle3/PATCHED

<br>
Code:

Bp_PickUpEquiptLeg – 

-	Handles picking up the leg and setting the player's speed

<br>BP_ PickUpEquiptArm –

-	Handles picking up the arm
  
<br>BP_NewBoxPush -

-	Handles simulating movable objects' physics
  
-	Handles if the player can interact with it
  
-	Controls move object SFX
  
<br>BP_AlwaysMovingPlatform –

-	Allows and sets move positions
  
-	Always move
  
<br>BP_ActivateMovingPlatform –

-	Allows and sets move positions
  
-	Moves on activation
  
<br>BP_ActivateMovingPlatformOn_Off–

-	Allows and sets move positions
  
-	Moves on activation once
  
<br>BP_Lore-4 –

-	Handles showing lore pop-up on/off-screen

<br>BP_LoreManager –

-	Keeps track of which lore sheets have been collected
  
-	Once all are collected, congratulate the player

<br>BP_Crusher – 

- Handles the movement of crusher parts
  
- If player is crushed by the crushed kill player

<br>BP_CrusherButton – 

- Turns the crusher on/off

<br>BP_Grabber –

-	Handles grabber movement
  
-	If the player is in range of the grabber, the player is frozen for 2 sec.
  
-	Resets logic if the player is cut by the saw

<br>BP_Saw –

-	Handles saw movement
  
-	If Saw hits the player, the player loses a limb and is teleported back to the pawn point
  
-	Resets if the hit player

<br>BP_Steam –

-	Handles steam movement
  
-	Steam rolls in and temp blinds the player

<br>BP_ActivateHazards –

-	Activates hazards if the player overlaps

<br>BP_ConveyorBeltCurved –

-	Add forward movement to any object that overlaps

<br>BP_ConveyorBeltStrate –

-	Add forward movement to any object that overlaps

<br>BP_ConveyorButton – 

-	Turn off selected conveyor belts

<br>SFX:

-	FlippingPaper.mp3
  
-	Conveyor1.mp3

-	Conveyor.mp3

-	MonsterScream1.mp3

-	MonsterScream.mp3

-	Dollfootsteps.mp3\
  
- FanSmall.mp3

-	Pulse.mp3

-	PushingObj.mp3

-	SowingFull.mp3

-	ItemDropped.mp3

-	FlipSwitch.mp3

-	Static.mp3

-	LoseLimb.mp3

-	PullStringOp2.mp3

-	PullStringOp1.mp3

-	MachineHum.mp3

-	FanLarge.mp3

-	Beep.mp3

-	Hit.mp3

- Alarm.mp3


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

-	Draws an eight-by-eight grid using Gizmos.DrawLine.

<br>HandlePiece – 

-	Draws a custom Scene view gizmo for GameObjects with the script

<br>ColorPiece – 

-	Allows the user to change the pawn's color in the inspector in real-time

<br><br>
### Coding2_Lab2: ###

Github: https://github.com/corinnedaigle3/Coding2_Lab2/blob/main/Assets/Runtime/CubeBehaviour.cs

<br>
CubeBehaviourEditor– 

-	Handles the size of cubes, selection of cubes, and the button for cubes

<br>SphereBehaviourEditor– 

-	Handles the size of spheres, selection of spheres, and the button for spheres

<br>CubeBehaviour– 

-	Holds the variable for the size of cubes

<br>SphereBehaviour– 

-	Holds the variable for the size of spheres

<br><br>
### Coding2_Lab3: ###
Github: https://github.com/corinnedaigle3/Coding2_Lab3

<br>
Targeting – 

-	Handles enemy movement (rotating around the player, while never hitting the player)

<br>PlayerMovement – 

-	Basic player movement

<br><br>
### DIG4778C_Lab4: ###

Github: https://github.com/corinnedaigle3/DIG4778C_Lab4

<br>
Player – 

-	Handles player movement with the new input system

<br>Meteor – (Updated)

-	Updated the meteor script so it will rotate around the player

<br><br>
### Lab5: ###

Github: http://github.com/LilyW3865/Lab5/tree/main

<br>
Avoider – 

-	Handles when the avoider sees the avoided, select new poissin point until hidden.

<br><br>
### Coding2_Lab6: ###

Github: https://github.com/corinnedaigle3/Lab6TextAdv

<br>
DLL – 

-	Text Adventure tutorial 

<br><br>
### Coding_Lab7: ###

Github: https://github.com/Sze0921HY/Coding_Lab7

<br> 
DLL Native – 

-	function to test how long it takes to sort an array

<br>Test DLL – 

-	function to test how long it takes to sort an array

<br><br>
### Coding2_Lab9/10: ###

Github:  https://github.com/corinnedaigle3/Coding2_Lab9

<br>
Target –

-	Sets the rigidbody velocity to move right * speed from TargetBuilder.cs to the spawned targets in TargetSpawner.cs 1-3

-	Destroys target after 5 seconds for optimization.

<br>TargetBuilder –

-	TargetBuilder class holds the variables 

-	The Builder class sets values and returns the builder

-	The build function is where the GameObjects are created

<br>TargetSpawner(1-3) –  

-	Spawns random targets constructed targets from TargetBuilder.cs at set intervals

-	Sets the variables from TargetBuilder.cs

-	Returns the Build function

<br>SaveManager – 

-	Implements the saving/loading when the respective keyboard buttons are pressed and destroys the save when it is loaded.

<br>ISaveable – (Helped)

-	An interface that defines the saved data using an ID. It has a saving class that manages the actual saving and loading of objects.

<br><br>
### Coding2_Lab11: ###

Github: https://github.com/corinnedaigle3/Coding2_Lab11

<br>
Pathfinding – 

-	Sets the NavMeshAgent's target destination to the goal position

-	Draw the calculated path in blue, start cell in green, and goal cell in red

-	Check if grid coordinates are within the grid

<br>LevelGenerator –

-	Set grid width and height

-	Spawns in the player

-	Generates grid
