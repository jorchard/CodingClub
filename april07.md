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

## Challenge 1

You are going to add code to make a second bouncing circle. Set up variables for its location (call them `a` and `b`), its velocity (call them `va` and `vb`), and its radius (call it `r2`).

Inside the `while` loop, update the position of circle 2, and draw it.

<details>
<summary>Solution</summary>
    Replace
    <pre>#===== SET UP CIRCLE 2 =====</pre>
    with
    <pre># Position and velocity of circle 2
a = 20
b = 20
va = 2
vb = 3
r2 = 12  # radius of circle 2</pre>
    Replace
    <pre>   #===== MOVE CIRCLE 2 =====</pre>
    with
    <pre>    # Move circle 2
    a += va
    b += vb
    # Bounce circle 2
    if a\<r2 or a\>=width - r2:
        va = -va
    if b\<r2 or b\>=height - r2:
        vb = -vb</pre>
    Finally, replace
    <pre>   #===== DRAW CIRCLE 2 =====</pre>
    with
    <pre>   pygame.draw.circle(screen, (20, 255, 100), (a, b), r2)</pre>
</details>

## Challenge 2

Add code inside the loop that calculates the distance between the positions of the two circles. In Python, you can square a number using the double-asterix. For example, I can square `x` using `x**2`. Also, you can compute a square root of `y` using `np.sqrt(y)`.

Once you've done that, see if you can make circle 2 bounce when circles touch each other.

*Hint: How far apart are the centres of the circles when the circles touch?*

<details>
<summary>Solution</summary>
Compute the distance between the circle centres.
    <pre>   dist = np.sqrt( (x-a)**2 + (y-b)**2 )</pre>
Bounce them if they touch.
    <pre>   if dist<=20+r2:
        va = -va
        vb = -vb</pre>
</details>

