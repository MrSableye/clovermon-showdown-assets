# Clovermon Showdown Assets
This is a central repository for sprites and audio related to [Clovermon Showdown](https://github.com/MrSableye/clovermon-showdown) and the [Clovermon Showdown Client](https://github.com/MrSableye/clovermon-showdown-client).

## Structure
### Directories
Each mod has a dedicated folder in the root of the repository like `clover/` and `clover-cap/`.

### `manifest.json`
Each mod directory requires a `manifest.json` file that defines the mod's expected assets.

```json
{
  "entityDirectories": [{
    "entities": [ // Entities are what the data in each directory represents, like Pokemon
      "pikachu",
      "charizard"
    ],
    "directories": [{ // Directories define the directories in which entity (Pokemon) data resides
      "extension": "png", // The expected extension of the file
      "required": true, // Whether a file for each entity is required
      "path": "sprites/gen3", // The relative path from the mod directory to where the files are stored
      "ignoredEntities": [ // Entities that might exist in other directories but should be ignored
        "pikachu"
      ]
    }]
  }]
}
```

## Contribution
Contributions should consist of new files and appropriate manifest updates. GitHub workflows will prevent pull requests from merging that do not contain all files required.