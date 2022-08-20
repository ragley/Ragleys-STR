# Ragley's Skyrim Together Reborn

I am fairly new to wabbajack and also github so bear with me, and let me know if theres improvements to make. I will be updating this when I make changes, and/or find more mods. Likely I'll be adding more soon. Feel free to join the discord: https://discord.gg/xTr26KDndy

## Included Mod Highlights
<details>
  <summary>Click to Expand</summary>

- Skyrim Together Reborn
- Smoothcam
- USSEP (Non CC dependent version)
- SKyUI
- Nordic UI
- True Directional Movement
- The Elder Scrolls Legends Loading Screens
- SMIM
- High Poly Project
- Skyrim 2018/2020/Terrain Parallax
- Blended Roads
- Racemenu
- CBBE
- Tempered Skins (male/female)
- KS Hairdos
- Alternate Start
- Better Jumping
- Smilodon
- Rustic Clothing
- Immersive Weapons and Armors
- Bandolier
- Cloaks of Skyrim
- Cathedral Armory
- Wearable Lanterns
- NPCs Walk and Run at Your Own Pace
- A Quality World Map
- Carriage Stops of Skyrim
- Point the Way
- Lux, Lux Via, Lux Orbis
- Embers XD
- Inferno
- KD -  Realistic Fireplaces
- Many ENB Particle Lights
- The Truth - ENB Preset
- Deadly Spell Impacts
- Dwemer Pipework Reworked - With ENB Lights
- Dwemer Automatons Glowmapped
- Dwemer Weapons Glowmapped
- Folkvangr
- The Grass Must Grow
- Landscape Fixes for Grass Mods
- Grass Collisions
- Immersive Sounds Compendium
- Security Overhaul
- Realistic Melee Range
- Strange Runes
- Ordinator
- JKs Skyrim
- All JKs Interiors
- Sidequests of Skyrim
- Vanguard and Leviathan Animations
- EVG Animation Variance
- Spell Perk Item Distributor
- First Person Combat Animations Overhaul
- Gesture Animations Remix
- Fixed Face Discoloration
- Bunch of JS models
- Immersive Equipment Displays
- Mura Presets for IED
- Tweaked Animation Priority
- Staff Animations
- More Plant Retextures
- Majestic Mountains
- Volumetric Mists
- Fluffworks
- FISSES
- Improved weapon Impact Effects
- Smoother Skies
- Ethereal Clouds
- Water for ENB
- Bandit Lines Expansion
- Underdog Animations
- College of Winterhold - Quest Expansion
- Eyes of Beauty - Ai Remastered
- Improved Closedfaced Helmets
- VIGILANT
  - Seems to work, but if multiple people enter Windspeak Inn in Dawnstar when first starting the quest it can cause a crash
  - When traveling for quests and meeting an npc that's walking there, follow with them because fast traveling/coc does not pass time that I can tell so they will still be walking for a long time.
- Wet and Cold
- Rain, Ash, and Snow Shaders (RASS)
- Vanguard Crossbow Animations
- MCM Recorder to auto-configure MCMs at start of new game
- Weather Control
- Realistic Regeneration
- Mysticism
- Apocalypse
- Basic Camp Gear
</details>

## Requirements
This seems pretty performance friendly overall, mostly due to the ENB preset I think. These are specs that will likely result in good performance in 1080p60fps at most times.
- 2080 Super
- 32G RAM
- Ryzen 7 3700x
- At least 110 Gb storage space on an SSD
  - HDD will work but expect slower loads and possibly pop in, I havent tested anything on a HDD in a long time

## References
Throughout this guide I will make references to specific folders, they are:
- Skyrim Game Folder
  - Where the Skyrim.exe is located
- Data Folder
  - The Data folder within your skyrim game folder
- Installation folder
  - The location where wabbajack installs Mod Organizer 2

## Clean Install Skyrim
1. Follow the guide here: https://wiki.tiltedphoques.com/tilted-online/guides/client-setup up until the Mod Organizer 2 section. Past this will be covered by this guide.

## Wabbajack
1. Install Wabbajack according to the instructions at: https://github.com/wabbajack-tools/wabbajack (__NOT IN ROOT OF DRIVE, PROGRAM FILES, or DOWNLOADS. It needs to be in a new folder__)
2. Download the latest release .zip from this repo and extract it to a folder anywhere.
3. Open Wabbajack and select install from disk.
4. Sign in to nexus when prompted (premium HIGHLY recommended)
5. Install the instance to a separate folder. (e.g. X:/Games/RSTR)
6. When it says "Installation Complete," Select open instance, open Mod Organizer, and proceed with the rest of this guide.

## Set your Skyrim.ini and SkyrimPrefs.ini settings
1. In MO2 click the puzzle icon at the top and select ini editors
2. Select SkyrimPrefs.ini and find the [DISPLAY] section
3. Adjust these parameters to your desired specifications: 	
	- bBorderless=0
	- bFull Screen=1
	- iSize H=1080
	- iSize W=1920
4. Copy all text in the box
5. Save to a text file OUTSIDE your SkyrimTogetherReborn installation folder
6. If you have to reinstall the entire STR installation for some reason, you can paste your backup into the inis again
7. Repeat steps 4-6 if you make changes to either your skyrim.ini or SkyrimPrefs.ini to ensure changes are kept between installs

## ENBSeries and Game Folder Files
Due to how Wabbajack works and me being too retarded to figure out how to do it, these need to be installed manually.
Good news is they will persist between installs and you likely wont have to do it again. If you are coming from a previous install of this modpack you first need to delete a few files, as I've switched the ENB.

### Removing a Previously Installed ENB Preset
This step is semi optional if you like the current ENB setup and it perfoms well. Personally, my friends and I have experienced MUCH better performance on this new one but the old one still works. If you want to keep the old ENB (or another preset of your choice), skip this subsection and complete steps 4, 5, and 6 of "The Truth - ENB Preset" subsection.
1. Go to your base Skyrim Install Folder, where SkyrimSE.exe is located
2. Select the files and folders:
   - enbseries (folder)
   - enbcache (folder)
   - enbseries.ini
   - enblocal.ini
3. Delete these files.

### __Installing the ENB and SKSE__
#### __SKSE__
If you havent installed SKSE you can do it like this:
1. Go to the "Game Folder Files" folder in your STR Installation folder.
2. Extract the SKSE archive.
3. Open the SKSE folder you just made and select:
	- DATA folder
	- skse64_loader
	- skse64_1_6_353.dll
	- skse64_steam_loader.dll
4. Copy these to your base skyrim game folder where SkyrimSE.exe is located.

#### __ENBSeries__
If you havent installed an ENB ever you can do it like this:
1. Go to http://enbdev.com/mod_tesskyrimse_v0475.htm and download the enbseries .zip file
2. Open the archive and go to the Wrapper folder
3. Extract ONLY the d3d11.dll and d3dcompiler_46e.dll to the base skyrim install folder, where skyrimSE.exe is located

#### __The Truth - ENB Preset__
If you removed a previous ENB Preset or are continuing to install a new one follow these steps:
1. Go to https://www.afkmods.com/ and create an account.
2. Once you have an account go to https://www.afkmods.com/index.php?/files/file/2241-the-truth-enb/ and download the full version of The Truth ENB.
3. Open the archive and copy the contents to your base skyrim folder. (enbseries folder, enbseries.ini, and enblocal.ini)
4. Extract the "Presets for grass collisons" archive in your Game Files Folder where MO2 is located.
5. Enter the folder and select a preset. I believe 5 is the most movement and 1 is the least, but I am unsure. I just use 5.
6. Copy the enbgrasscollisions.ini file to your game directory, where the SkyrimSE.exe is located.
7. That should install The Truth ENB, and grass collisions. Unless you have another installation game modifying your skyrim base game with an ENB etc. or you want to change ENB Presets, you wont have to repeat these steps.
8. For a warmer ENB, you can use SHIFT+ENTER to open the ENB menu and edit the enbbloom.fx and enbeffect.fx sections to match these respectively:
   - [enbbloom.fx](https://github.com/ragley/Ragleys-STR/raw/dev/bloomfx.jpg)
   - [enbeffect.fx](https://github.com/ragley/Ragleys-STR/raw/dev/effectfx.jpg)

## Management of Creation Club Content
Skyrim comes with AE Creation Club Content by default, and the creators of STR recommend deleting this content. However a number of mods require Unofficial Skyrim Special Edition Patch. to function, but this also relies on CC content. The USSEP author has hidden downloads of past versions of the mod, but they are still availible to download through Nexus directly. If it is not included in the Wabbajack Install you can get the last AE, non CC dependent USSEP mod here: https://www.nexusmods.com/skyrimspecialedition/mods/266?tab=files&file_id=241103
0. Close M02 if it is open.
1. Go to your skyrim data folder and select all creation club content. (Files like ccXXXXXXXXX.esm/.esp/.bsa)
2. Add these files to an archive and name it CCContent.zip or something like that.
3. Delete the Creation Club content from the Data folder, leaving the archive.
4. If you ever want to use the free AE content, simply go to MO2 and add the zip you created as a mod, then place it just below the skyrim DLC's.

## Launching STR for the First Time
When you first run STR you have to select the proper .EXE file. This is __NOT__ SKSE.
- At the prompt, select "SkyrimSE.exe" from your base Skyrim folder.
- If you select the wrong one follow these steps:
  1. Select the executables setting in MO2 (Green Gears)
  2. Select SkyrimTogetherReborn
  3. in the arguments field add: ```-r```
  4. Click "OK" and launch STR again.
  5. Close the game and remove the -r argument or it will ask every time you launch the game.

## Smoothcam Functionality
1. In MO2, uncheck the SmoothCam Mod
2. Run STR then start a new game and skip through character creation
3. Save the game then quit to desktop (or console > qqq)
4. Enable SmoothCam in MO2.
5. Launch STR and load that save. (Not Continue)
6. SmoothCam should be working and will stay working when starting a new game.

## Immersive Equipment Display Presets
I've included Mura's presets for Immersive Equipment Displays and this is how to enable them. Likely you'll have to do this every new game you start as it doesn't seem to stay.
1. Press the DELETE (DEL) key to open the UI for IED
2. Click VIEW on the menubar and select custom.
3. Select the checkbox for either gender, and also slect sync.
4. From the dropdown menu under "Preset" select "Coin Pouch for JS by Mura"
5. Click "Merge" then OK
6. Repeat step 4 and 5 for:
   - Potions for APS by Mura
7. Press the x at the top or ESC to close the UI

## Racemenu Edits
To attempt to ensure racemenu changes are synced in game, follow these steps.
1. Launch STR from MO2
2. Start a New Game
3. Skip initial character creation by just pressing accept.
4. Chose your start and sleep in the bed
5. Once you have loaded in, open console (~) then enter "showracemenu"
6. Make the desired changes to your character
   - Some things will not sync like custom hair color (i think), and body morphs (both racemenu and cbbe)
7. Accept and name your character
8. Save the game in a new save (__MANUAL__)
9. Only now should you connect to a server. Your characters appearance should be synced with the other players.
10. If you want to make changes, disconnect from the server and repeat steps 6-9, or else other people will not see them.
    
## Tips When Playing (WIP)
1. Don't Save when playing on a server. The server/STR handles this.
2. Try to allow the party leader to enter cells first, both interior and exterior to avoid the issue of invisible enemies.
3. If you experience bugs and aren't sure whats causing them first refer to: https://github.com/tiltedphoques/Mod-Compatibility or https://wiki.tiltedphoques.com/tilted-online/guides/troubleshooting for information on STR and mods.
   - I will do my best to avoid these in the installation process but its not yet very solid at what works properly with STR.
   - If you check that mod compatability page and also check the modpages of the installed mods and still can't figure it out, post an issue and I will try to help as best I can.
4. Always have the party leader join the server first and create the party.
   - The party leader should be physically in front of the party when travelling to ensure they are the first to enter a new cell
   - The party leader should be the only person progressing quests to help keep everything synced.
     - If someone other than the party leader progresses a quest, have the party leader repeat the same steps to catch up.
5. Do not join a server before selecting your start. This can cause problems.


# Disclaimer
## You are free to modify this list how you want, however you do so at your own risk. I am a student who enjoys skyrim modding in his free time and I don't have the time or energy to provide support on a modded setup that I don't know what exactly has been done. Should you decide to make modifications, all responsibility for problems that occur falls on you, and I respectfully as you search elsewhere for the solutions.

# Thanks for playing!
- Ragley
