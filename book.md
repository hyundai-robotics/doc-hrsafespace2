
[__SOURCE](README.md)
# Hi7 Robot Controller Function Manual - HRSafeSpace2

{% endhint %}

[__SOURCE](0-about-this-manual/README.md)
# About the Manual

[__SOURCE](0-about-this-manual/precautions.md)
# Precautions

{% include file="en/precautions.md" %}

[__SOURCE](0-about-this-manual/safety-notice.md)
# Safety Cautions

{% include file="en/safety-notice.md" %}

{% hint style="warning" %}
- Control through external communication commands and applications is not a safety function and shall not be used as a substitute for a safety-related control system.
- Safety functions such as SafeSpace and Soft Joint are supplementary risk-reduction measures and do not replace external safety fencing, interlocks, or risk assessments.
{% endhint %}

[__SOURCE](1-preface/README.md)
# 1. Preface

This document describes how to use HRSafeSpace2, the PC-based configuration utility for the SafeSpace 2.0 feature of the HD Hyundai Robotics Hi7 controller.

[__SOURCE](1-preface/1-intro.md)
# 1.1 Introduction


The Hi7 controller from HD Hyundai Robotics is equipped with SafeSpace v2.0, a safety feature compliant with the IEC 61508 Functional Safety standard.
This feature is designed to protect human operators in the event of misuse, malfunction, or failure of the robot system.

The SafeSpace 2.0 settings of the Hi7 controller can be configured using one of the following three methods:

  * TP630 Teach Pendant (industrial-type TP)
  * TP640 Teach Pendant (tablet-type TP)
  * HRSafeSpace2 Application (Windows desktop PC application)

All SafeSpace v2.0 configuration screens are identically provided across these three devices.

This manual does not describe the individual configuration screens. Instead, it covers the following topics:

  * How to install the HRSafeSpace2 application
  * Screen layout and basic operation of HRSafeSpace2
  * How to link HRSafeSpace2 with HRSpace4 to visually edit safety layouts within a 3D virtual workspace

For detailed information on each configuration screen, please refer to the
[SafeSpace 2.0 Safety Function Manual](https://hrbook-hrc.web.app/#/view/doc-safespace2.0/english/README).

[__SOURCE](1-preface/2-prerequisite.md)
# 1.2 Prerequisite


This manual is intended for users who are already familiar with the following materials:

  * [Hi6/Hi7 Controller Operation Manual](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/README)

  * [SafeSpace 2.0 Safety Function Manual](https://hrbook-hrc.web.app/#/view/doc-safespace2.0/english/README) : You may read this manual first if preferred.

  * HRSpace4 Function Manual (HRSpace4 Help) : Required only when using HRSafeSpace2 in conjunction with HRSpace4.
  
[__SOURCE](2-install/README.md)
# 2. Installation

- Required Environment
  * Windows 10 64-bit or later
  * Wired Ethernet interface

1. Visit the [HD Hyundai Robotics Download Center](https://www.hd-hyundairobotics.com/en/download-center/list) and search for HRSafeSpace2 under `search` to download the installer.
(A user account and login are required to download files.)


2. Extract the downloaded ZIP file to any folder and run setup.exe.


3. Proceed by clicking the `Next >` button.
   
	![](../_assets/ch01_10_install.PNG)


4. When the Complete screen appears, click `Close` to finish the installation.. 
   
	![](../_assets/ch01_14_install.PNG)

[__SOURCE](3-operation/README.md)
# 3. Operation


HRSafeSpace2 can be run either as a stand-alone application or as a plug-in integrated within HRSpace.

Chapters 3 and 4 describe the operation based on the stand-alone application.
The same procedures apply similarly when running it as a plug-in.

This chapter explains how to launch HRSafeSpace2, its screen layout, and how to load and save configuration files.

[__SOURCE](3-operation/1-start.md)
# 3.1 How to Launch the Application


1. Click the HRSafeSpace2 icon on the Windows desktop or from the Start menu.
The `_ko` icon launches the Korean version, and the `_en` icon launches the English version.

   ![](../_assets/ch03_10_start.PNG)

2. HRSafeSpace2 will start.

   ![](../_assets/ch03_20_hrsafespace2.PNG)

{% hint style="info" %}

If the application fails to start, install the following file and try again:

```cmd
C:/Program Files/HHI Robotics/HRSafeSpace2/vc_redist.x64.exe
```

{% endhint %}
[__SOURCE](3-operation/2-screen-layout.md)
# 3.2 Screen Layout


![](../_assets/ch03_20_hrsafespace2.PNG)

* At the top, you will find the title bar, pull-down menus, and the toolbar.

* On the left side, a tree view displays all configuration items for SafeSpace2.

* When you select a specific item in the tree, the corresponding configuration screen appears on the right.

* At the bottom, the log window displays various errors and messages.
Clicking the `clear log` button on the right side of the log window clears the log entries.

[__SOURCE](3-operation/3-setting.md)
# 3.3 Configuring SafeSpace2


- Select the item you want to configure in the tree view, and set the values on the right-hand screen.

  ![](../_assets/ch03_30_setting.PNG)

- Even if you select a different item in the tree and move to another screen, the values you entered are retained in memory.
  (In other words, there is no need to save before switching screens.)

- If a value outside the allowed range is entered, attempting to switch to another screen will fail. The log window at the bottom displays the invalid value along with the valid range.
  Correct the value to fall within the valid range before switching screens.

  ![](../_assets/ch03_40_range.PNG)

[__SOURCE](3-operation/4-open-save.md)
# 3.4 Saving and Loading


- To save your configuration, select `File - Save` or `File - Save As...` from the menu.

  ![](../_assets/ch03_60_open_save.PNG)

  Alternatively, click the Save button on the toolbar:

- In the save dialog, navigate to the desired folder and enter a file name.
Configuration files are saved in `.json` format.

  ![](../_assets/ch03_63_save.PNG)

- To load a previously saved file after restarting HRSafeSpace2, select `File - Open` from the menu, or click the ![](../_assets/toolbar_open.PNG) button on the toolbar:

- Selecting the saved file will load the configuration into the application.

- To reset SafeSpace2 settings to their default values, select `File - New` from the menu, or click the ![](../_assets/toolbar_new.PNG) button on the toolbar:

[__SOURCE](4-comm/README.md)
# 4. Communication


This chapter explains how to connect HRSafeSpace2 to the Hi7 controller, set a password, and download or upload the configured settings.

[__SOURCE](4-comm/1-network-setting.md)
# 4.1 Network Configuration


1. Connect the PC running HRSafeSpace2 to the Hi7 controller's general-purpose Ethernet port using an Ethernet cable.

2. Ensure that the PC's network adapter IP address is on the same subnet as the Hi7 controller.

   ![](../_assets/ch04_05_network_adapter.PNG)

3. Open the IP Address Settings dialog by selecting `Tools - Set IP Address` from the menu.

   ![](../_assets/ch04_00_tool_menu.PNG)

   Alternatively, click the ![](../_assets/toolbar_ipaddr.PNG) button on the toolbar:

4. Enter the IP addresses for both the PC and the Hi7 controller, then click `OK`.

[__SOURCE](4-comm/2-password.md)
# 4.2 Password


To prevent unauthorized modifications to SafeSpace2 settings, it is mandatory to set a SafeSpace2 password on the Hi7 controller.


## Setting a Password for the First Time

1. Select `Tools - Change Password` from the menu.

   ![](../_assets/ch04_00_tool_menu.PNG)

   Alternatively, click the ![](../_assets/toolbar-password.PNG) button on the toolbar:

2. When the dialog appears, enter the new password in `New Password` and re-enter the same password in `Confirm Password`, then click `Change`.

   ![](../_assets/ch04_20_ch_password.PNG)

3. If the `Complete` message box appears, the password has been successfully set.

   ![](../_assets/msgbox_complete.PNG)

4. If a `Timeout Error` message box appears, check the IP address settings, the Ethernet cable connection, or whether the Hi7 controller is functioning properly.

   ![](../_assets/ch04_30_timeout.PNG)


## Changing an Existing Password

1. Select `Tools - Change Password` from the menu.

   ![](../_assets/ch04_00_tool_menu.PNG)

   Or click the ![](../_assets/toolbar-password.PNG) button on the toolbar:

2. In the dialog, enter the current password in `Old Password`, the new password in `New Password`, and re-enter the new password in `Confirm Password`, then click `Change`.

   ![](../_assets/ch04_40_ch_password2.PNG)

3. If the `Complete` message box appears, the password has been successfully changed.

   ![](../_assets/msgbox_complete.PNG)

[__SOURCE](4-comm/3-download.md)
# 4.3 Download


1. Select `Tools - Download` from the menu.

   ![](../_assets/ch04_00_tool_menu.PNG)

   Alternatively, click the ![](../_assets/toolbar_download.PNG) button on the toolbar:

2. When the dialog appears, enter the password in the `Password` field and click `Download`.

   ![](../_assets/ch04_50_download.PNG)

3. If the `Complete` message box appears, the download was successful.

   ![](../_assets/ch04_60_download_ok.PNG)

[__SOURCE](4-comm/4-upload.md)
# 4.4 Upload

1. Select `Tools - Upload` from the menu.

   ![](../_assets/ch04_00_tool_menu.PNG)

   Alternatively, click the ![](../_assets/toolbar_upload.PNG) button on the toolbar:


2. If the `Complete` message box appears, the upload was successful.

   ![](../_assets/msgbox_complete.PNG)
   
[__SOURCE](5-hrspace/README.md)
# 5. HRSpace4 Integration


This chapter explains how to load HRSafeSpace2 as a plug-in in an HRSpace4 project and visually edit the safety layout within a 3D virtual workspace.

{% hint style="info" %}
If HRSpace4 is not installed, visit the [HD Hyundai Robotics Download Center](https://www.hd-hyundairobotics.com/en/download-center/list) and search for HRSpace to download and install the latest version.
{% endhint %}

{% hint style="warning" %}
HRSpace version 4.3.2.0 or higher is required.
{% endhint %}


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

[__SOURCE](5-hrspace/1-install-plugin.md)
# 5.1 Installing the SafeSpace2 Plug-in


1. Copy the following five files from the folder where HRSafeSpace2 is installed:

   * favicon.ico
   * MxSafeSpace2.en.dll
   * MxSafeSpace2.ko.dll
   * SafeSpace2_en.hrsj
   * SafeSpace2_ko.hrsj

   ![](../_assets/ch05_10_plugin_install.PNG)


2. In the folder where HRSpace4 is installed, create a folder
`SafeSpace2/` on the `Library/Etc/` folder, and paste the copied files into this folder.

   ![](../_assets/ch05_15_plugin_install2.PNG)


{% hint style="info" %}

When launching HRSpace4 for the first time after installing the plug-in, the following dialog may appear.
Please wait until the configuration is complete.

   ![](../_assets/ch05_18_plugin_install3.PNG)

{% endhint %}

[__SOURCE](5-hrspace/2-load-plugin.md)
# 5.2 Loading the SafeSpace2 Plug-in


1. In HRSpace4, right-click the robot model in your workspace and select `Load Model as a Child...` from the pop-up menu.

   ![](../_assets/ch05_20_plugin_load.PNG)

2. Check the `Category - Etc.`, select `SafeSpace2_en` from the list, and click `OK`.

   ![](../_assets/ch05_25_plugin_load2.PNG)

3. Right-click the SafeSpace2 model created as a sub-model of the robot, and select `Extension properties...` from the pop-up menu.

   ![](../_assets/ch05_30_ex_prop.PNG)

4. The Extension properties dialog for the SafeSpace2 model will open, which is the HRSafeSpace2 interface.

   ![](../_assets/ch05_35_ex_prop2.PNG)

[__SOURCE](5-hrspace/3-open-save-in-plugin.md)
# 5.3 Opening and Saving Files in the SafeSpace2 Plug-in


When operating as a plug-in in HRSpace, the following file is loaded and saved by default, without additional specification:

```
{HRSpace project folder}/{robot's virtual controller folder}/project/safety/safety_parameter.json
```

For example, if you have saved the project file `spot_LH2.hrsj` in the folder `spot_LH2/` and the robot model is named `robot_0`, the folder structure is as follows:

```
spot_LH2/
  robot_0/
    project/
      jobs/
      logs/
      safety/
        safety_parameter.json   <--- This file is automatically loaded and saved.
      vars/
      hi6_proj.json
  spot_LH2.hrsj
```

If you wish to load or save a file other than the default, you can use `File - Save` or `File - Save As...`.
Integration with the 3D view works in the same way regardless of the file chosen.

[__SOURCE](5-hrspace/4-space-working.md)
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

[__SOURCE](5-hrspace/5-space-protective.md)
# 5.5 Configuring the Protective Space


Let’s designate the area where a human operator can stand as a protected space.

1. For convenience, change the view to a top-down perspective.
   In HRSpace4, select `Top` from the `View` ribbon menu.

   ![](../_assets/ch05_40_view_up.PNG)


2. In Extension Properties, select `layout/spaces/space 1`.
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

[__SOURCE](5-hrspace/6-robot-link.md)
# 5.6 Configuring Robot Links

You can apply capsule volumes to the robot's upper_frame and arm_frame to prevent collisions.

1. In Extension Properties, select `layout/robot`.
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
   Changes made with the gizmo are immediately reflected in the Extension Properties dialog.

   ![](../_assets/ch05_68_link_gizmo3.PNG)

[__SOURCE](5-hrspace/7-tool.md)
# 5.7 Configuring the Tool


You can apply various-shaped volumes to the robot's tool to prevent collisions.

1. In Extension Properties, select `layout/tools/tool0`. Each tool can combine up to 10 models.
First, set Model 0 as follows, then click the  ![](../_assets/toolbar_save.PNG) button.
   The shape will appear in the robot flange coordinate system.

   * Shape: `R.Plate`
   * Radius: 200 mm
   * Height: 500 mm
   * Width: 300 mm
   * Other parameters: 0

   ![](../_assets/ch05_70_tool_tool.PNG)


2. Use the Gizmo to move, rotate, and scale Model 0 so that it fully encloses the tool.
   Changes made with the gizmo are immediately reflected in the Extension Properties dialog.

   ![](../_assets/ch05_72_tool_tool2.PNG)


3. For precise adjustments, open Model 0's model properties and type the values directly.

   ![](../_assets/ch05_73_tool_tool_model_prop.PNG)


4. If there are portions extending beyond Model 0, add another model.
Create Model 1 as a capsule and use the gizmo to cover the protruding areas.

   * Shape: `Capsule`
   * Radius: 200 mm
   * Height: 500 mm
   * Other parameters: 0

[__SOURCE](5-hrspace/8-tool-orient.md)
# 5.8 Configuring Tool Orientation


If you want to limit the direction that the robot tool points within a specific angular range, you can use the Tool Orientation (tool_orient) settings.

(For demonstration purposes, the tool shapes from the previous section have been removed, and the spot welding gun tool's transparency is set to 60% via `Style - Transparency`.)


1. In Extension Properties, select `layout/tool_orient`.
   Enter an angular deviation of 60°, then click the [](../_assets/toolbar_save.PNG) button. A cone-shaped tool orientation range will appear in the robot flange coordinate system.

   ![](../_assets/ch05_76_tool_orient.PNG)


2. When Org.Rx, Ry, Rz are set to (0, 0, 0)°, the cone extends upward along the +Z direction in robot coordinates.
   This 60° cone limits the TCP +Z axis.
   The images below illustrate the TCP Z-axis within the allowed range and outside the range:

<table>
   <tr>
      <td>
         <img src="../_assets/ch05_78_tool_orient2.PNG"/>
      </td>
      <td>
         <img src="../_assets/ch05_79_tool_orient3.PNG"/>
      </td>
   </tr>
   <tr>
      <td align='center'>
          within the allowed range
      </td>
      <td align='center'>
         outside the allowed range
      </td>
   </tr>
</table>   


3. After modifying the angular range or direction values, click the ![](../_assets/toolbar_save.PNG) button again to apply the changes to the 3D view.

[__SOURCE](appendices/README.md)
# Appendices

  



[__SOURCE](appendices/rules-occupational-safety.md)
# Rules on Occupational Safety and Health Standards, and Notice for Safety Inspection

The industrial robot should be installed in consideration of the inspection standards, both of the Rules on Occupational Safety and Health Standards and of the Notice for Safety Inspection (if subject to inspection).

"[Rules on Occupational Safety and Health Standards](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/english/README)"

[__SOURCE](quality-assurance.md)
# Quality Assurance

"[Quality Assurance](https://hrbook-hrc.web.app/#/view/quality-assurance/en/README)"
