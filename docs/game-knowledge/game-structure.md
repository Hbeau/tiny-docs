# Game Structure

## How It Works
The game is developed in **Rust** and utilizes the **Bevy** engine ([Bevy Engine](https://bevyengine.org/)). The music is managed with **FMOD** ([FMOD Documentation](https://www.fmod.com/docs/2.02/api/studio-api.html)), which allows for **evolutive** and dynamic soundscapes.

## Game Files
The main executable file is **`TinyGlade.exe`**. This binary contains the compiled Rust code where all the magic happens.

### `Assets` Folder
The `Assets` folder contains all the necessary game resources, organized into subdirectories:

- **`Audio/`**: This directory holds the game’s music and sound effects. The files are in an **bank format**, they are openable with the _fmod studio_ free for small organization < $200k.
- **`Meshes/`**: This directory contains all the **3D models** used in the game. The assets are categorized into subfolders such as `Decorations/` and `Clutters/`, reflecting their in-game organization.
- **`Data/`**: :pick: mining in progress :pick:
- **`Fonts/`**: Contains fonts used by the games stored in the ttf format
- **`Glade/`**: settings for each [glades]() : automn, flowery,olden,summer and winter.
- **`Lang/`**: Contains translation for many language. easy editable yml files with all translation key and the corrsponding value for each languages
- **`Luts/`**: :pick: mining in progress :pick:
- **`Prefabs/`**: It contains the different kind of tree. Not the meshes but a configuration in the ron format about how to load the tree
- **`Starting-Build/`**: This forlder contains [save files](./save.md) that are loaded when you start a new glade
- **`Tod/`**: acronym of **time of the day**, contain the light settings for every time settings
- **`Ui/`**: :pick: mining in progress :pick:
- **`Colors.json`**: :pick: mining in progress :pick:

### `Manifest.json`
To ensure assets are not corrupted, a **`Manifest.json`** file is included. This file contains a list of all asset paths along with their corresponding **checksums**. If a file is modified and its checksum does not match, the game will **crash on startup**.

!!! info 
    The game does **not** verify if `Manifest.json` itself is corrupted. You can manually remove entries from the manifest list or even clear the entire array to allow every assets modifications.  


## Additional Resources
- [Rust Programming Language](https://www.rust-lang.org/)
- [Bevy Engine GitHub](https://github.com/bevyengine/bevy)
- [FMOD API Reference](https://www.fmod.com/docs/2.02/api/studio-api.html)
