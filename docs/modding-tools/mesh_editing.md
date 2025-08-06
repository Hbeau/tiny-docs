# Mesh Editing with Blender Add-On

The **Tiny Glade Blender Add-On** lets you easily **import and export** [Tiny Glade mesh files](../game-knowledge/meshes.md) (`.json`) for editing in [Blender](https://www.blender.org/).

---

## Installation

### **Requirements:**  
- [Blender](https://www.blender.org/download/) (any recent version)
- The add-on Python script: [Download from GitHub](https://github.com/Hbeau/TinyGlade-Blender-AddOn/releases)

### **To install:**  
1. Open Blender.  
2. Go to **Edit → Preferences → Add-ons**.  
3. Click the **arrow-down button** at the top right, then select **Install from Disk**.  
4. Choose the downloaded `tiny_glade_blender_addon.zip` file and click **Install from Disk** (bottom right).  
5. **Enable** the add-on by checking its box in the add-ons list.  

---

## Importing Tiny Glade Meshes

1. In Blender, go to **File → Import → Tiny Glade JSON (.json)**.
2. Select your mesh file and click **Import**.
![import window](import.jpg)

Your object will appear in Blender as **"Tiny Glade Object"**.

### **Supported features:**
- **Vertex positions** and **faces** import correctly.  
- **Normals** may sometimes be inverted—double-check them!  
- **Vertex colors** are poorly supported (may need manual adjustment).  
- **UV maps** are not well supported.  

*Other mesh attributes are not currently supported.*

---

## Modeling Tips

- **Triangulate faces**: Use Blender’s edit mode to convert all faces to triangles. This is required for proper color handling.
- **Apply vertex colors**: Use **Vertex Paint** mode after triangulating.
- **Check normals**: Make sure all normals point outward.
- **Paint every vertex**: If any vertex is missing a color, the game will crash.

!!! danger
    **Missing vertex colors will crash the game!**  
    Always ensure every vertex is painted.

---

## Exporting Tiny Glade Meshes

1. Select your object in **Object Mode**.
2. Go to **File → Export → Tiny Glade JSON (.json)**.
3. Choose a file name matching the asset you want to replace.
4. In the right panel, select the required attributes for your mesh.
![export window](export.jpg)
!!! info
    Export change the order of vertex and faces, that can cause trouble especially when you animate sheep

---

## Video Tutorial

Watch this step-by-step video by JSK for a full walkthrough:

<div align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/0-j9FaxsRGE?si=H5yMLdaPEZ3J2YAw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

---
## Troubleshooting

If you run into problems after importing or exporting meshes, here are some common issues and solutions:

### 1. Game Crashes at Startup

![crash window](crash.jpg){: style="height:360px;display:block;margin:auto"}

If Tiny Glade crashes, a log file is generated in `tmp/panics/panic_yyyy-mm-dd hh:mm:ss` inside your Tiny Glade folder.  
To access the log, click the right button and then the "Details" button in the crash window.

**Check the bottom of the log for error messages.**  
The two most common causes are:

- **Missing required mesh attributes:**  
  Your exported mesh may lack necessary data (like normals or colors).  
  Example error:
  ```
  2025-03-24T22:27:02.493+01:00 ERROR [tiny_glade::panic_reporter] [frame:0] PANIC: panicked at crates/country-core/src/resources/render/mesh_atlas_library.rs:89:17:
  Error adding prefab AtlassedMeshName(NameHash { hash: 13536922265885218580 }) to atlas of shader SolidVertexColor: Mesh attribute mismatch.
      Existing: ["Vertex_Color", "Vertex_Normal", "Vertex_Position", "flags"]
      Incoming: ["Vertex_Color", "Vertex_Position", "flags"]
  ```
  **Solution:**  
  Make sure your mesh includes all required attributes in the export windows 
!!!Info
    If the atribute is not in the export windows you can try to add it manually in the json file

- **Unpainted vertices:**  
  If any vertex is missing a color, the game will crash.
  ```
  2025-05-30T18:02:02.238+02:00 ERROR [tiny_glade::panic_reporter] [frame:0] PANIC: panicked at crates/country-core/src/utils/load_json.rs:44:9:
  assertion failed: values.array_length() as i32 > max_index
  ```
  **Solution:**  
  In Blender, use Vertex Paint mode and make sure every vertex is painted.

---

### 2. Colors Are Incorrectly Placed

If your mesh has strange or misplaced colors, it’s usually because the original object had quad faces instead of triangles.

![cube quad](cube_paint.jpg)

**Solution:**  
Always triangulate faces before painting colors.  
Go to **Edit Mode → Select All → Faces → Triangulate Faces**.

---

### 3. Item Looks Dark or Transparent

If your item appears too dark or transparent in-game, the normals are probably inverted.

![cube normal inverted](cube_normal_inverted.jpg)

**Solution:**  
In Blender, select your mesh, go to **Edit Mode → Mesh → Normals → Recalculate Outside** to fix the normals.

---

**Still stuck?**   
- Visit the **Tiny Glade Discord** #modding channel for help.  
- Check the [Mesh Rendering](../game-knowledge/meshes.md) page for more technical details.  

---


