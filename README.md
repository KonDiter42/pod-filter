# wallow's Loot Filter for Path of Diablo

## Overview
A loot filter that tries to keep the original Diablo II style while displaying useful details.

## Sample Screenshots
![ground](https://user-images.githubusercontent.com/81270285/122657624-4d93c800-d133-11eb-9a52-5209e18f0e46.png)
![chat](https://user-images.githubusercontent.com/81270285/122657628-54223f80-d133-11eb-86f9-670d69cc5952.png)

## Features
- Shows the item names next to unique and set items while they're unid
- Shows the # of sockets for items
- Shows the %ED and %-REQ for superior items
- Shows the % All Resist for Paladin shields
- Shows useful skills for scepters, claws, wands, and orbs
- Shows an indicator for ethereal items
- Colored symbols added next to some items to make them stand out more
- Names for gems and potions are shortened by making them follow a number format instead

## Presets
There are 3 presets to choose from depending on your progress in the game.
1. wallow-1 - Recommended while you get your first character ready for farming in hell difficulty.
2. wallow-2 - Once you're ready to start mfing in hell difficulty, I recommend switching to this one.
3. wallow-3 - A stricter version of preset #2, less items will show up on the ground and in your chat notifications.

I suggest having a look at the README files for each preset for details on what will be displayed on the ground and in the chat notifications.

## README Files
Check out the links below to find out what items will be displayed on the ground and in the chat notifications for each preset.

[wallow-1](https://github.com/wallowlol/pod-filter/tree/main/wallow-1)


[wallow-2](https://github.com/wallowlol/pod-filter/tree/main/wallow-2)


[wallow-3](https://github.com/wallowlol/pod-filter/tree/main/wallow-3)

## Download Links
Save these files to the "filter" folder located in your Path of Diablo folder.

You can do this by right-clicking the links below and selecting "Save link as...". 

[wallow-1](https://raw.githubusercontent.com/wallowlol/pod-filter/main/wallow-1/wallow-1.filter)


[wallow-2](https://raw.githubusercontent.com/wallowlol/pod-filter/main/wallow-2/wallow-2.filter)


[wallow-3](https://raw.githubusercontent.com/wallowlol/pod-filter/main/wallow-3/wallow-3.filter)

## How to Edit This Loot Filter
Before you start editing/customizing a preset, make a copy of it and name it something else. This prevents auto-updates (if they're enabled) from overwriting your edits. It's also good to keep the default preset so you can compare your edited version to it.

Example: Making a copy of "wallow-3" and naming it to "wallow-3-custom".

I'll explain two simple edits that are really easy to do.
1. Show/hide items on the ground
2. Show/hide items from showing up in your chat notifications

### 1. Show/Hide Items on the Ground
- Find the item you want to edit
- Add "//" to the beginning to hide it, remove "//" from the beginning to show it
- Example: Magic Large Charms from wallow-3 (showing by default, but you want to hide it)
  - Current:
    - ItemDisplay[MAG cm2 !ID]: %RED%@ %BLUE%%NAME% %RED%@
  - Edited so it no longer shows on the ground:
    - //ItemDisplay[MAG cm2 !ID]: %RED%@ %BLUE%%NAME% %RED%@

### 2. Show/Hide Items From Showing Up in Your Chat Notifications
- Find the item you want to edit
- Add "%NOTIFY-COLOR%" to the beginning of the text after the colon to show it, remove "%NOTIFY-COLOR%" to hide it
- Check the [loot filter wiki](https://pathofdiablo.com/wiki/index.php?title=Loot_Filtration_Codes) to see which colors are supported (if you want to change it)
- Example: IK Armor from wallow-3 (showing by default, you want it to only show on the ground but hide it from chat)
  - Current:
    - ItemDisplay[SET !ID uar]: %NOTIFY-GREEN%%NAME% %RED%(Immortal King's Soul Cage)
  - Edited so it no longer shows in the chat:
    - ItemDisplay[SET !ID uar]: %NAME% %RED%(Immortal King's Soul Cage)
