Made by mat1432 [Steam](https://steamcommunity.com/id/mat1432/) [GitHub](https://github.com/mat1432/Colonial_Partitioning)

The change logs are in English, so far any and all translations of the Change Logs were done via online websites:
* NONE of the Translators who Volunteered their time are at fault for any imperfections!

## 1.1.2b
* Bug Fix: Previous Owner Setting would change New Owner setting by mistake (my bad)

## 1.1.2
* Now uses Colonist icon instead of '\<CP\>' as prefix text
* Colony Core Settings: Renamed to 'New Owner Cores & Claims Setting'. *Or similar equivalent*
* Previous Owner Claims Settings: Renamed to 'Previous Owner Cores & Claims Setting'. *Or similar equivalent*
* Previous Owner Cores & Claims:
  * Added 4th option, 'Gain Full Cores & Claims' **Only Enabled by Cheats**
    * *If enabled: Colonies that were every a player will Gain Full Cores & Permanent Claims on all lost land.*
* Undo Partitioning:
  * Bug Fix: Could not give YOUR soverign lands to the subject specified.
  * Refactored Code: Slightly reduced the time it takes for the game to find eligible provinces, then confirms all required conditions in a second step.
    * *Still very laggy*

## 1.1.1c
* Bug fix: Cheat menus can now be opened mid game (properly)
  * They were fire_only_once, this does not allow them to be opened after already fired. (Thanks [url=https://steamcommunity.com/profiles/76561198256679997]Sirius[/url])
  * *This update will cause them to fire again on any active save game started before this update*

*Cheats Menu: 'event cpt.98'*
*Multiplayer Menu: 'event cpt.99'*

## 1.1.1b
* Bug Fix: Prevents 'Undo Partitioning' from processing provinces already owned by the recipient!

## 1.1.1
* Allow 'Undo Partitioning' Diplo Action on active players.
  * Reason: It only gives them provinces, I do not see the harm. Additionally this allows for some unforseen consequences to be undone without multiplayer savescum. (What this mod was made to avoid!)
  * *Other Players are still always protected from this action!*
* 'Undo Partitioning' now counts for the Multiplayer delay.
  * *Reason: It scans every province worldwide; It is more intensive than regular Partitioning!*
* Allow 'Undo Partitioning' when cheats are disabled.
  * *Testing Gameplay Balance (on you guys!); May be Reverted Later.*
* Minor Improvements to Player Protection descriptions, and the Player protection Settings menu.
* Added Tooltip for cheats menu cheats options, they list the features that will be enabled by cheats

1.1.0b
* Minor Refactoring of code
* Improved Documentation
* Credited myself for my code

1.1.0
* Added [GitHub Repository](https://github.com/mat1432/colonial_fixes/)
* Now licensed under the [GNU General Public License v3.0](https://github.com/mat1432/colonial_fixes/blob/main/LICENSE)
* Refactored Code with callable scripts and triggers for common cases to improve tooltips
* Fix Console flags editing mistakes regarding this mod's cheats
* Fixed descriptive tooltip for setting a colony as protected
* 'Reset ALL Colony Protections' now describes every colony which will lose protected status
* Addded Event pictures, will only show if you have DLC [Star and Crescent](https://store.steampowered.com/app/625171/Europa_Universalis_IV_Digital_Extreme_Edition_Upgrade_Pack/) (Completely Optional)

1.0.5d
* Undo Partitioning Diplomatic Action now fires a choice event where you can chose to set that colony as Protected.

1.0.5c
* Minor Fixes to German Translation (Credit to [Thylon](https://steamcommunity.com/id/thylon125/))

1.0.5b
* Fixed Protection & Player Protection mechanics for 'Undo Partitioning' Diplomatic Action

1.0.5
* Added 'Undo Partitioning' Diplomatic Action.
    * Note: Only works on colonies partitioned after this update!!!
    * Note: Uses the Tag of the colony in province flags, if you annex the colony or it changes to a formable: They will lose all recognition of partitioned lands
* Added Recursive Menus
* Improvements to localisation
    * Added German Translation (Credit to [Thylon](https://steamcommunity.com/id/thylon125/))
    * Fixed Player Protection settings tooltip
    * Fixed Typo
* Fixed ability to change startup settings through console commands:
    * Cheats: 'event cpt.98'
    * Multiplayer: 'event cpt.99'
    * NOTE: If specifying a County Tag: that country cannot be AI or the event will not fire.

1.0.4 (4 Updates)
* Fixed Ongoing Partitioning Warning
* Fixed Multiplayer Delay
* Fixed Multiplayer Protection
* Fixed bug where the mod thinks someone is partitioning but is in fact not
* Fixed bug Where provinces from previous partitions would sometimes be assigned to the core layout of the previous partitioning, not the current layout

1.0.3 (2 Updates)
* Improvements to localisation
    * Cleaned up Menus with walls of text
    * Corrected Typos
    * Fixed Missing Tooltips (Split Tooltips file into 3)
    * Adjusted wording on Tooltips, Options, & Descriptions
    * Improved my use of Colours to signify & identify Objects of Interest
* Cleaned Code
    * Trimmed all unique identifiers (Won't improve performance, but will make the code easier to read!!!)
    * Adjusted Logic to improve Readability (And Performance, but not by much)

1.0.2
* Trimmed some unnecessary code and comments
* Minor adjustments to localisation
* Fixed and re-added Multiplayer delay option (Also included hidden auto checks to ensure compatibility with any active save games)
* Fixed instant annex diplomatic action

1.0.1
* Added Thumbnail
* Removed Multiplayer optional delay; I did not understand had_global_flag triggers, I might re-add later if I fix it.

1.0.0
* Foundation of the mod
