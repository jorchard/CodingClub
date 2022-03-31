# March 31, 2022
[Home](./index.md)

## Graphics

We will use a module called [PyGame](https://www.pygame.org/docs/){:target="_blank"}.

Start by creating a replit using the Pygame template.

<img width="295" alt="image" src="images/templates.png">

Search for the "pygame" template. It might give you 2 choices. You can choose either one.

Paste the following lines:
```python
import sys, pygame

pygame.init()   # start pygame

# (width, height) of our graphics window
width = 400
height = 300

# Create the graphics window
screen = pygame.display.set_mode((width, height))
```

We are going to draw a circle. The circle's position will be stored in `x` and `y`.
```python
# Position of circle
x = 50  # x coordinate
y = 50  # y coordinate
```

Now let's draw on the screen.
```python
#-----Paint the screen-----

# Background
screen.fill((0,0,0))

# Draw a circle at position (x, y)
pygame.draw.circle(screen, (255,100,100), (x, y), 20)

# We have to ask pygame to display our drawings
pygame.display.flip()
```
It's like you draw on the back of a piece of paper, and then **flip** it over once you're done drawing. Then you draw on the back again.

<details>
<summary>Solution</summary>
<pre><code>age = int(age_string)
import sys, pygame

pygame.init()   # start pygame

\# (width, height) of our graphics window
width = 400
height = 300

\# Create the graphics window
screen = pygame.display.set_mode((width, height))

\# Initial position
x = 50
y = 50
\# Velocity
vx = 2
vy = 3

while True:

    # Update location
    x += vx
    y += vy

    # Bounce of sides
    if x<0 or x>width:
        vx = -vx
    if y<0 or y>height:
        vy = -vy

    # Paint the screen
    screen.fill((0,0,0))   # Background
    # Draw a circle
    pygame.draw.circle(screen, (255,100,100), (x,y), 20)

    # We have to ask pygame to display our drawings
    pygame.display.flip()
    pygame.time.Clock().tick(60)</code></pre>
</details>

---

