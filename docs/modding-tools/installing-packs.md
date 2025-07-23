# How to Install Asset Packs

Tiny Glade includes many [assets](../game-knowledge/game-structure.md) that you can modify to change the look and feel of your game.  
**Asset packs** are collections of these modified files, letting you customize things like:  
- Decorations and clutter  
- Entities (sheep, ducks, etc.)  
- Trees  
- Seasonal settings  

Asset packs **replace existing game files** and are loaded when the game starts.

!!! warning
    **Asset files are protected!**  
    The game uses a file called `build-info/manifest.json` to check if assets have been changed.  
    If you modify any asset, the game will refuse to start unless you update or clear the manifest.  
    See below for [how to clean the Manifest file](#manifest-file).

---

## Installation Methods

There are **two ways** to install custom assets:  
- **Manual installation**  
- **Automatic installation** (using Whiterun)

## Manual Installation

### 1. Clearing the Manifest File

The `manifest.json` file stores a **hash** for every game file, preventing unauthorized changes or file corruption.  
A typical entry looks like:

```json
[
  "default_settings.ron",
  "db6f245b9ab982c11191a4bbd7288267d879b530b5b052ca8ed8b5299b16ee91"
]
```

**Good news:**  
The manifest does **not** check itself, so you can safely edit or clear it.  
To allow modding, simply **remove all entries** from the manifest.  
Here’s a blank manifest you can use (or [download it here](./manifest.json){:download="manifest"}):  

```json
{
  "version": 1,
  "files": []
}
```

This disables the file check, letting you use your custom assets.  
*(But beware: the game may crash if your assets are broken!)*

!!! danger
    **Modding is fun but risky!**  
    - Always **back up your saves** before experimenting.  
    - If the game asks to send a crash report, say **no** to avoid annoying the dev teams (but you can share logs on Discord’s #modding channel, click on details, open `log.txt` and scroll to the bottom).  
    ![crash report](./crash-report.jpg){: style="height:400px;display:block;margin:auto"}
    - The manifest is reset after every game update, so check it regularly!

---

### 2. Installing the Asset Pack

1. **Extract** the new asset pack (usually a ZIP file).
2. **Copy** the new `assets` folder into your game directory, replacing existing files if prompted.
3. **Start the game** and enjoy your new content!

---

## Automatic Installation (Recommended for Beginners)

![Whiterun application](./Whiterun.jpg)
You can use the **Whiterun** tool to automate the process:

1. **Download Whiterun** from [GitHub](https://github.com/Hbeau/Whiterun/releases/tag/V1.2)  
   *(Requires [Java 24](https://adoptium.net/temurin/releases/?version=24) to run)*
2. **Open Whiterun** and patch your game (this will clear the manifest for you).
3. Click **"Add asset pack"** and move your ZIP file (do not extract) into the folder.
4. The pack should appear in the list.  
   Click on it, then click **"Install"**.
5. **Start the game** and enjoy!

---

## Recovering from Problems

If you want to **restore the default game** or if something breaks.  
1. go one the Tiny Glade steam page in your library  
2. click on the cog at the right and in the dropdown menu click on properties  
![properties](./steam_properties.jpg){: style="height:300px;display:block;margin:auto"}  
3. On the pop-up go to "installed files" menu and click on "verify integrity"
![verify integrity](./verify_integity.jpg){: style="height:300px;display:block;margin:auto"}

---

## Need Help?

- Join the **Tiny Glade Discord** (accessible inside the game) for help and sharing mods.
- You can find mods in the [Reddit community](https://www.reddit.com/r/TinyGladeMods/).

---

*Happy tinkering!*