# Ragley's Skyrim Together Reborn Testing Repo
## Install Wabbajack
1. Install Wabbajack according to the instructions at: https://github.com/wabbajack-tools/wabbajack (NOT IN ROOT OF DRIVE, PROGRAM FILES, or DOWNLOADS. It needs to be in a new folder)
2. Download the Wabbajack files from this repo.
3. Open Wabbajack and select install from disk.
4. Sign in to nexus when prompted (premium HIGHLY recommended)
5. Install the instance to a separate folder. (e.g. X:/Games/SkyrimTogether
6. When it says "Installation Complete," Select open instance, open Mod Organizer, and proceed with the rest of this guide.

## Set your Skyrim.ini and SkyrimPrefs.ini settings
1. In MO2 click the puzzle icon and select ini editors
2. Select SkyrimPrefs.ini and find the [DISPLAY] section
3. Adjust these parameters to your desired specifications: 	
	bBorderless=0
	bFull Screen=1
	iSize H=1080
	iSize W=1920
4. Copy all text in the box
5. Save to a text file OUTSIDE your SkyrimTogetherReborn installation folder
6. If you have to reinstall the entire STR installation for some reason, you can paste your backup into the inis again
7. Repeat steps 4-6 if you make changes to either your skyrim.ini or SkyrimPrefs.ini to ensure changes are kept between installs

## ENBSeries and Game Folder Files
Due to how Wabbajack works and me being too retarded to figure out how to do it, these need to be installed manually.
Good news is they will persist between installs and you likely wont have to do it again.
1. Go to http://enbdev.com/mod_tesskyrimse_v0475.htm and download the enbseries zip
2. Open the archive and go to the Wrapper folder
3. Extract ONLY the d3d11.dll and d3dcompiler_46e.dll to the base skyrim install folder, where skyrimSE.exe is located
4. Go to the "Game Folder Files" folder in your STR Installation folder. Unzip the SKSE and NVT archives to folders here.
5. Open the SKSE folder and select the 
	DATA folder
	skse64_loader
	skse64_1_6_353.dll
	skse64_steam_loader.dll
6. Copy these to your base skyrim game folder where SkyrimSE.exe is located
7. Go to the NVT folder you got from the archive.
8. Go to "1. Main File" folder and pick a preset. I recommend 2.
9. Enter the chosen preset folder and copy the contents to your base game folder (SkyrimSE.exe folder)
10. Go back to the NVT folder and into "2. Optional DOF Strengths"
11. Repeat Step 9 with your chosen DOF preset. I highly recommend 6.
12. That should install SKSE and an ENB, unless you have another game modifying your skyrim game with an ENB you wont have to repeat these steps.
13. (Optional Step): replace the enbseries.ini in your skyrim directory with my custom one from the files downloaded here.

## Smoothcam Functionality
1. in MO2 Right-Click the STR Mod, and press remove.  
2. Run the game through skse
3. Make a new game and new character, press R to accept character creation
4. Wait for MCM messages to stop.
5. Go 3rd person and ensure smoothcam is working. If you've never used smoothcam before you will easily be able to tell.
6. Save the game (non-quicksave)
7. open the console and enter "qqq" to quit the game
8. Reinstall the STR mod (should be in downloads tab) and place it directly below smoothcam, where it was before.
