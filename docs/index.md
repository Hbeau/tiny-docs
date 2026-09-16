# Welcome to Tiny Glade Modding Documentation

Tiny Glade is a cosy diorama builder where you can create whimsical castles, cottages, ruins, and landscapes using a flexible, gridless building system.

There are no management systems, combat mechanics, or objectives. The focus is entirely on building, experimenting, and creating detailed scenes.

**[Tiny Glade](https://store.steampowered.com/app/2198150/Tiny_Glade/)** is developed and published by [Pounce Light](https://x.com/pouncelight) and was released on **September 23, 2024**.

The game is written in **[Rust](https://www.rust-lang.org/)** and uses the **[Bevy](https://bevyengine.org/)** game engine.

Tiny Glade now includes **official mod support** together with a [Steam Workshop](https://steamcommunity.com/app/2198150/workshop/).

For most users, the official modding system and Steam Workshop are the recommended way to create, install, and share mods. The community also continues to document older asset-replacement methods and reverse-engineered game systems.

The modding community is active on Tiny Glade's **Discord server**, which can be accessed through the in-game menu. You can also visit the [Tiny Glade Mods subreddit](https://www.reddit.com/r/TinyGladeMods/) for community discoveries, guides, and modding discussions.

## Official Modding Documentation

The official Tiny Glade modding guide is available on the [Pounce Light website](https://pouncelight.games/tiny-glade/info/modding/).

This should be the first reference for information about supported modding features, including Steam Workshop integration and creating new clutter mods.

## Game Knowledge

Tiny Docs also documents game systems and asset formats that have been investigated by the community.

Current topics include:

- [Game Structure](game-knowledge/game-structure.md) — an overview of Tiny Glade's files and asset organisation.
- [Mesh Rendering](game-knowledge/meshes.md) — information about the built-in JSON mesh format and vertex data.
- [Saves](game-knowledge/save.md) — information about Tiny Glade save files, history, and snapshots
- [Starter Builds](game-knowledge/starterbuilds.md) — an overview of Tiny Glade's starter builds and adding new ones.
- Replacing Assets:
    - [Sheep](game-knowledge/objects/sheeps.md)
    - [Trees](game-knowledge/objects/trees.md)
    - [Windows](game-knowledge/objects/windows.md)
    - [Terrain](game-knowledge/objects/terrain.md)
    - [Garden Brush](game-knowledge/objects/garden_brush.md)
    - [Ducks](game-knowledge/objects/ducks.md)
    - [Roofs](game-knowledge/objects/roofs.md)
    - [Clutter](game-knowledge/objects/clutter.md)
    - [Flags](game-knowledge/objects/flags.md)
    - [Terrain Mod Tutorial](game-knowledge/objects/terrain_mods/terrain.md)

## Modding Tools

Explore community guides and tools for working with Tiny Glade:

- [Installing Assets](modding-tool/installing-assets.md) — working with the legacy Whiterun program for installing Tiny Glade assets.
- [Mesh Editing with Blender Add-On](modding-tools/mesh-edit-with-blender.md) — import, inspect, edit, and export Tiny Glade's built-in JSON meshes for asset replacement mods.
- [Sound Editing](modding-tools/sound-editing.md) — information about Tiny Glade sounds and music and how to replace them.
- [LUT Editing](modding-tools/lut-editing.md) — information about the games photomode filters and styles and how to change them.

!!! note

    The Blender Add-On is primarily used for Tiny Glade's built-in JSON mesh format and legacy asset-replacement workflows.

    New clutter created through Tiny Glade's official modding system uses `.glb` files and does not require the JSON Blender Add-On workflow.