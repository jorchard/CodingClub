# March 31, 2022
[Home](./index.md)

## Graphics

We will use a module called [PyGame](https://www.pygame.org/docs/){:target="_blank"}.

Start by creating a replit using the Pygame template.

<img width="295" alt="image" src="images/templates.png">

Search for the "pygame" template. It might give you 2 choices. You can choose either one.

Paste the following lines:
```python
import pygame

pygame.init()   # start pygame

# (width, height) of our graphics window
size = (400, 300)

# The next line creates the graphics window
screen = pygame.display.set_mode(size)
```

Now let's draw a circle on the screen.
```python
# Draw a circle
pygame.draw.circle(screen, (255,100,100), (50, 50), 20)

# We have to ask pygame to display our drawings
pygame.display.update()
```
For speed reasons, PyGame doesn't actually *show* what you drew until you ask it to update the display.

<details>
<summary>Solution</summary>
<pre><code>age = int(age_string)
print(f'Ten  years from now, you will be {age+10} years old.')
</code></pre>
</details>

---

