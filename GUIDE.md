# Feedwater Level Code Guide

While we're waiting for [Feedwater](https://jamesbrill.itch.io/feedwater) to get a proper level editor, it's possible to create and share levels by writing level codes. It's a bit painful, but it's all we've got until the level editor arrives. This guide explains the symbols you can use, as well as the format of the blocks.

# Anatomy of a Feedwater level

There are 4 blocks in a Feedwater level:
1. Level name: this must always be the first line in the level code
2. Level code: this is most items in the game, including walls. It can also include doors and wires. This block must start with `level` on its own line and finish with `endlevel` on its own line
3. (OPTIONAL) Doors: Feedwater levels can have button-operated doors. These include a button connected to a door via a wire. You may want to overlay wires on top of other items in the level (e.g. walls), hence this is a separate layer. This block must start with `doors` on its own line and finish with `enddoors` on its own line
4. (OPTIONAL) Checkpoints: each one is written on its own line and has the following format: `checkpoint <topLeftX> <topLeftY> <bottomRightX> <bottomRightY> <respawnX> <respawnY>`. The first two pairs of coordinates define the region in which the checkpoint is activated; the last one defines where the player will respawn when they die. The top-left position on the level has coordinates (0, 0). The x-axis goes from left to right and the y-axis goes from top to bottom. This block must start with `checkpoints` on its own line and finish with `endcheckpoints` on its own line

# Rules

There is currently no validation on the level code submission, so you'll need to follow a few rules to make sure it's not broken:
1. Every line in the level code must have the same length
2. Every line in the doors code must have the same length
3. The doors code must have the same dimension as the levels code
4. There must be a player (represented by `P`)
5. There must be a level name and a level code
