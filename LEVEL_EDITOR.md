# Feedwater Level Editor

Feedwater now has a basic tool for building custom levels. This is what it currently looks like when editing a level:

<img width="962" alt="Screenshot 2023-09-04 at 20 56 45" src="https://github.com/JamesBrill/FeedwaterLevelCodeGuide/assets/2140027/13c5775e-4d08-4c93-b1e0-f9ff913e7048">

# Current limitations

* The editor uses a 100x100 grid, so larger levels cannot be made. Smaller levels loaded into the editor will be fit into the top-left corner
* Only one level is saved at any one time. This level is cleared whenever loading a level into the editor from a code via Edit Level. Therefore, it's a good idea to paste your level codes into your own files for safe-keeping. Better level storage support is coming!
* There's a lot of quality-of-life features missing like undo, clear, line-drawing, etc. These will come in time

# How to move around the level editor grid

There are three ways of doing this:
1. Arrow keys
2. Drag the right mouse button around to pan
3. Hover your mouse at the edge of the level editor grid and it will start panning after a short delay

# How to zoom in and out of the level editor grid

Simply use the mouse scroll wheel.

# How to paint a tile

You can select tiles from the palette on the left by clicking on them. Alternatively, you can select them using their hotkeys. The hotkey for the selected tile is displayed under the palette when you click on it, so it's possible to learn the hotkeys from the editor.

Once a tile is selected, you can paint it on the grid. Note that only one Spawn Point can be placed.

# How to create a new level

From the main menu, click Custom Levels and then Load Level. In the code box, paste the following:
```
New Level
level
endlevel
```

(note that this will clear any saved level!) Click Edit Level.

# How to load a level from a code

Maybe you want to reload a code you saved in a file or edit someone else's level from Discord.

From the main menu, click Custom Levels and then Load Level. In the code box, paste the level code.

(note that this will clear any saved level!) Click Edit Level.

# How to load the saved level

From the main menu, click Custom Levels and then Build Level.

# How to save your level

The level loaded in the level editor will automatically save every 10 seconds, when you test it, and when you view the level code.

# How to test your level

While editing, click Play Level. When you're done testing, hit Backspace or Escape on your keyboard to return to the editor.

# How to share your level with others

I encourage you to share your creations on Discord! From the editor, click Share Level Code and copy the level code from the code box (this does not work in full-screen) into a text file. Then share the file on the [#share-your-level](https://discord.com/channels/1001578650522636420/1071058347618471956) channel.

By default, the level code is at the full 100x100 grid size - this is intended for reloading levels into the editor to ensure all items are in the same position relative to the level borders. However, if you just want others to play the level and give them the smallest possible code, click Minified Code. You can toggle it back again if needed.

# How to add checkpoints to your level

For now, you'll still need to add checkpoints to your level code manually as per [this guide](https://github.com/JamesBrill/FeedwaterLevelCodeGuide/blob/main/GUIDE.md).
