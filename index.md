## Let's Learn Python... right NOW!

Copy and paste this code into `main.py` in [replit.com](http://replit.com){:target="_blank"}.
```python
# Any line that starts with a number sign is just for
# the programmer to read, and is ignored by
# the computer.

# Print "Hello world!"
print('Hello world.')

# Set the string variable <name> to your name.
name = 'Jeff'
print(f'Hello {name}')

# Set your age
age = 14

# Boolean variables are True or False
am_a_baby = (age<2)
# Print it
```

## Lists
Copy and paste.
```python
#===== LISTS =====
mygrades = [79, 85, 60, 91]
print(mygrades[0])
print(mygrades[2])
print(mygrades[-1])

print(mygrades)

# You can create a list for counting
print(list(range(8)))
# What happens when you uncomment the next line?
#print(range(8))
```


## Loops
Add the code below to your program.
```python
#===== LOOPS =====
# Print 'Are you 1?', 'Are you two?', etc.
mygrades = [79, 85, 60, 91]

for grade in mygrades:
    # The indented lines are repreated in the loop.
    # They are inside the loop block.
    print(grade)
print('Done.')

# We can use range to count.
for number in range(10):
    print(number)

# Write a loop that prints:
# Are you 1?
# Are you 2?
# ...
# Are you 14?
    
age = 14
# for c in...
#    print(...)
```
