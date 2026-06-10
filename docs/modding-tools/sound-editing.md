# Sound editing 

## Introduction 

After some talks with the Game Dev and the Audio Dev on how to edit files and if it is feasible. They told me editing directly with [Fmod](https://www.fmod.com/) is only possible by editing with the Original Project, but we dont have this.

So i tried multiple different Tools to edit Fmod files, around 4 different ones i could find. Most i found either dont work with the game files, or unpack into a unreadable, unplayable *.ogg.

But at least i found one, which is very easy and simple.


## Necessary Tools

To edit the sounds you only need [Fmod-Bank-Tools](https://github.com/Wouldubeinta/Fmod-Bank-Tools)

For editing the audio i use [Audacity](https://www.audacityteam.org/) or you can use any other Audio editing Software.


## Steps

- Download Fmod Bank Tools
- Unpack it anywhere and keep the folder structure.
- go to **`...\Tiny Glade\assets\audio\Desktop`**
- make a Backup of all **[NAME].assets.bank** you want to edit.
!!! info
     we only ever need to edit the asset.bank files, all other files do not contain any audio

- Copy the files you want to edit into the **`Banks\`** folder inside the Fmod-Bank-Tools folder
!!! info
    The same sound effect, can be in multiple *.asset.Bank files. f.e. the sheep sound is in 3 different files and all of them need to be changed to have the sound work consistantly.
- Run the Tool and press *extract*
- The tool will now create multiple folders:
  
    **fsb** - This Folder has the extracted archives (*.fsb) where the audio files are stored in.

    **wav** - where you find the converted Audio files **This is our Main folder to work with**

- you can now open and edit the *.wav files with a editor of your choice

!!!Danger
    - It's important to keep the original bitrate (or lower)  
      Original Bitrate of TG Audio is 1536 kBit/s or 48000 kHz

    - The length of the new audio needs to be the same or shorter. (same length is the safe bet to have it work later)

    - And ofc. the final filename needs to be the same.

!!! tipp
    I always open the original *.wav first. Then load my sound into a second channel so that i can fit my sound to the original channel. After im done, i delete the original channel and save the file overwriting the original.

- After you are done with all files you want to edit. Open the Fmod-Banks-Tool and press on *rebuild*
- The tool creates another folder called **`Build\`** where it puts your new files.
- Copy the new **[NAME].assets.bank** file you just build into the games folder and overwrite the original.




*Have fun making your own Audio* 