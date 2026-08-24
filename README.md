# dRally Vita 

* Based on work of urpx : https://github.com/urxp/dRally
* Based on EnriqueSomolinos port for psvita : https://github.com/enriquesomolinos/dRally-vita

🎮 Installation Guide

Step 1: Install the Game App
Download and install the .vpk file on your PlayStation Vita using VitaShell.

Step 2: Prepare the Data Files
Download death rally data template.zip from the Releases section.

Extract it and copy the data folder directly into the root of your ux0: partition.

This automatically creates the path ux0:data/DERA00002/DATA/ with the pre-configured cdrom.ini.

Step 3: Copy Steam Game Files
Open your Death Rally installation folder on your PC (via Steam).

Copy all the game files from your PC.

Paste them directly inside ux0:data/DERA00002/DATA/ on your Vita.

Step 4: Move the Cinematic Files
Inside the DATA folder on your Vita, locate the 3 files ending in .HAF.
Move those 3 .HAF files into the CINEM folder.
````
Ux0:data/DERA00002/DATA
    |--/CINEM
    |  |--ENDANI.HAF
    |  |--ENDANI0.HAF
    |  |--SANIM.HAF
	|--CDROM.INI        [1]
    |--ENGINE.BPA
    |--IBFILES.BPA
    |--MENU.BPA
    |--MUSICS.BPA
    |--TR[0-9].BPA

	[1] CDROM.INI contains relative location of CINEM directory (./CINEM)
`````
🎮 Native Control Layout
Once the custom dr.cfg is placed in the data folder, the handheld controls will map as follows:
````
D-Pad: Smooth and continuous steering (fixed the legacy tap-steering bug).
R Trigger: Accelerate.
L Trigger: Brake / Reverse.
X (Cross): Nitro / Turbo (Also acts as Keypad-Enter for general menu navigation).
Square (□): Shoot main weapons.
Circle (○): Drop mines.
Triangle (△): Horn / Native Exit Shortcut (Sends 'Y' key to instantly quit races in the pause overlay).
