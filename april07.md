# April 7, 2022
[Home](./index.md)

## Graphics

Let's start with where we ended last week. Create a PyGame replit and paste the following code.
```python
import pygame
import numpy as np

pygame.init()  # start pygame

# (width, height) of our graphics window
width = 400
height = 300

# Create the graphics window
screen = pygame.display.set_mode((width, height))

# Position and velocity of circle 1
x = 50  # x coordinate
y = 50  # y coordinate
vx = 2
vy = 5

#===== SET UP CIRCLE 2 =====

while True:

    # Move circle 1
    x = x + vx
    y = y + vy

    # Bounce circle 1
    if x<=0 or x>=width:
        vx = -vx  # reverse x direction
    if y<= 0 or y>=height:
        vy = -vy  # reverse y direction

    #===== MOVE CIRCLE 2 =====
    
    #-----Paint the screen-----
    # Background
    screen.fill((0, 0, 0))
    # Draw a circle at position (x, y)
    pygame.draw.circle(screen, (255, 100, 100), (x, y), 20)
    
    #===== DRAW CIRCLE 2 =====
    
    # We have to ask pygame to display our drawings
    pygame.display.flip()
    # Ask pygame to slow down so we can see movement
    pygame.time.Clock().tick(60)
```

**Challenge**

Add a second bouncing ball with radius `r2`. Set `r2` to Use `a` and `b` to store its position, and `va` and `vb` for its velocity.

<details>
<summary>Solution</summary>
    Add these lines before the loop.
<pre>vx = 1  # x velocity
vy = 1  # y velocity</pre>
    
Then add these lines inside the loop.
<pre>    if x<0 or x>width:
        vx = -vx
    if y<0 or y>height:
        vy = -vy</pre>
</details>
