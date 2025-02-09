# Game Structure
## How it works
The game is made in rust and use the bevy engine. The music is managed with fmod who allow evolutive sounds.
## Game Files
The main file is the TinyGlade.exe binary. its where sll the magic take place. the compiled rust code is turned in this binary.
the `Assets` folder contains the game assets : 
* Audio : under the audio folder you will found the musics but its and fmod compatible format , they are pretty heavy.
* Meshes : in the meshes folder, you will find the 3d models. they are sorted in the same ways of the game with subfolder for decorations and clutters.

To make sure assets are not corruped. a Manifest.json file list all path a corresponding checksum. if a file is modified, the game will crash att start
> Note that nothing verify is the manifest file is corrupted, so you just need to clear the corresponding entry in the manifest list or clear the whole array
