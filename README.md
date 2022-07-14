# Ragley's Skyrim Together Reborn Testing Repo

I am fairly new to wabbajack and also github so bear with me, and let me know if theres improvements to make. I will be updating this when I make changes, and/or find more mods. Likely I'll be adding more soon.

## References
Throughout this guide I will make references to specific folders, they are:
- Skyrim Game Folder
  - Where the Skyrim.exe is located
- Data Folder
  - The Data folder within your skyrim game folder
- STR Installation folder
  - The location where wabbajack installs Mod Organizer 2

## Clean Install Skyrim
1. Follow the guide here: https://wiki.tiltedphoques.com/tilted-online/guides/client-setup up until the Mod Organizer 2 section. Past this will be covered by this guide.

## Install Wabbajack
1. Install Wabbajack according to the instructions at: https://github.com/wabbajack-tools/wabbajack (__NOT IN ROOT OF DRIVE, PROGRAM FILES, or DOWNLOADS. It needs to be in a new folder__)
2. Download the Wabbajack files from this repo.
3. Open Wabbajack and select install from disk.
4. Sign in to nexus when prompted (premium HIGHLY recommended)
5. Install the instance to a separate folder. (e.g. X:/Games/SkyrimTogether
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
Good news is they will persist between installs and you likely wont have to do it again.

1. Go to http://enbdev.com/mod_tesskyrimse_v0475.htm and download the enbseries .zip file
2. Open the archive and go to the Wrapper folder
3. Extract ONLY the d3d11.dll and d3dcompiler_46e.dll to the base skyrim install folder, where skyrimSE.exe is located
4. Go to the "Game Folder Files" folder in your STR Installation folder.
5. Open the SKSE folder and select:
	- DATA folder
	- skse64_loader
	- skse64_1_6_353.dll
	- skse64_steam_loader.dll
6. Copy these to your base skyrim game folder where SkyrimSE.exe is located
7. Go to the NVT folder within the Game Files Folder
8. Go to "1. Main File" folder and pick a preset. I recommend 2.
9. Enter the chosen preset folder and copy the contents to your __BASE GAME FOLDER__ (SkyrimSE.exe folder)
10. Go back to the NVT folder and into "2. Optional DOF Strengths"
11. Repeat Step 9 with your chosen DOF preset. I highly recommend 6.
12. That should install SKSE and an ENB, unless you have another game modifying your skyrim game with an ENB you wont have to repeat these steps. (But you shouldn't since you should be starting with a clean install.
13. (Optional Step): For a warmer ENB, in your (Base Game)/enbseries/ replace the enbeffect.fx.ini with my custom one from the files downloaded here.

## Smoothcam Functionality
1. in MO2 Right-Click the STR Mod, and press remove.  
2. Run the game through the SKSE Launcher by selecting it from the executable dropdown menu in the upper right.
3. Make a new game and new character, press R to accept character creation
4. Wait for MCM messages to stop.
5. Go 3rd person and ensure Smoothcam is working. If you've never used smoothcam before you will easily be able to tell.
6. Save the game (non-quicksave)
7. open the console (~ key) and enter "qqq" to quit the game
8. Reinstall the STR mod (should be in downloads tab) and place it directly below smoothcam, above USSEP, where it was before.
9. Run the game through SkyrimTogether executable from MO2.
10. __LOAD__ your save you just created. Do not use "Continue"
11. Ensure Smoothcam is working.
12. Open the console > qqq
13. Relaunch Skyrim Together. 
14. Smoothcam should work on new games you make now.
15. If issues still persist, such as the fatal camera offset error, you can try manually installing smoothcam
    - If you go this route take extra care to remember exactly what files you moved in case you have to remove them later
    - I won't cover this as I've not tried it, you should know what you're doing before trying this.
    - Alternatively, just disable Smoothcam in MO2

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
1. Use normal saves instead of Quicksaves, and turn off autosave functionality.
   - These have been known to start causing issues for extended play in Skyrim so I recommend against relying on them.
2. If you experience bugs and aren't sure whats causing them first refer to: https://github.com/tiltedphoques/Mod-Compatibility for information on mods used with STR.
   - I will do my best to avoid these in the installation process but its not yet very solid at what works properly with STR.
   - If you check that mod compatability page and also check the modpages of the installed mods and still can't figure it out, post an issue and I will try to help as best I can.

### Thanks for playing!
- Ragley
