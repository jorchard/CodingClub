# April 7, 2022
[Home](./index.md)

## Graphics

Let's start with where we ended last week. Create a PyGame replit and paste the following code.
```python
import pygame

pygame.init()  # start pygame

# (width, height) of our graphics window
width = 400
height = 300

# Create the graphics window
screen = pygame.display.set_mode((width, height))

# Position of circle
x = 5  # x coordinate
y = 5  # y coordinate

vx = 1
vy = 1

while True:
    # Update the location BELOW
    x = x + vx
    y = y + vy

    if x<=0 or x>=width:
        vx = -vx

    if y<= 0 or y>=height:
        vy = -vy

    #-----Paint the screen-----
    # Background
    screen.fill((0, 0, 0))
    # Draw a circle at position (x, y)
    pygame.draw.circle(screen, (255, 100, 100), (x, y), 20)
    # We have to ask pygame to display our drawings
    pygame.display.flip()
    # Ask pygame to slow down so we can see movement
    pygame.time.Clock().tick(60)
```

**Challenge**

Add if-statements inside the loop that reverses the direction of motion when the ball hits the edges of the screen. Remember that the screen is `x=0` on the left, `x=width` on the right, `y=0` at the top, and `y=height` at the bottom.

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
