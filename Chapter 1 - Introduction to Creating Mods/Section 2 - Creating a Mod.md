# Introduction

Before diving into coding, it's crucial to understand how to create a mod that the game can load. This chapter will guide you through creating a basic resource replacement mod, such as a sprite replacement.

# Creating a Mod

The process of creating a mod is very straightforward. 

1. **Navigate to the mods folder.** For Steam users, this is typically located at `C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\mods`.
2. **Create a new folder.** Give it a clear and descriptive name to easily identify your mod.
3. **Restart the game if it's running.** The game only loads new mods upon startup.
4. **Open the mods menu.** You should see your newly created mod listed.
5. **Congratulations!** You made your first mod! Right now, it doesn't do anything. However, this will soon change.

# Enabling the Debug Console

The debug console is an invaluable tool for modders, allowing you to reload mods, spawn items, and much more. To check if it's enabled, start a run and press the `~` key. If the console appears, you're good to go. Otherwise, follow these steps:

1. **Close the game.** This is important to prevent your changes from being overwritten.
2. **Open the `options.ini`** file. This is usually found in `C:\Users\%username%\Documents\My Games\Binding of Isaac Repentance`.
3. **Locate the line `EnableDebugConsole=0` and change it to `EnableDebugConsole=1`.**
4. **Save the file and launch the game.** The  debug console will now be accessible.

5. Close the game. This is important as if you were to modify `options.ini` while the game is running, your changes will be overridden. 
6. Open the `options.ini` file. It is typically found in `C:\Users\%username%\Documents\My Games\Binding of Isaac Repentance`.
7. Option the `options.ini` file and look for a line that says `EnableDebugConsole=0`. Change it to `EnableDebugConsole=1`.
8. Save the file and launch the game. The debug console will now work.

# Creating a Resource Replacement Mod

Replacing existing resources with your own is very simple. Let's replace The Sad Onion item sprite as an example:

1. **Create your sprite.** You can create your own or use an [already existing sprite from Bajongo.](https://i.imgur.com/S3jHjdt.png)

>⚠️ **Warning**
> Save your sprite as a **.png file with a 32-bit depth.** Otherwise, it won't display correctly in-game.

2. **Locate the original sprite.** The game's resources are stored in the "resources" and "resources-3" folders within the game directory (`C:\Program Files (x86)\Steam\steamapps\common\The Binding of Isaac Rebirth\` for Steam users). "resources-dlc3" contains Repentance-specific resources, while "resources" contains everything else. Since The Sad Onion predates Repentance, its sprite resides in "resources". 
  * Navigate through "resources" > "gfx" > "items" > "collectibles". You'll find the Sad Onion sprite named "collectibles_001_thesadonion.png". Remember its location and name.

3. **Mirror the folder structure in your mod.**
 * Create a "resources" folder within your mod folder.
 * Inside "resources", create a "gfx" folder.
 * Inside "gfx", create an "items" folder.
 * Inside "items", create a "collectibles" folder.
 * Place your new Sad Onion sprite inside the "collectibles" folder and name it "collectibles_001_thesadonion.png".

4. **Restart the game if it's running.**

5. **Spawn the Sad Onion pedestal using the debug console command: `spawn 5.100.1`**
   
Viola! You created your first resprite mod.

> ℹ️ **Troubleshooting**
> If your new sprite doesn't appear, double-check the folder structure and filenames for accuracy (remember, they're case-sensitive!). Another mod might also be overriding your sprite, so try disabling conflicting mods.

# Replacing Other Resources

The same process applies to replacing other sprites, music, sound effects, and animations. The only difference would be the file type of your new resource and the folder structure you are mirroring.

> **⚠️ Warning**
> If you are trying to add your own sound, sound effects require 32-bit encoding. Otherwise, they will sound like extremely loud static in-game and hurt your ears. Ouch!

# More on the Debug Console

If you would like to learn more about the Debug Console and the commands it offers, the Isaac wiki has a [page covering it.](https://bindingofisaacrebirth.fandom.com/wiki/Debug_Console). Some commands will be covered in-depth in later sections.