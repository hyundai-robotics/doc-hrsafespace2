# 5. HRSpace4 Integration


This chapter explains how to load HRSafeSpace2 as a plug-in in an HRSpace4 project and visually edit the safety layout within a 3D virtual workspace.

Assume that a robot spot-welding cell layout has been designed in HRSpace4 as shown below:

   ![](../_assets/ch05_00_hrspace4.PNG)

One HDR220-26 manipulator is installed inside the cell.
A C-type spot welding gun (c_gun_m) is mounted on the robot flange, and the robot is installed on a riser (Riser) with a height of 800 mm.
At the start of each work cycle, the operator places the workpiece on the positioner in front of the robot.
The robot performs spot welding on the workpiece and occasionally uses a tip dresser for dressing.

The entire cell is enclosed by five-sided fences.
To prevent collisions with the ceiling structure, the robot tool’s Z-axis range is limited to 0–3400 mm from the cell floor.
Additionally, assume there is one column (pillar) inside the fenced area.

Using HRSpace4's visual editing integration, we will generate SafeSpace2 configuration parameters and then download the resulting safety_parameter.json file to the actual Hi7 robot controller.
