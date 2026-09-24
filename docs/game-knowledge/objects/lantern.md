Lantern are special items that are actually light source. Unlinke clutter with emissive, lantern can light items in their surrounding. They are stored in the decorator folder and modding these assets comes under the assets replacement type (you can't add lantern).

You have to use the blender addon to export the proper json files. 

There are 3 types of lanterns based on where they are placed : on the ground, this is the lantern_terrain, on top of a building it's the "lantern" and against walls it's the lantern_wall.You may find a collision mesh in the files.its purpose is to set the bounding box but it can be leaved as is.

Lantern has two main mesh , three for the lantern terrain.
The outside and the inside. The outside is like the structure of the lantern it (can have multiple colors to be verified) but no texture. The inside color should be set (for a reason) but does not appear in game because it's replaced by the light color.Further research has to be performed to see if light color can be changed. 
Lantern_terrain has a support that has the wood texture.

Note : Each lantern has a fixed light source height, so the new lantern must keep the shape of the original. 



