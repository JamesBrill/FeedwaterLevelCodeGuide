# Feedwater Level Code Guide

While we're waiting for [Feedwater](https://jamesbrill.itch.io/feedwater) to get a proper level editor, it's possible to create and share levels by writing level codes. It's a bit painful, but it's all we've got until the level editor arrives. This guide explains the symbols you can use, as well as the format of the level code blocks.

Please share your levels on Discord [here](https://discord.com/channels/1001578650522636420/1058777284514943057) and look out for creations from other players too.

# How to play a custom level

* Open the game [here](https://jamesbrill.itch.io/feedwater)
* Click Custom Levels
* Paste your code into the text box
* Click Play Level

# Anatomy of a Feedwater level

There are 4 blocks in a Feedwater level:
1. Level name: this must always be the first line
2. Level code: this is most items in the game, including walls. It can also include doors and wires, though it's recommended you put them in the doors code. This block must start with `level` on its own line and finish with `endlevel` on its own line
3. (OPTIONAL) Doors code: Feedwater levels can have button-operated doors. These include a button connected to a door via a wire. You may want to overlay wires on top of other items in the level (e.g. walls), hence this is a separate layer that is placed on top of the level code layer. This block must start with `doors` on its own line and finish with `enddoors` on its own line. It can _only_ contain buttons, wires, and doors - anything else is ignored
4. (OPTIONAL) Checkpoints: each one is written on its own line and has the following format: `checkpoint <topLeftX> <topLeftY> <bottomRightX> <bottomRightY> <respawnX> <respawnY>`. The first two pairs of coordinates define the region in which the checkpoint is activated; the last one defines where the player will respawn when they die. The top-left position on the level has coordinates (0, 0). The x-axis goes from left to right and the y-axis goes from top to bottom. This block must start with `checkpoints` on its own line and finish with `endcheckpoints` on its own line


# Example

```
LEVEL NAME GOES HERE
level
XXXXXXXXXXXXXX]]]]]]]]]]uX
XXXXXXXXXXXXXXnXXXXXXXXXuX
XXXXXXXXXXXXXXnXXXXXXXXXuX
XXXXXXX....XXXnXXXXXXXX...
XXv.M......M<XnXXXXXXXX...
XX.XXX....XX.Xn[[[[[XXXXuX
...........X.XXXXXXnXX..v.
.......O......XXXXXnXX....
...XXXXXX..O..XXXXXnXX^.D^
XXDDDDD>..O...S]]]]nXX^D^.
XXXXXXXXX.....XXXXXXX.D...
X.......O.....XXXXXXX.^D..
X....O.......XXXXXXX...^D^
X......P...X.XXXXXXX.....D
XX.......XXX.XXXXXXX....D^
XX>.......M.^XXXXXXX...D^.
XXXXXXX..XXXXXXXXXXX..D...
XXXXXXX...XXXXXXXXXXXD^...
XXXXXXX...XXXXXXXXXXX^D^..
XXXXXXX....XXXXXXXXXXE^D^.
XXXXXXXX...XXXXXXXXXXXXXD.
XXXXXXXXXXXXXXXXXXXXXXXX^D
XXXXXXXXXXXXXXXXXXXXXXXXX^
endlevel
doors
..........................
..........................
..........................
..........N...............
..........|...............
..'.......|.'.............
.{+-------+-J.............
.rJ.......|...............
.|........|...............
.|......(7|...............
.|.......||...............
.U.......||...............
.........||...............
.{-------++-7.............
.........||.,.............
...(-----+J...............
.........|................
.........|................
.........|................
.........|................
.........U................
..........................
..........................
..........................
enddoors
checkpoints
checkpoint 23 3 25 4 24 3
endcheckpoints
```

# Rules

There is currently no validation on the level code submission, so you'll need to follow a few rules to make sure it's not broken:
1. Every line in the level code must have the same length
2. Every line in the doors code must have the same length
3. The doors code must have the same dimension as the levels code
4. There must be a player (represented by `P`)
5. There must be a level name and a level code
6. Each wire and button must be connected to a door

# Level Symbols

These are the symbols you can use in the level code:

## Player

`P`

<img width="110" alt="Screenshot 2022-12-31 at 15 48 37" src="https://user-images.githubusercontent.com/2140027/210148704-a15d99b8-5d47-4041-b4fc-51440436b9c8.png">

## Exit

`E`

<img width="99" alt="Screenshot 2022-12-31 at 15 49 14" src="https://user-images.githubusercontent.com/2140027/210148720-1d080638-f537-4d21-af90-34ec6d8e3f97.png">

## Empty Space

This can be anything, but I recommend you use `.` to make them easier to see.

## Wall

`X`

<img width="61" alt="Screenshot 2022-12-31 at 15 28 25" src="https://user-images.githubusercontent.com/2140027/210142847-e197d446-c317-4e1e-898f-13ad539a915d.png">

## Left Arrow

`<`

<img width="95" alt="Screenshot 2022-12-31 at 15 29 07" src="https://user-images.githubusercontent.com/2140027/210143157-cb0eadbb-4baf-4e41-a3ca-4e138a14474d.png">

## Right Arrow

`>`

<img width="97" alt="Screenshot 2022-12-31 at 15 29 23" src="https://user-images.githubusercontent.com/2140027/210143273-f43d03c7-1bff-4a7d-9b4b-ef465fd350e1.png">

## Up Arrow

`^`

<img width="97" alt="Screenshot 2022-12-31 at 15 41 21" src="https://user-images.githubusercontent.com/2140027/210147988-d42803da-bf39-4552-a9eb-941612780732.png">

## Down Arrow

`v`

<img width="96" alt="Screenshot 2022-12-31 at 15 41 38" src="https://user-images.githubusercontent.com/2140027/210148073-0ed56786-9303-4c8b-9c7f-fa51980898ad.png">

## Steel Crate

`S`

<img width="96" alt="Screenshot 2022-12-31 at 15 42 06" src="https://user-images.githubusercontent.com/2140027/210148251-bf963068-7ee6-4865-84fc-374020b0a23b.png">

## Ball/Boulder

`O`

<img width="96" alt="Screenshot 2022-12-31 at 15 42 23" src="https://user-images.githubusercontent.com/2140027/210148370-ff0a18d5-b5df-4c8c-bee0-940b6ff451df.png">

## Dynamite

`D`

<img width="95" alt="Screenshot 2022-12-31 at 15 42 42" src="https://user-images.githubusercontent.com/2140027/210148501-0dee60c9-ca66-4281-b9d0-e8768d8e59a9.png">

## Spike

`M`

<img width="98" alt="Screenshot 2022-12-31 at 15 44 16" src="https://user-images.githubusercontent.com/2140027/210148557-b4fd1a05-3132-4db5-94a6-61eb8ef5e5bd.png">

## Left Conveyor Belt

`[`

<img width="103" alt="Screenshot 2022-12-31 at 15 44 53" src="https://user-images.githubusercontent.com/2140027/210148582-39da2183-b6e3-47b8-9799-756918af9980.png">

## Right Conveyor Belt

`]`

<img width="101" alt="Screenshot 2022-12-31 at 15 45 14" src="https://user-images.githubusercontent.com/2140027/210148592-6f0cc978-bb60-4182-b665-d782663860b5.png">

## Up Conveyor Belt

`n`

<img width="96" alt="Screenshot 2022-12-31 at 15 45 44" src="https://user-images.githubusercontent.com/2140027/210148612-c2961edd-2395-4beb-bd36-502461eb6efe.png">

## Down Conveyor Belt

`u`

<img width="94" alt="Screenshot 2022-12-31 at 15 46 10" src="https://user-images.githubusercontent.com/2140027/210148625-58afb6b8-cd21-4c3a-a669-ea4a88dae0a0.png">

## Toxic Waste

`T`

<img width="103" alt="Screenshot 2022-12-31 at 15 47 33" src="https://user-images.githubusercontent.com/2140027/210148677-670b2e6f-631f-401f-91b2-51366c112be3.png">

## Secret

`*`

<img width="148" alt="Screenshot 2022-12-31 at 15 49 52" src="https://user-images.githubusercontent.com/2140027/210148745-587a11ee-9444-40a3-bdf3-ef4e67c42e65.png">

# Door Symbols

Below are the door symbols you can use in either the level code or the doors code to connect buttons to doors. Remember, doors must be connected to a button via an unbroken wire to function.

## Left Button

`{`

<img width="96" alt="Screenshot 2022-12-31 at 15 52 14" src="https://user-images.githubusercontent.com/2140027/210148822-2a67e703-68c8-4d09-836e-0dd65969674d.png">

## Right Button

`}`

<img width="100" alt="Screenshot 2022-12-31 at 15 52 46" src="https://user-images.githubusercontent.com/2140027/210148834-ce48133a-9285-4bf7-9d96-205c9a0b90c1.png">

## Up Button

`N`

<img width="99" alt="Screenshot 2022-12-31 at 15 53 13" src="https://user-images.githubusercontent.com/2140027/210148841-998078fd-5599-46ed-b269-a62d62aac0c2.png">

## Down Button

`U`

<img width="100" alt="Screenshot 2022-12-31 at 15 53 36" src="https://user-images.githubusercontent.com/2140027/210148855-de008a16-398d-46d9-9459-2838e69a6ddf.png">

## Left Door

`(`

<img width="100" alt="Screenshot 2022-12-31 at 15 54 04" src="https://user-images.githubusercontent.com/2140027/210148864-0882b6c9-a50b-427d-a7e3-26f166c42040.png">

## Right Door

`)`

<img width="98" alt="Screenshot 2022-12-31 at 15 54 21" src="https://user-images.githubusercontent.com/2140027/210148871-48da4186-6367-49d4-b9eb-acaa42ed5915.png">


## Up Door

`'`

<img width="99" alt="Screenshot 2022-12-31 at 15 54 44" src="https://user-images.githubusercontent.com/2140027/210148875-bd0c0ea1-b436-444a-9df3-6e3be30c65d4.png">


## Down Door

`,`

<img width="100" alt="Screenshot 2022-12-31 at 15 54 59" src="https://user-images.githubusercontent.com/2140027/210148884-8cff5b57-ff24-45d1-ac4b-a22e25e9128c.png">

## Vertical Wire

`|`

<img width="97" alt="Screenshot 2022-12-31 at 15 56 25" src="https://user-images.githubusercontent.com/2140027/210148911-7ed8ea93-1df5-4ca2-a891-a6f04f55912d.png">

## Horizontal Wire

`-`

<img width="99" alt="Screenshot 2022-12-31 at 15 56 44" src="https://user-images.githubusercontent.com/2140027/210148917-f5faf6f8-5226-4b63-9acb-5cf41e1b4a8c.png">

## Cross Wire

`+`

<img width="99" alt="Screenshot 2022-12-31 at 15 59 58" src="https://user-images.githubusercontent.com/2140027/210149034-a1878bac-6581-47f5-bdbf-5f1cdf3c8877.png">

## Bottom Left Wire

`7`

<img width="98" alt="Screenshot 2022-12-31 at 16 00 28" src="https://user-images.githubusercontent.com/2140027/210149049-93b58ac4-165f-47c7-b2d9-b83d7e384f72.png">

## Bottom Right Wire

`r`

<img width="98" alt="Screenshot 2022-12-31 at 16 00 46" src="https://user-images.githubusercontent.com/2140027/210149056-a527c695-5797-43e2-8ebc-9bfc37429d26.png">


## Top Left Wire

`J`

<img width="99" alt="Screenshot 2022-12-31 at 16 01 06" src="https://user-images.githubusercontent.com/2140027/210149071-7bce3fcf-1b3d-4ef6-8694-4edabc698239.png">

## Top Right Wire

`L`

<img width="100" alt="Screenshot 2022-12-31 at 16 01 26" src="https://user-images.githubusercontent.com/2140027/210149082-f00b563f-1f17-4e2b-855e-4fee11358631.png">

