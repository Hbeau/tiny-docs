# Windows

There are 3 main kinds of windows, each with several variants:
- **Arrow Slit**: small square hole in the wall
- **Cottage Window**: square window in a rustic style
- **Gothic Window**: pointed arch window

Each type comes in 3 sizes and can be placed in a **building**, a **wall**, or a **roof**.  
Each window has simple, dormer, and half-dormer versions, which are considered different kinds of windows.

Each window is made up of several meshes that define its appearance and behavior in the environment. Not all windows use these meshes in the same way:
- The **collision mesh** defines a bounding box around the window. This is used to prevent overlapping. For **cottage windows only**, the collision mesh also creates a square hole in the wall. For other window types, the hole in the wall is hardcoded and cannot be modified.

Below are side-by-side images showing the collision results for different window types:
<div style="display: flex; justify-content: space-evenly;" markdown="span">
    ![Cottage Collision](cottage_window_collision_result.png){ width="200" }  
    ![Arrow Slit Collision](arrow_slit_collision_result.png){ width="200" }  
    ![Gothic Collision](gothic_window_collision_result.png){ width="200" }  
</div>




 


---

## Window Meshes Table

| Window & Image                                                                                                       | Related Meshes                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Arrow Slit 1x1**<br>![arrow_slit_1x1](tg_windows/arrow_slit_1x1.jpg)                                               | - arrow_slit_1x1.json<br>- arrow_slit_1x1_collision.json<br>- arrow_slit_1x1_interaction.json<br>- arrow_slit_1x1_glass.json<br>- arrow_slit_1x1_outline.json                              |
| **Arrow Slit 1x2**<br>![arrow_slit_1x2](tg_windows/arrow_slit_1x2.jpg)                                               | - arrow_slit_1x2.json<br>- arrow_slit_1x2_collision.json<br>- arrow_slit_1x2_interaction.json<br>- arrow_slit_1x2_glass.json<br>- arrow_slit_1x2_hat.json<br>- arrow_slit_1x2_outline.json |
| **Arrow Slit 1x3**<br>![arrow_slit_1x3](tg_windows/arrow_slit_1x3.jpg)                                               | - arrow_slit_1x3.json<br>- arrow_slit_1x3_collision.json<br>- arrow_slit_1x3_interaction.json<br>- arrow_slit_1x3_glass.json<br>- arrow_slit_1x3_hat.json<br>- arrow_slit_1x3_outline.json |
| **Arrow Slit 1x2 Half-Dormer**<br>![arrow_slit_1x2_halfdormer](tg_windows/arrow_slit_1x2_halfdormer.jpg)             | - arrow_slit_1x2_halfdormer.json                                                                                                                                                           |
| **Arrow Slit 1x3 Half-Dormer**<br>![arrow_slit_1x3_halfdormer](tg_windows/arrow_slit_1x3_halfdormer.jpg)             | - arrow_slit_1x3_halfdormer.json                                                                                                                                                           |
| **Cottage Window 1x1**<br>![cottage_window_1x1](tg_windows/cottage_window_1x1.jpg)                                   | - window_cottage_1x1.json<br>- window_cottage_1x1_collision.json<br>- window_cottage_1x1_interaction.json<br>- window_cottage_1x1_glass.json<br>- window_cottage_1x1_outline.json          |
| **Cottage Window 1x1 Dormer**<br>![cottage_window_1x1_dormer](tg_windows/cottage_window_1x1_dormer.jpg)              | - window_cottage_1x1_dormer.json<br>- window_cottage_1x1_full_dormer.json                                                                                                                  |
| **Cottage Window 1x1 Half-Dormer**<br>![cottage_window_1x1_halfdormer](tg_windows/cottage_window_1x1_halfdormer.jpg) | - window_cottage_1x1_halfdormer_frame.json                                                                                                                                                 |
| **Cottage Window 1x2**<br>![cottage_window_1x2](tg_windows/cottage_window_1x2.jpg)                                   | - window_cottage_2x1.json<br>- window_cottage_2x1_collision.json<br>- window_cottage_2x1_interaction.json<br>- window_cottage_2x1_glass.json<br>- window_cottage_2x1_outline.json          |
| **Cottage Window 1x2 Dormer**<br>![cottage_window_1x2_dormer](tg_windows/cottage_window_1x2_dormer.jpg)              | - window_cottage_2x1_full_dormer.json                                                                                                                                                      |
| **Cottage Window 1x2 Half-Dormer**<br>![cottage_window_1x2_halfdormer](tg_windows/cottage_window_1x2_halfdormer.jpg) | - window_cottage_2x1_halfdormer_frame.json                                                                                                                                                 |
| **Cottage Window 1x3**<br>![cottage_window_1x3](tg_windows/cottage_window_1x3.jpg)                                   | - window_cottage_3x1.json<br>- window_cottage_3x1_collision.json<br>- window_cottage_3x1_interaction.json<br>- window_cottage_3x1_glass.json<br>- window_cottage_3x1_outline.json          |
| **Cottage Window 1x3 Dormer**<br>![cottage_window_1x3_dormer](tg_windows/cottage_window_1x3_dormer.jpg)              | - window_cottage_3x1_full_dormer.json                                                                                                                                                      |
| **Cottage Window 1x3 Half-Dormer**<br>![cottage_window_1x3_halfdormer](tg_windows/cottage_window_1x3_halfdormer.jpg) | - window_cottage_3x1_halfdormer_frame.json                                                                                                                                                 |
| **Gothic Window 1x1**<br>![gothic_window_1x1](tg_windows/gothic_window_1x1.jpg)                                      | - window_gothic_1x1.json<br>- window_gothic_1x1_collision.json<br>- window_gothic_1x1_interaction.json<br>- window_gothic_1x1_glass.json<br>- window_gothic_1x1_outline.json               |
| **Gothic Window 1x1 Dormer**<br>![gothic_window_1x1_dormer](tg_windows/gothic_window_1x1_dormer.jpg)                 | - window_gothic_1x1_dormer.json<br>- window_gothic_1x1_hat.json<br>- window_gothic_1x1_hat_full.json                                                                                       |
| **Gothic Window 1x1 Half-Dormer**<br>![gothic_window_1x1_halfdormer](tg_windows/gothic_window_1x1_halfdormer.jpg)    |                                                                                                                                                                                            |
| **Gothic Window 1x2**<br>![gothic_window_1x2](tg_windows/gothic_window_1x2.jpg)                                      | - window_gothic_2x1.json<br>- window_gothic_2x1_collision.json<br>- window_gothic_2x1_interaction.json<br>- window_gothic_2x1_glass.json<br>- window_gothic_2x1_outline.json               |
| **Gothic Window 1x2 Dormer**<br>![gothic_window_1x2_dormer](tg_windows/gothic_window_1x2_dormer.jpg)                 | - window_gothic_2x1_dormer.json<br>- window_gothic_2x1_hat.json<br>- window_gothic_2x1_hat_full.json                                                                                       |
| **Gothic Window 1x2 Half-Dormer**<br>![gothic_window_1x2_halfdormer](tg_windows/gothic_window_1x2_halfdormer.jpg)    |                                                                                                                                                                                            |
| **Gothic Window 1x3**<br>![gothic_window_1x3](tg_windows/gothic_window_1x3.jpg)                                      | - window_gothic_3x1.json<br>- window_gothic_3x1_collision.json<br>- window_gothic_3x1_interaction.json<br>- window_gothic_3x1_glass.json<br>- window_gothic_3x1_outline.json               |
| **Gothic Window 1x3 Dormer**<br>![gothic_window_1x3_dormer](tg_windows/gothic_window_1x3_dormer.jpg)                 | - window_gothic_3x1_dormer.json<br>- window_gothic_3x1_hat.json<br>- window_gothic_3x1_hat_full.json                                                                                       |
| **Gothic Window 1x3 Half-Dormer**<br>![gothic_window_1x3_halfdormer](tg_windows/gothic_window_1x3_halfdormer.jpg)    |                                                                                                                                                                                            |


