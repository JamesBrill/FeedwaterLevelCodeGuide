# Feedwater Level Code Guide

While we're waiting for [Feedwater](https://jamesbrill.itch.io/feedwater) to get a proper level editor, it's possible to create and share levels by writing level codes. It's a bit painful, but it's all we've got until the level editor arrives. This guide explains the symbols you can use, as well as the format of the blocks.

# Anatomy of a Feedwater level

There are 4 blocks in a Feedwater level:
1. Level name: this must always be the first line in the level code
2. Level code: this is most items in the game, including walls. It can also include doors and wires. This block must start with `level` on its own line and finish with `endlevel` on its own line
3. (OPTIONAL) Doors code: Feedwater levels can have button-operated doors. These include a button connected to a door via a wire. You may want to overlay wires on top of other items in the level (e.g. walls), hence this is a separate layer. This block must start with `doors` on its own line and finish with `enddoors` on its own line
4. (OPTIONAL) Checkpoints: each one is written on its own line and has the following format: `checkpoint <topLeftX> <topLeftY> <bottomRightX> <bottomRightY> <respawnX> <respawnY>`. The first two pairs of coordinates define the region in which the checkpoint is activated; the last one defines where the player will respawn when they die. The top-left position on the level has coordinates (0, 0). The x-axis goes from left to right and the y-axis goes from top to bottom. This block must start with `checkpoints` on its own line and finish with `endcheckpoints` on its own line

# Rules

There is currently no validation on the level code submission, so you'll need to follow a few rules to make sure it's not broken:
1. Every line in the level code must have the same length
2. Every line in the doors code must have the same length
3. The doors code must have the same dimension as the levels code
4. There must be a player (represented by `P`)
5. There must be a level name and a level code
6. Each wire and button must be connected to a door

# Symbols

These are the symbols you can use in the level code and doors code:


## Player

`P`

<img width="110" alt="Screenshot 2022-12-31 at 15 48 37" src="https://user-images.githubusercontent.com/2140027/210148704-a15d99b8-5d47-4041-b4fc-51440436b9c8.png">

## Exit

`E`

<img width="99" alt="Screenshot 2022-12-31 at 15 49 14" src="https://user-images.githubusercontent.com/2140027/210148720-1d080638-f537-4d21-af90-34ec6d8e3f97.png">

## Empty space

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


