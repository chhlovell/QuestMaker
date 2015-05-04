# QuestMaker
API and Interface for basic roguelike game and editor


## Aims
-  A playable roguelike game with mechanics similar to HeroQuest
-  An editor that allows you to create any game possible from the ruleset


## Platform
- The game and editor will run on Chrome desktop
- All game data will be saved in JSON format
- The API will deal with all data getting, setting and modification
- The Interface will deal with all interaction, visuals and sound
- There will be a separate Interface for the game and the editor


## Classes
- **Campaign** <br> Player & Team info. Level list. Activities between levels
- **Level** <br> Map (2D array), Victory conditions. 
- **Floor** <br> Tile graphics
- **Wall** <br> Can be right or bottom of tile only. Even on activate
- **Trigger** <br> Map entry/exit. Trap. Map revealer. Event on enter/leave
- **Furniture** <br> One or more tiles grouped. Can contain Treasure
- **Creature** <br> Universal hero or monster
- **Equipment** <br> Held by creature or in Furniture. May be stacked. Event on activate
- **Spell** <br> Held by creature. Event on activate
- **Condition** <br> An ongoing effect on a creature
- **Treasure** <br> An event that can occur when searching for treasure


## Rule concepts
- The ruleset should be similar to HeroQuest but far more flexible
- No concept of rooms
- Can only search for treasure on a furniture item (eg. chest, bookcase) not rooms
- Search traps in visible area or limit of squares?
- Item (stack) limit per creature (Say 8 for a hero, 0 for most monsters), some - items can be stacked though, eg. coins up to 100 or potions
- All Equipment owned is immediately used. (eg. you cannot hold two items of same type, say two 'Left hand' items)
- Maps can be any shape or size (2D grid)
- Each Tile can have one creature, one trigger, one item of furniture and a right and bottom wall.
- Line of sight based on squares not rooms (this has implications for multi square objects like furniture)
- Is line of sight per player, per team or per creature?
- There is no difference between a hero and monster other than attribute values (eg. Can this creature leave the map? Can it reveal fog of war?, Can it carry equipment? etc..)
- Named special monsters are just different monster types that you only see once in a campaign
- Campaign defines max players, number of teams and level sequence
- Triggers (eg. traps, level exits) belong to a specific team(s) and can only be activated by that team
- Each level (map) defines entry and exit points
- Each level defines its own victory conditions






