Measure and improve your smile arc
On your running smiley, create a balanced smile arc and explain how your measurements keep the face responsive on a phone screen.

Sketch the face center, radius, mouth Rect, start angle, and sweep angle before coding.
Use size and radius instead of fixed screen pixels for the mouth position and size.
Test the painter on portrait and landscape phone-emulator layouts. Explain one change you made to keep it responsive.
Explain why shouldRepaint should return true when the mood changes and false when the inputs stay the same.


> The measurements keep the face responsive by adjusting the arc based on the size of the rectangle. The drawArc function inscribes an oval inside of the rectangle, so by specifying how much of the oval should be drawn (using the start angle and sweep angle), all you would need to change is the height of the rectangle, which is controlled by the  mood slider.

> shouldRepaint should return true only when the mood changes because shouldRepaint is the function that keeps track of if a change has been made. This prompts flutter to rebuild the widget with the new changes. If the function was set to always be true, flutter would keep trying to rebuild the widget even when there are no changes, costing processing time. 

> One change I made was to decrease the size of the hat. On landscape mode, the top of the hat gets cut off by the top widget due to space, so I made the hat smaller so that it would be noticeable on both landscape and portrait.