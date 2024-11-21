# Import the CMU Graphics package:
from cmu_graphics import *

Label('Position Properties Tutorial', 200, 20, size=20, bold=True)
Label('Press the mouse to move the rectangles', 200, 45)
Label('Blue rectangle sets the centerX & centerY properties', 200, 65)
Label('Gold rectangle sets the left & top properties', 200, 85)
Label('Red rectangle sets the right & bottom properties', 200, 105)

rect1 = Rect( 50, 150, 150, 100, fill='maroon', opacity=50)
rect2 = Rect(125, 200, 150, 100, fill='navy', opacity=50)
rect3 = Rect(200, 250, 150, 100, fill='gold', opacity=50)

def onMousePress(mouseX, mouseY):
    rect1.right = mouseX
    rect1.bottom = mouseY
    
    rect2.centerX = mouseX
    rect2.centerY = mouseY
    
    rect3.left = mouseX
    rect3.top = mouseY

# Run program:
cmu_graphics.run()

