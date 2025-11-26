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
