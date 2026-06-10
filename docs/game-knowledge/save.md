# Savegames

## Infos about Game Saves

All information regarding how savegames work, when the game saves, what it saves and where you find your savegames can be found in the [Developers Guide](https://pouncelight.games/tiny-glade/troubleshooting/saves/)

## Why do my Savegames use a lot of Space?

To understand why the savegames use a lot of space we need to understand what uses this space and what main parts are the saves comprised of.

The Saves are made out of basically 2 parts. The History and the Snapshots.


**History.json**

- This file contains all of your edits and progress. This is your actual savegame


**Snapshots**

- Snapshots generate each manual and automatic save. The snapshots help the Game to instantly load your build upon opening the glade.
- Without the snapshots, the game would read the history.json and make each edit. basically rebuilding the glade a new. Like a Timelapse. With the snapshots the game knows the current state and can build it instantly. This way you dont need to sit through the rebuilding process every time, which gets more and more time consuming the bigger the build gets.

Since these Snapshots accumulate over time, the savegame folder gets bigger and bigger over time. So you need to delete the unnecessary ones yourself.

!!! quote "*tl;dr:*"
     To reduce the filesize you can delete all snapshots, except the very last one. So you will still instantly load your glade, but the folder size will not grow infinitely big


## Can i install other peoples savegames?

Yes, you can get savegames from friends and family and copy them to your savegame folder, to use them for yourself.

You can also download savegames from the community made website [Open-Glade](https://www.open-glade.com) or Upload your own for others to use.

!!! info
    Open-Glade is not affiliated with pounce-light and purely community made. Be aware of things you download and never download files you are not sure are safe to use. And never download anything without a proper anti-virus on your PC.

    For questions regarding Open-Glade, they have a seperate discord you can find on their webside.