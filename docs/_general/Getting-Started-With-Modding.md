Thanks for being interested in wanting to mod Starground! This wiki will go over the requirements and basics of setting up your Godot project to create a mod for the game.

## Requirements
1. You must use [Godot version 4.3](https://godotengine.org/download/windows/).
2. [Understand what you can & can't create with a mod!](_general/what-is-possible.md)
3. Basic understanding of Godot.

## Modding
Modding is pretty flexible, since it's done through Godot. This allows you to do all sorts of things, like:
* Adding new buildings, items, effects, and more
* Modifying base-game assets (images, sounds, scripts, etc.)
* Texture packs that just replace images or sounds
* And pretty much anything else you can think of!

Modding is done the same way as regular game development in Godot. You can add scenes, code, and images into your project in the usual way.

## Integrating Modded Content
To integrate your content into the game, it's recommended to do this through the `ModAPI` class. This is a helper class that integrates your content in a way that is safe alongside other mods. Anything you do through the `ModAPI` class should rarely ever have conflicts with other mods (as long as IDs and asset names are different).

### Adding or Replacing Content
Inside of `info.json`, you can point to an initial script to load within the res:// directory. This script will be ran once when your mod is initiated. This is the perfect place to use functions like `add_building_entry()` in order to integrate your modded content in. Examples of how to do this, and other related modding functions can be seen in the project in templates.

In order to replace base-game assets, you only need to name them the same thing in the same location. For example, to replace the collector, you can create the Sprites folder and name your new sprite collector.png. This works the same way with sounds and any other assets.

## Exporting
When you've built your mod, exporting is pretty straight forward, but there are a few things to be aware of.

First you need to build an export preset in the export tab under Project. Under scripts inside of your export preset, you need to set GDScript Export Mode to Text (easier debugging). This is so that Starground can scan your mod for malicious code.

Once your export settings are configured properly, export it as a ZIP (not a pck!). Do this by manually selecting ZIP file on the bottom right. Name your .zip, and you're good to go!
