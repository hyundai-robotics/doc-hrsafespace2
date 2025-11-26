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
