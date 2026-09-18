# Game Structure

*By Rapunzilla*

## How It Works

Tiny Glade is developed in **Rust** using the [Bevy Engine](https://bevyengine.org/).

Music and sound are managed using **FMOD** ([FMOD Documentation](https://www.fmod.com/docs/2.02/api/studio-api.html)), which allows the game to use dynamic and adaptive soundscapes.

## Game Files

The main executable is `TinyGlade.exe`. This binary contains the game's compiled Rust code.

### `assets` Folder

The `assets` folder contains many of the resources used by the game. These are organised into several subdirectories:

- **`Audio/`** — Contains the game's music and sound effects. Audio is stored in FMOD `.bank` files. These can be [edited using community tools](../modding-tools/sound-editing.md).

- **`Meshes/`** — Contains many of the game's built-in **3D meshes**. Assets are organised into subfolders according to their purpose, including decorations and clutter.

    !!! note
        These are the game's built-in mesh assets. Clutter added through Tiny Glade's official modding and Steam Workshop support uses `.glb` files and follows a separate workflow.

- **`Data/`** — :pick: Mining in progress :pick:

- **`Fonts/`** — Contains fonts used by the game, stored in the `.ttf` format.

- **`Glade/`** — Contains configuration for the different [glade environments](), including Autumn, Flowery, Olden, Summer, and Winter.

- **`Lang/`** — Contains the game's translations. These are stored in editable YAML files containing translation keys and their corresponding text for each supported language.

- **`Luts/`** — Contains LUTs (**Look-Up Tables**) used to map one set of colours to another, including those used by Photo Mode. These can be [modified](../modding-tools/lut-editing.md).

- **`Prefabs/`** — Contains configuration for objects such as trees. Rather than containing the mesh itself, these files describe how assets are assembled and loaded using the RON format.

- **`Starting-Build/`** — Contains [save files](./starterbuilds.md) that are loaded when starting a new glade.

- **`Tod/`** — Short for **time of day**. Contains lighting and environmental settings for the different time-of-day options.

- **`Ui/`** — :pick: Mining in progress :pick:

- **`Colors.json`** — :pick: Mining in progress :pick:

### `Manifest.json`

`Manifest.json` contains a list of asset paths together with their corresponding **checksums**. The game can use these checksums to detect modified or corrupted asset files.

If an asset has been modified and its checksum no longer matches the value recorded in the manifest, the game may fail to load or crash during startup.

!!! info
    `Manifest.json` itself is not checked in the same way as the listed assets. Entries can therefore be removed from the manifest when experimenting with modified assets.

    Modifying game files directly is separate from Tiny Glade's official modding and Steam Workshop system.

## Additional Resources

- [Rust Programming Language](https://www.rust-lang.org/)
- [Bevy Engine](https://bevyengine.org/)
- [Bevy Engine GitHub](https://github.com/bevyengine/bevy)
- [FMOD API Reference](https://www.fmod.com/docs/2.02/api/studio-api.html)