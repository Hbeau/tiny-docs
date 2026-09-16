# Sound Editing

## Introduction

After discussing sound editing with the game and audio developers, we learned that directly editing Tiny Glade's audio with [FMOD](https://www.fmod.com/) would require the original FMOD project, which is not publicly available.

Several tools were tested for extracting and rebuilding FMOD files. Most either did not work with Tiny Glade's files or extracted audio into unreadable or unplayable `.ogg` files.

Fortunately, **Fmod-Bank-Tools** provides a relatively simple way to extract, edit, and rebuild the game's audio banks.

## Necessary Tools

To edit Tiny Glade's sounds, you will need:

- [Fmod-Bank-Tools](https://github.com/Wouldubeinta/Fmod-Bank-Tools)
- An audio editor

This guide uses [Audacity](https://www.audacityteam.org/), but any suitable audio editing software can be used.

## Editing Audio

### 1. Find the Audio Banks

Tiny Glade's FMOD audio banks can be found in:

```text
...\Tiny Glade\assets\audio\Desktop
```

Before making any changes, create a backup of every `[NAME].assets.bank` file you intend to edit.

!!! info

    Only the `.assets.bank` files need to be edited for this process. The other bank files do not contain the audio being replaced.

### 2. Copy the Banks into Fmod-Bank-Tools

Copy the `.assets.bank` files you want to modify into the `Banks` folder inside the Fmod-Bank-Tools directory.

!!! info

    The same sound effect may appear in multiple `.assets.bank` files.

    For example, a sheep sound may be present in several different banks. Each copy may need to be replaced for the edited sound to be used consistently throughout the game.

### 3. Extract the Audio

Run **Fmod-Bank-Tools** and select **Extract**.

The tool will create several folders, including:

- **`fsb/`** — contains the extracted `.fsb` archives where the original audio is stored.
- **`wav/`** — contains the extracted audio converted to `.wav` files.

The `wav` folder is the main folder you will work with when editing sounds.

### 4. Edit the Audio

Open the `.wav` file you want to modify in Audacity or another audio editor.

!!! warning

    When replacing audio, keep the following limitations in mind:

    - Keep the same audio format and sample rate as the original file where possible.
    - Tiny Glade audio commonly uses a **48 kHz** sample rate.
    - The replacement audio should be the same length as, or shorter than, the original. Keeping the same duration is the safest option.
    - The final file name must remain exactly the same as the original.

!!! tip

    A useful workflow in Audacity is to open the original `.wav` file first, then import your replacement audio as a second track.

    This allows you to compare the timing and adjust the replacement audio to match the original. Once finished, remove the original track and export the edited audio using the original file name.

### 5. Rebuild the Audio Bank

After editing all of the desired `.wav` files:

1. Open **Fmod-Bank-Tools**.
2. Select **Rebuild**.
3. The tool will create a `Build` folder containing the rebuilt bank files.
4. Copy the new `[NAME].assets.bank` file back into Tiny Glade's audio folder.
5. Replace the original file when prompted.

!!! warning

    Make sure you have a backup of the original bank before replacing it. Game updates may also restore modified audio files.

## Restoring the Original Audio

If the modified audio causes problems, you can either restore your backup or use Steam to restore Tiny Glade's original files:

1. Open **Tiny Glade** in your Steam library.
2. Click the **gear icon** and select **Properties**.
3. Open **Installed Files**.
4. Select **Verify integrity of game files**.

Steam will restore modified or missing game files.

Have fun creating your own Tiny Glade audio replacements!