# 5.6 Configuring Robot Links

You can apply capsule volumes to the robot's upper_frame and arm_frame to prevent collisions.

1. In Extended Properties, select `layout/robot`.
   Modify Link 3 and Link 2 as follows, then click the ![](../_assets/toolbar_save.PNG) button. Capsules will appear at the positions of the two links.

   - Link 3 (Vertical)
     * Radius: 300 mm
     * Cylinder Height: 600 mm
     * RY: 90°

   - Link 2 (Horizontal)
     * Radius: 300 mm
     * Cylinder Height: 600 mm

   ![](../_assets/ch05_64_link.PNG)


2. Open `Home - Gizmo`, select the capsule for Link 3, and switch between Scale and Position modes to adjust the capsule size and position so that it fully encloses Link 3.

   ![](../_assets/ch05_64_link_gizmo.PNG)

   ![](../_assets/ch05_66_link_gizmo2.PNG)


3. Select the capsule for Link 2 and adjust its size and position in the same way to fully enclose Link 2.
   Changes made with the gizmo are immediately reflected in the Extended Properties dialog.

   ![](../_assets/ch05_68_link_gizmo3.PNG)
