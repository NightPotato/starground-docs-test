
## Game Version
Mods can support multiple versions of the base game as long as they are still compatible. To see your current game version, take a look at the number on the bottom of the screen. The version should be a number without any letters (E.x 0.9.0.0, 0.8.3.0).

## Important Notes
 * [Restricted Classes/Namespaces](_scripting/Restricted-Namespace.md)
 * [Info.json Explained](_general/info-JSON.md)

## Tips
1. You should avoid replacing base-game scenes and code as little as possible. Every time you modify something in vanilla Starground, you run the risk of conflicting with other mods. You should always use the ModAPI script for adding your modded content into the game in the proper way.
2. Mods can be client side or server side. As long as you don't need any networking, you can make mods that work on vanilla servers.