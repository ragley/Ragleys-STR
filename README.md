# Ragley's Skyrim Together Reborn Testing Repo

I am fairly new to wabbajack and also github so bear with me, and let me know if theres improvements to make. I will be updating this when I make changes, and/or find more mods. Likely I'll be adding more soon. I apologize for the hoop-jumping to get the install working properly, part is due to me being new at wabbajack lists, part due to mod author permissions, and part due to issues with STR. I hope you'll bear with me, I will do my best to walk you through it. 

## Troubleshooting
You can reach me through the discord to help with troubleshooting, as well as talk with other people using the modpack.
Feel free to join the discord at: https://discord.gg/xTr26KDndy

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
- At least 150 Gb storage space on an SSD
  - HDD will work but expect slower loads and possibly pop in, I havent tested anything on a HDD in a long time

## References
Throughout this guide I will make references to specific folders, they are:
- Installation/Instance folder
  - The location where wabbajack installs Mod Organizer 2
  - (e.g. ```X:/Games/RSTR/```)
- Skyrim Game Folder
  - This is within the in instance folder
  - Where the Skyrim.exe is located
  - (e.g. ```X:/Games/RSTR/Game Root/```)
- Data Folder
  - The Data folder within the skyrim game folder
  - (e.g. ```X:/Games/RSTR/Game Root/Data```)


## Wabbajack
1. Install Wabbajack according to the instructions at: https://github.com/wabbajack-tools/wabbajack (__NOT IN ROOT OF DRIVE, PROGRAM FILES, or DOWNLOADS. It needs to be in a new folder__)
2. Download the latest release .zip from this repo and extract it to a folder anywhere.
3. Open Wabbajack and select install from disk.
4. Sign in to nexus when prompted (premium HIGHLY recommended)
5. Install the instance to a separate folder. (e.g. X:/Games/RSTR)
6. When it says "Installation Complete," Select open instance, open Mod Organizer, and proceed with the rest of this guide.

## ENBSeries
I finally figured out how to utilize the stock game feature of Wabbajack, so luckily for you this means less installation steps on your part. Unfortunately the ENBSeries and ENB preset must still be installed manually. (This is due to the distribution limitations in place by the author.)
### __ENBSeries__
If you havent installed an ENB ever you can do it like this:
1. Go to http://enbdev.com/mod_tesskyrimse_v0475.htm and download the enbseries .zip file
2. Open the archive and go to the Wrapper folder
3. Extract ONLY the d3d11.dll and d3dcompiler_46e.dll to the Game Root folder within the instance folder (e.g. X:/Games/RSTR/Game Root/), where the SkyrimSE.exe is located

### __The Truth - ENB Preset__
If you removed a previous ENB Preset or are continuing to install a new one follow these steps:
1. Go to https://www.afkmods.com/ and create an account.
2. Once you have an account go to https://www.afkmods.com/index.php?/files/file/2241-the-truth-enb/ and download the full version of The Truth ENB.
3. Open the archive and copy the contents to the Game Root folder. (enbseries folder, enbseries.ini, and enblocal.ini)
4. Extract the "Presets for grass collisons" archive in your Game Files Folder where MO2 is located.
5. Enter the folder and select a preset. I believe 5 is the most movement and 1 is the least, but I am unsure. I just use 5.
6. That should install The Truth ENB Preset. Unless you have another installation game modifying your skyrim base game with an ENB etc. or you want to change ENB Presets, you wont have to repeat these steps.
7. For a warmer ENB, you can use SHIFT+ENTER to open the ENB menu and edit the enbbloom.fx and enbeffect.fx sections to match these respectively:
   - [LINK TO ENB BLOOM SETTINGS]
   - [LINK TO ENB FX SETTINGS]

## BethINI Configuration
I have included Bethini to allow for easy customization of .ini files. Before launching any executables from MO2, you should run BethINI.
  1. Close MO2, leaving it open causes issues with BethINI.
  2. Navigate to /RSTR/Tools/BethINI Standalone/
  3. Launch BethINI.exe
  4. Ensure the settings on the ```Setup``` tab show the proper paths, and the INI path is the ```ModOrganizer > Default``` option.
  5. In the ```Basic``` tab select your resolution and other optional settings. (they have tooltips if you hover)
  6. Select the ```Recommended Tweaks``` box, and then click your desired preset. (I __DO NOT__ recommend ultra, High is still very demanding, I'd recommend medium)
  7. Hit ```Save & Exit```
  
## Launching The Game
BEFORE launching STR, a couple things need to be taken care of. 
  1. With the ENB installed, you must run the game through SKSE.
  2. Ensure ENB is working (it will tell you in the upper left corner)
  3. Start a New Game, ignore character creation, choose a start just to get into the world.
  4. Make a manual save. 
  5. Quit the game.
  
When you first run STR you have to select the proper .EXE file. This is __NOT__ SKSE.
- At the prompt, select "SkyrimSE.exe" from /RSTR/Game Root/. __(Make sure it is the correct one)__
- If you select the wrong one simply close the popup.
- I have included the ```-r``` argument by default in the executable within MO2, this means you will have to select it every launch
  - If you would like to disable the repeating selection:
  1. Be sure you have successfully run STR at least once.
  2. Hit the green gears icon at the top of MO2
  3. Select ```Skyrim Together Reborn - Nemesis Version```
  4. Remove ```-r``` from the arguments field.

## Smoothcam Functionality
To get Smoothcam to work follow these steps:
1. Launch STR.
2. Manually load the save you just made __(NOT CONTINUE)__
3. Make a new save.
4. Quit the game.

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

### Racemenu Edits
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


## Disclaimer
 __You are free to modify this list how you want, however you do so at your own risk. I am a student who enjoys skyrim modding in his free time and I don't have the time or energy to provide support on a modded setup that I don't know what exactly has been done. Should you decide to make modifications, all responsibility for problems that occur falls on you, and I respectfully as you search elsewhere for the solutions.__

# Thanks for playing! -Ragley
