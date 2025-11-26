# 5.4 Configuring the Working Space


We will define the space to limit the robot tool's operating range within the allowed workspace.
The XY plane will be restricted inside the pentagonal fence, and the Z-axis range will be limited to 0–3400 mm.

1. For convenience, change the view to a top-down perspective.
In HRSpace4, select `Top` from the `View` ribbon menu.
(Each click rotates the view 90°.)

   ![](../_assets/ch05_40_view_up.PNG)

2. Temporarily hide the column (pillar) model that obstructs area selection by unchecking it in `Style - Show`.

   ![](../_assets/ch05_43_pillar.PNG)
   ![](../_assets/ch05_46_show.PNG)

3. In Extended Properties, select `layout/spaces/space 0`.
On the General tab, set the `Activation` option to `Always On`.
The settings should match the figure below:

   ![](../_assets/ch05_50_space_gen.PNG)

4. On the `Area` tab, click the `Start Input` button on the right.
   (The button will change to `End Input`.)
   Using the left mouse button, click slightly inside each of the five corners of the pentagonal fence in the 3D view.
   A light green polygon will appear, representing the working space.
   (Z max and Z min are automatically set to 20 and -20, respectively.)

   ![](../_assets/ch05_53_space_area.PNG)

5. After selecting all five points, click the `End Input` button. (The button will revert to `Start Input`.)
If you want to redefine the area, click `Start Input` to clear all previous points and start over.

   ![](../_assets/ch05_54_space_area2.PNG)


6. For precise adjustments, you can type values directly into the table widget.
Click the (![](../_assets/toolbar_save.PNG)) button to apply the changes to the 3D view.

   ![](../_assets/ch05_56_space_area_adjust.PNG)


7. Rotate the view to inspect from the side.
   Since the current Z range is -20 to 20 mm, the working space appears flat at the robot base height when viewed from the side.

   ![](../_assets/ch05_58_z.PNG)


8. The robot coordinate system is at a height of 800 mm, and the Z-axis range should be 0–3400 mm in world coordinates.
Therefore, in robot coordinates, set Zmin–Zmax to -800–2600 mm.
After entering the values, click the ![](../_assets/toolbar_save.PNG) button to finalize the configuration.

   ![](../_assets/ch05_60_z2.PNG)


9. Open `Home - Gizmo`, and in position or scale adjustment mode, drag along the Z-axis to adjust Zmax and Zmin. (Adjustment along the X or Y axes is not available.)

   ![](../_assets/ch05_61_z3.PNG)


10. Since the configured working space occupies the entire cell, it may obstruct other settings.
On the `General` tab, set Activation to `Always Off` to temporarily hide the working space shape.
After completing other settings, switch it back to `Always On`.
