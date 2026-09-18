# Savegames

*By Rapunzilla*

## Information About Game Saves

Information about how Tiny Glade savegames work, when the game saves, what data is stored, and where save files are located can be found in the [Developer Guide](https://pouncelight.games/tiny-glade/troubleshooting/saves/).

## Why Do My Savegames Use So Much Space?

To understand why a save folder can become large, it helps to know what the save is made of.

A Tiny Glade save is primarily made up of two components:

### `history.json`

This file contains the history of edits made to the glade and represents the underlying save data.

### Snapshots

Snapshots are created during manual and automatic saves. They allow the game to load the current state of a glade quickly.

Without a suitable snapshot, the game may need to reconstruct the glade from `history.json` by replaying the recorded edits. This is similar to rebuilding the glade from a timelapse and can take increasingly longer as a build becomes larger and more complex.

Snapshots provide a cached state of the build, allowing the game to load it much more quickly.

Because snapshots accumulate over time, the save folder can gradually increase in size.

!!! tip "Reducing save size"

    If you want to reduce the size of a save folder, older snapshots can be removed while keeping the most recent snapshot.

    Keeping the latest snapshot allows the current glade state to load quickly while reducing the amount of space used by older snapshots.

    Make a backup of the save folder before deleting files manually.

## Can I Install Other People's Savegames?

Yes. Savegames can be copied from another player into your Tiny Glade save folder and then opened in the game.

Community-created saves can also be downloaded from sites such as [Open-Glade](https://www.open-glade.com), where users can share their own builds.

!!! info "About Open-Glade"

    Open-Glade is a community-run website and is not affiliated with Pounce Light.

    As with any community-hosted download, only download files from sources you trust and scan unfamiliar files before opening them.

    Questions about Open-Glade should be directed to the community channels linked on the Open-Glade website.