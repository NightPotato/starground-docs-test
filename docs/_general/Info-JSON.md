# Info JSON Schema
Mod Developers are required to include a JSON Schema that contains information about their mod within the packed version of their mod. Below is a explanation of the `info.json` file that is required in every mod.

### Example `info.json` File
```json
{
	"Format": 1,
	"Script": "res://AwesomeMod/loader.gd",
	"Data": {
		"ID": "bbg_templatemod_1",
		"DisplayName": "Awesome mod!",
		"ModVersion": "1.0",
		"Description": "A super awesome mod!",
		"GameVersions": ["0.9.0.0"],
		"Author": "Jesse Schramm",
		"Dependencies": [],
	}
}
```

### Important Fields within `info.json`
> Script | This is the entry-point of the mod and is loaded automatically by the Mod Loader.

> Data.ID | This is the identifier for your mod. Must be Unique.

> Data.DisplayName | Name of your mod.

> Data.ModVersion | The current version of your mod.

> Data.Description | A Description of your mod and what it does.

> Data.GameVersions | An Array of supported Game Versions that your mod works on.

> Data.Author | The Author of the mod. (You)

> Data.Dependencies | This is not yet used, hopefully will be implemented soon to control what mods have a dependency.