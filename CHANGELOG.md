TBD - 2.3.0

* Bugfix: Removed extra closing parentheses `)` on all tokens and panels which caused macros to fail in MapTool 1.18.x ([#43](https://github.com/melek/Simple5e/issues/43)).
* Bugfix: Theme foreground and background are now saved in the libSettings properties.  New variable being used in CSS macro for background coloring ([#40](https://github.com/melek/Simple5e/issues/40)).
* Bugfix: Changed macro sizes to be 85px, 100px, or automatic to mitigate wrapping ([#37](https://github.com/melek/Simple5e/issues/37))
* Bugfix: #36, corrected links to go to the proper locations ([#36](https://github.com/melek/Simple5e/issues/36)).
* Tweak: Updated macro buttons with 'default' colors to have 'default' text for theme compatibility
* Tweak: Included link to Jmr3366 Lib:SpellLibrary and Lib:MonsterMaker
* Tweak: Reverted 'CHA' macro to work like other saving throw macros
* Tweak: Removed newlines in Standard Token macro tooltips using `[r: ...]` rolls to improve display
* Tweak: Reworked all macro button widths to a new, slightly wider standard

8/6/2020 - 2.2.1

* Tweak: The 'Validate Token' GM Macro no longer resets PassivePerception and PassiveInsight to preserve custom values for these properties ([#21](https://github.com/melek/Simple5e/issues/21)).
* Bugfix: The new 'Jack of All Trades' GM macro now updates the selected token's PassivePerception and PassiveInsight skills ([#21](https://github.com/melek/Simple5e/issues/21)).
* Bugfix: The 'Tweak Token' GM Macro now displays the raw property for AC, Speed, and InitiativeBonus and preserves formula values for these properties. Speed may still be reset to an integer. This will be most noticeable in that the AC formula will be properly preserved on new tokens, rather than being overwritten by a value. AC can still be replaces by a simple integer value if you so wish. It also preserves the updated InitiativeBonus from 'Jack of all Trades' ([#23](https://github.com/melek/Simple5e/issues/23)).
* Bugfix: The new 'Marked' Campaign macro now has a correct tooltip ([#22](https://github.com/melek/Simple5e/issues/22)). 
* Bugfix: Standard Token no longer comes with non-default 'Sheet' preferences ([#24](https://github.com/melek/Simple5e/issues/24)).
* Bugfix: Counters are now readable in the 'Sheet' macro frames when dark mode is enabled ([#25](https://github.com/melek/Simple5e/issues/25)).
* Meta Bugfix: Updated the changelog on the Simple5e Help token
* Meta Bugfix: Fixed the 2.x - 2.2.1 Update Token to be more accurate than prior versions

7/31/2020 - 2.2

* Bugfix: The 'Concentration' token macro now works when 'Immediately roll saving throw' is unchecked ([#19](https://github.com/melek/Simple5e/issues/19)).
* Bugfix: The 'Macro Seach and Replace' GM macro has been fixed to eliminate use of double-encoding and better handle Regex sensitive characters ([#14](https://github.com/melek/Simple5e/issues/14)).
* New Feature: The 'Create Action' button now has a drop down for SRD weapon templates. Using these templates automatically fills out the name, attack and damage attributes according to melee/ranged weapons accounting for finesse, and the damage code. Selecting a weapon template also adds that weapon's information to the attack roll's tooltip. Players can now also add their own tooltip notes during the wizard ([#18](https://github.com/melek/Simple5e/issues/18)).
* New Feature: A new 'Apply Jack of All Trades' macro is in the GM panel. To use, select the target token and click the GM macro. This feature automatically applies several complex macro edits which are hard to reverse, so use with care ([#20](https://github.com/melek/Simple5e/issues/20)).
* New Feature: 'Hexed' and 'Marked' campaign states have been added, with corresponding macros in the '4. Other States' Campaign panel group ([#8](https://github.com/melek/Simple5e/issues/8)).
* New Feature: Added campaign properties and states for compatibility with Illydth's Spell States ([#8](https://github.com/melek/Simple5e/issues/8)) Credit to Rogue Ronin and game-icons.net for the art on these compatibility states.
* Tweak: Reordered campaign states to make Death and AFK show up over other states ([#8](https://github.com/melek/Simple5e/issues/8)).
* Tweak: New campaign property 'libAuthor' added to encourage use by plugin developers ([#3](https://github.com/melek/Simple5e/issues/3)).
* Tweak: Added art credit to Nick Robles directly to the Standard Token GM Notes.
* Tweak: Added workarond logic to turn off log.info() debugging information from being enabled in 1.7.0, since a bug in that version prevents log.info() calls from working properly when called from the GM panel ([#15](https://github.com/melek/Simple5e/issues/15)). Affected macros:
  * Configure Token
  * Tweak Token
  * Validate Token
  * Convert 5e Monster Token
  * Macro Search and Replace
  * Create Action (GM and Campaign panel versions)
  * Custom Counters (GM panel Version)
 
5/14/2020 - 2.1

Note: A bug in MapTool prevents non-GMs from using 'Tweak Token' on newly created tokens. To workaround this, the player can double-click the token, hit 'OK' (no need to alter any settings), and then run 'Tweak Token' as normal.

* Bugfix/Improvement: The 'Invisibility' campaign macro has been refactored to let the GM secretly hide tokens without alerting players. The macro code should also be more clear and similar to other state macros ([#13](https://github.com/melek/Simple5e/issues/13)).
* Bugfix: 'Remove All' campaign macro refactored to properly remove Invisibility, retain Inspiration, and use `resetProperty` ([#5](https://github.com/melek/Simple5e/issues/5)).
* Tweak: The 'Dead' state is now a bit darker and less distracting ([#12](https://github.com/melek/Simple5e/issues/12)).
* Bugfix: 'Roll Initiative' campaign macro now only displays the roll tooltip to GMs to prevent players peeking at NPC initiative bonueses ([#11](https://github.com/melek/Simple5e/issues/11)).
* Bugfix: TempHP and MaxHP is now correctly accounted for in the 'Damage NPC' and 'Heal NPC' macros ([#10](https://github.com/melek/Simple5e/issues/10)).
* Bugfix: Players can no longer run 'Damage NPC' and 'Heal NPC' campaign macros on tokens they do not own, which allowed them to peek at HP ([#7](https://github.com/melek/Simple5e/issues/7)).
* Bugfix/Workaround: The Create Action macro now functions properly when run by players. It did not work due to a bug in MapTool where GM macros aren't considered 'Trusted' when invoked by non-GM clients ([#9](https://github.com/melek/Simple5e/issues/9)).
* Bugfix: Counter-adjusting macros created with 'Create Action' campaign/GM macro now correctly handle counters with maximum values, and their code has been improved ([#6](https://github.com/melek/Simple5e/issues/6)).
* Tweak: Several large tooltips were shortened to prevent them from obscuring macro buttons once tooltips are engaged ([#2](https://github.com/melek/Simple5e/issues/2)).
* Lib:Simple5eHelp Bugfix: Player Quickstart link from 'Setting up MapTool' article ([#1](https://github.com/melek/Simple5e/issues/1)).
   
5/4/2020 - 2.0
* New Feature: There is now a basic Character Sheet in the 'Adventuring' Macros. Yes!
   - Click on saving throw, skill, and ability checks to immediately roll them to chat.
   - Tweak Token and Configure Token are now accessible via the character sheet options panel.
   - This sheet has some basic accessibility options such as a dark mode and a font size toggle.
* New Feature: New Custom Counters system to track spells, ammunition, special abilities, and anything else. 
   - The system is built in JSON for GMs to plug into and learn.
   - Custom Counters can be configured to automatically reset on a long or short rest.
   - Custom Counters can be included in new action buttons.
* New Feature: Added a help system and basic tutorial in an optional Library Token. 
   - The first time a user loads the campaign file, a Welcome window will appear.
   - Whenever loading the campaign, users get a dismissible welcome message appropriate to their role (GM or Player) with a link to open the help system.
   - Explore the custom-built Lib:Simple5eHelp Library Token to read the articles and explore this new feature. It is designed to be customizable for your own needs.
* New Minor Feature: 'Healing' and 'Damage' macros now use two health bars:
   - Token Take/Heal Damage macros trigger an accurate health bar. 
   - Campaign Damage/Heal NPC macros trigger an approximate health bar that only shows HP at 75%, 50%, 25%, and 0%.
   - By default, all health bar are fully visible. MapTool lets you control who sees which health bars in the 'Campaign Properties &gt; Bars' dialog, as well as update their look and type.
* Major Improvement: 'Configure Token' and 'Tweak Token' have been overhauled with Class level properties, new pronouns and extra options.
   - Class levels now help set token HD. The old HD assignment system is still available to GMs in the 'Advanced' tab.
   - New 'Ze/Zir/Zirs' and custom pronoun options are available.
   - Some pages of the wizards have been condensed, clarified, and cleaned up.
   - Basic Token Sight options (normal and darkvision) are now assignable during configuration. 
* Major improvement: The 'Create Action' buttons have been combined into a single button that launched a wizard for new actions.
   - Designed to handle any combination of Attack roll, Damage roll, Save DC, Concentration, and Custom Counter use with some format options.
   - Attacks now alert users if they roll a natural 20.
* Major improvement: The 'Death Save' macro has been significantly improved and makes use of new Stable and Dying meta-conditions.
   - When not at 0 HP, the macro now prompts you to choose whether you want to roll anyway instead of requiring you to first set your HP to 0 and hit the button again.
   - These conditions should work with all token Heal/Damage/Rest macros. 
* Breaking Change: Class specific logic for Action Surges and Ki has been removed. 
   - Compatibility: If you used them, re-add 'Ki', 'MaxKi', 'ActionSurge', and/or 'MaxActionSurge' properties to the Basic token property list. 
   - Alternatively, update all uses of these properties with 'getProperty' and 'setProperty', as these work regardless of defined token properties.
   - You can also replace these trackers with new Custom Counters.
* New Minor Feature: Inspiration has been added to 'Other States' campaign macros. Inspiration is shown with a bright green-yellow dot in the top-right of the token.
* New Minor Feature: Away From Keyboard macro ('♪' / music note Token macro) is a compact macro to let others know when a player isn&#39;t present.
* New Minor Feature: 'Resize Skills' campaign macro lets you instantly swap a token&#39;s skill macros between 2 and 3 columns.
* New Minor Feature: Skills and saving throw tooltips now dynamically display proficiency and bonus.
* Improvement: The Concentration saving throw macro now prompts you rather than requiring a roll.
* Improvement: Saving throw macros have been tightened up to save significant panel space.
* Improvement: Macros and their output have been cleaned up and made more consistent across the framework in numerous small fixes. 
* Improvement: The GM panel now holds several core macros. Some are referenced from the Campaign panel.
* Improvement: Token Manage campaign macros have been moved to the bottom of the campaign panel and all except for the new 'Resize Skills' macro. 
* Improvement: 'Other States' campaign macros have been reorganized to better fit in the Campaign panel.
* Improvement: Basic dice macros now match the standard framework button width of 180px and have been added to the 'Adventuring' macros to save vertical space.
* Improvement: Death Save Failure and Success property labels now appear with a space in the hover stat sheet.
* Improvement: Some macros have been resized or abbreviated to accomodate some size differences on different operating systems.
* Improvement: 'Convert 5e Monster Token' macro now converts saving throw and skill proficiencies.
* Improvement: 'Macro Search & Replace' macro overhauled with a user input dialog and the option to select any macro property to search/replace within. As always, backup first and use with care.
* Tweak: Rearranged some 'Basic' Token Properties for more logical flow.
* Tweak: Removed the additional sample macros to simplify download.
* Tweak: Renamed the 'Staging Map' to from 'Melek&#39;s Simple 5e Staging Map' to '0.0 Simple 5e Library'. 
* Bugfix: 1d100 and 2d20 basic dice macros output similarly to single-dice macros and use img HTML tags with a 'width' set to reduce an occasional visual error.
* Bugfix: Some Basic Token Properties had minor calculation errors which could cause the stat sheet to display incorrectly. Fixed.
* Bugfix: The Dodge macro used an incorrect pronoun property. Fixed.
* Other small tweaks and fixes may have gone unrecorded.

11/2/2019 - 1.3
* Fixed Charisma based skill macros which were incorrectly using DexMod.
* Fixed Investigation skill macro which was incorrectly using the History proficiency.
* Fixed the sample Unarmed Strike DMG macro to correctly calculate 1 + StrMod damage instead of 1d4 + StrMod.
* New Feature: Added a new 'Macro Search & Replace' macro for GMs to mass-repair token macros across multiple tokens.
* New Feature: Updated Fighter properties to include Second Wind macro and added corresponding campaign properties and added Aid spell in 'Other States' to showcase TempMaxHP increases.
* New Feature: The '...' token macro now directly runs the 'Tweak Token' Campaign macro via a macro roll option, and  'Tweak Token' and 'Validate Token' are similarly called in the 'Configure Token' macro to reduce redundancy. This change means 'Tweak Token' ever only has to be updated in one place, and showcases a way to write one campaign macro and call it from multiple tokens.
* Tweak: Moved 5e Monster Token library to object layer and added an explanatory GM Note on object-layer tokens.
* Tweak: Added an explanatory GM Note to Changelog and Acknowledgments to explain the use of their text labels.
* Improvement: Improved 5e monster compatibility by adding a new token property to help check for converted tokens and hiding unhelpful Passive Insight and Passive Perception stats on mouse-over for unconverted 5e monster tokens.
* Improvement: Added numerous tooltips and explanatory comments to campaign macros.
* Improvement: Numerous small fixes and adjustments (mispellings, refactoring, macro positioning & coloring, etc.)
* Special thanks to Smash the Cookies on Discord for finding the skill and Unarmed Strike macro bugs!

9/23/2019 - 1.2
*Added properties for enhanced compatibility with bobifle&#39;s 5e monster tokens. Some of these token properties show up on the hover-statsheet.
*Added a 'Convert 5e Monster Token' macro to it possible to edit bobifle&#39;s 5e monster tokens with the other standard campaign macros without breaking anything.
*Updated 'Validate Token' and 'Configure Token' macros to work with converted 5e monster tokens.
*Made HP so only the owner(s) of the token could see it on the hover-statsheet.
*Fixed incorrect proficiency calculation.
*Fixed 'Short Rest' and 'Long Rest' token macros from erroring if ActionSurge or Ki property were empty while MaxActionSurge or MaxKi were set above 0.

8/28/2019 - 1.1
*Fixed bugs in some token macros.
*There is now a 'Validate Token' campaign macro that will reset many of the default properties if needed. If you are getting errors, try using this macro while selecting your token. This also runs when you use 'configure token'.
*Added bobifle&#39;s 5e monster library token to the file to make it ready for drop-in monsters. It is too good to pass up, and the implementation is very simple.

8/27/2019 - 1.0
* Initial Release
