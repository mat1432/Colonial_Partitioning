### Made by mat1432 (Steam) https://steamcommunity.com/id/mat1432/
### https://github.com/mat1432/Colonial_Partitioning
### Though the project title is 'Colonial_Partitioning' the Steam download has the mod name 'colonial_fixes' as a relic from this mod's early development!

[b]1.34.5 ; This Mod Does Not Need to be Updated![/b]

This mod allows you to strip away all provinces any of your colonies has, that is in a colony charter outside their capital charter!
No more Brazil and Colombia completely colonizing Peru on an ironman save, you can just strip the lands to your possession and then unpause to create Colonial Peru!

This Mod is completely dynamic and should be compatible with just about every major map mod! Yes, it works on Random New Worlds, Anbennar, BT, Ante Bellum, etc.

This is a cheat mod, but I've included some settings so that it's less cheaty and more like gaming the system.


[h2]This Mod is:[/h2]
[b]NOT Achievement Compatible! (Modifies the checksum)[/b]
But will work on an Ironman save.


An event will pop at game start to specify if you want to enable cheaty options or not.

[h1]Features List:[/h1]
[h2]Diplomatic Actions:[/h2]
-> Can Instant Annex any of your colonies (requires enabling cheats at game start, or 'normal' on non-Ironman saves)
-> You can specifically set colonies to be protected from partitioning / instant annex
-> You can undo the partitioning of a colony (Only works on or after update 1.0.5)
- Will only undo lands that are your sovering provinces (Will NOT transfer lands owned by tributaries)

[h2]Partitioning:[/h2]
-> You can specify to skip any colonies that have not yet cored all provinces to at least a territory, (Uncored land does not form colonies)
-> You can specify to ignore the colony coring progress and just full core everything (not allowed on Ironman saves, and disabled by 'No Cheats' option at game start)

[h3]Undo Partitioning:[/h3]
-> Accessed by 'Undo Partitioning' Diplomatic Action under Influence Category
-> Will only transfer your soverign or colonial lands that were taken in a previous partitioning to the current colony.
-> Follows the same logic as regular partitioning, and all nations whose lands are taken from during this process will be flagged as partitioned.
-> Will only work on colonies partitioned after Update 1.0.5.
-> [b]The Undo process cannot affect active Players![/b]

[h2]Multiplayer Safety:[/h2]
-> By default, any colonies that were ever a player will be protected (Can be disabled)
-> Any colonies that were ever a player, if partitioned, will Always keep their cores (Including Territorial Cores) & gain Permanent claims on all lost land.

[h2]Install and Uninstall Compatibility:[/h2]
-> Forwards Compatability:
- The mod doesn't edit or replace any files, only adds files. It should be forwards compatible with every future update!
-> Backwards Compatibility:
- Same as above... The mod is compatible with prior versions, though don't go too far back because I'm not sure how far it is compatible with.
-> Save Compatibility:
- No need to worry about uninstalling, the mod only uses country, province and global flags which do not cause any save game damage upon uninstall.
You can safely use on any active save game and remove later if you wish.

[h2]AI[/h2]
[b]The AI will never use this mod or its features![/b]
If a game is saved with any menu open, the AI will close it without changes.
If a setup menu is given to the AI through save trickery, the AI will pick 'Normal' for the Cheats Menu and 'Singleplayer' for the MP menu.


[h1]Supported Languages:[/h1]
[list]
    [*]English by [url=https://steamcommunity.com/id/mat1432/]mat1432[/url]
    [*]German by [url=https://steamcommunity.com/id/thylon125/]Thylon[/url]
[/list]

[url=https://github.com/mat1432/colonial_fixes/]GitHub[/url]
Licensed under the [url=https://github.com/mat1432/colonial_fixes/blob/main/LICENSE]GNU General Public License v3.0[/url]

The change logs are in English, so far any and all translations of the Change Logs were done via online websites:
-> NONE of the Translators who Volunteered their time are at fault for any imperfections!

Most of the code is for compatibility, fine-tuning, and ease of use.
At its core the code to partition colonies is like this:
[code]colonial_partition = { # decision
    potential = {
        ai = no
        any_subject_country = { is_colonial_nation = yes }
    }
    allow = { always = yes }
    effect = {
        hidden_effect = {
            every_subject_country = {
                limit = { is_colonial_nation = yes }
                every_owned_province = {
                    limit = {
                        NOT = { colonial_region = capital }
                    }
                    if = {
                        limit = { is_core = prev }
                        remove_core = prev
                    }
                    add_core = root
                    cede_province = root
                }
            }
        }
    }
}[/code]
