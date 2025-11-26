# 5.5 Configuring the Protective Space


Let’s designate the area where a human operator can stand as a protected space.

1. For convenience, change the view to a top-down perspective.
   In HRSpace4, select `Top` from the `View` ribbon menu.

   ![](../_assets/ch05_40_view_up.PNG)


2. In Extended Properties, select `layout/spaces/space 1`.
On the General tab, set the `Activation` option to `Always On`.
   The settings should match the figure below:

   ![](../_assets/ch05_62_ps01.PNG)


3. On the `Area` tab, click the `Start Input` button on the right.
   (The button will change to `End Input`.)
   Now, use the left mouse button to click four points on the floor around the human operator in the 3D view.
   A red polygon will appear, representing the protective space.
   (Z max and Z min are automatically set to 20 and -20, respectively.)

   ![](../_assets/ch05_62_ps05.PNG)


4. After selecting all four points, click the `End Input` button. (The button will revert to `Start Input`.)
   If you want to redefine the area, click `Start Input` to clear all previous points and start over.


5. For precise adjustments, you can type values directly into the table widget.
Click the (![](../_assets/toolbar_save.PNG)) button to apply the changes to the 3D view.

   ![](../_assets/ch05_62_ps10.PNG)


6. Rotate the view to inspect from the side.
   Since the current Z range is -20 to 20 mm, the working space appears flat at the robot base height when viewed from the side.

   ![](../_assets/ch05_62_ps15.PNG)


7. Since the robot base height is 800 mm, if the protective space height is set to 3000 mm, set Zmin–Zmax to -800–2200 mm. After entering the values, click the ![](../_assets/toolbar_save.PNG) button to finalize the configuration.

   ![](../_assets/ch05_62_ps20.PNG)
