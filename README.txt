 --------------
| REQUIREMENTS |
 --------------
Blender 3.0 or above

 ---------------
| COMPILE ENGINE|
 ---------------
Open the bezier/build folder and run the following commands:
-cmake ..
-make
 ------------
| HOW TO RUN |
 ------------
Open Blender and from the scripting tab open the ui.py file and execute (Run Script button, Alt-P or Text -> Run Scipt). Now the Geodesic tab is created in 3d Viewport side context menu (press N in the viewport to toggle this menu).
NOTE: Only one instance of Blender using the Geodesic function can run at the same time since the add-on connects to a specific port.

 --------------
| INSTRUCTIONS |
 --------------

- ADD BEZIER SPLINE -
Press this button to enter in the drawing mode. In the drawing mode select 3 points in the same object to draw a spline. To exit the drawing mode before adding a spline press the Right mouse button or ESC.
NOTE: A spline with 4 control points will be created. The last two points are coincidents.

- EDIT BEZIER SPLINE -
Select a spline and press this button to enter the editing mode

PICK: left mouse button on the target object to pick a control point. If there is no control point near enough the first one will be selected. Once an anchor point on the curve has been selected the relative tangent points become pickable
 
DRAG: hold the left button on the target and move the mouse

ADD CONTROL POINT: right mouse button. Cannot add on closed splines

SHARP/SMOOTH TANGENTS: press the T key to switch between sharp and smooth tangents

CLOSE/OPEN SPLINE: C button to close or open a spline. Closing segment changes depending on sharp or smooth tangents

DELETE SEGMENT: Pick a segment to delete and press the X button. Cannot delete if only one segment is present

SPLIT: press S to enter in the split mode. Ctrl + MOUSE WHEEL to change the splitting point on the curve. Press the left mouse button to split, or the S button again to exit the splitting mode 

UNDO: Ctrl + Z

REDO: Shift + Ctrl + Z

EXIT: ESC 

Note: If a target object is modified after drawing spline, on the first draw request (on either add or edit modes) the current splines on the object will be invalidated and it will not be possible to edit the anymore. From that point it will be possible to draw new splines with the updated geometry

 ------------
| PARAMETERS |
 ------------

The decastel_jau option select the algorithm used to calculate the curve: decastel_jau if the box is selected, subdivisions otherwise.
The subdivision variable sets the number of subdivisions of the curve. The parameters will be applied on drawing the next time a spline is edited or added. 