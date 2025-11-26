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
