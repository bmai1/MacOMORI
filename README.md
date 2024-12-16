How to OMORI on MacOS (MBP M2).

Disclaimer: PlayOnMac is pretty shitty software that is not actively maintained. Wineskin is much more stable.

1. Obtain the game files from sailing the high seas. The folder should be ~2 GB, and the current build is 8879120.
2. Install PlayOnMac (POM). This is an emulator using Wine that runs Windows apps on Mac (it does not install Windows, it just fakes the function calls and drivers).
3. Once installed, open the POM main window and press the gear near the top of the window labeled "Configure".
4. Create a new virtual drive with the "New" button in the bottom left. Select "32 bits windows installation", and give it any name. Wine might ask for something called Gecko, but just ignore this.
5. Select the virtual drive you just created from the sidebar on the left, and in the general section, you should see "wine version". Click the plus sign, and install Wine 19.0.0-cx (x86on64). I am using 19.0.0-cx.
   * Apparently newer versions of wine will cause Omori to throw an error since it drops some required functions.
   * Make sure the drive doesn't have "System" selected for Wine, but the one you downloaded. If the version you downloaded doesn't show up, remake the drive and it should prompt for the Wine version.
![wine version](https://i.imgur.com/9SvzRGq.png)

6. Navigate to root OMORI game folder. Go into OMORI.Build.8879120, and find the file Launch_OMORI.bat. Note that this file is for running the game on Windows, so we need to pass the key into the POM arguments.
   * Open this file with a text editor, the built-in one for Mac is TextEdit, and copy the key starting with two dashes, looks something like [--6bd...]. Without this, OMORI.exe will just open a black screen on startup.
7. Navigate back to the POM Configuration window, and click on the virtual drive again. Click "Make a new shortcut from this virtual drive", select Browse, then find and select the OMORI.exe file from the OMORI game folder in OMORI.Build.8879120. An icon of OMORI should appear under the virtual drive.
8. Click on it and paste the key you copied from the bat file into "Arguments". Your drive should now be set up properly, so you can close the config window and go back to POM window, and click on the OMORI icon and the play button "Run" in the top left.
   * Mac will throw a bunch of security warnings saying [something].dll cannot be opened because it is by an unidentified developer. You can bypass this by opening Mac System Preferences, Security & Privacy, and under "Allow apps downloaded from:" there should be a message saying what was blocked, and you can press open anyways. POM starts up OMORI in windowed mode. You can go to options in the OMORI main menu and change to fullscreen.
   * Config window should look something like this (ignore other drives):
![config window](https://i.imgur.com/oOeHOff.png)
