# March 24, 2022
[Home](./index.md)

## User Input

Sometimes, you want the user to input some information. The program can ask a question, and it will
wait for the user to type something in and hit `Enter`. For example, this line of code,
```python
name = input('What is your name? ')
```
will take whatever the user typed, and assign it to the variable `name`. Try it. Then follow it with a print
command. Something like...
```python
print(f'{name} is a future coder.')
```

---
Have the user enter their age.
```python
age_str = input('How old are you? ')
```
How old they will be in 10 years? Notice that `age_str` is a **string** (text), not a number; we added `_str` to the name to remind us. You can't do math with a string. Instead, you can convert the string to a number (integer) using `int` like this,
```python
age = int(age_str)
```
**Add a print statement** that outputs something like this:
```
Ten years from now, you will be __ years old.
```
(except your print statement should give a number).

<details>
<summary>Solution</summary>
<pre><code>age = int(age_string)
print(f'Ten  years from now, you will be {age+10} years old.')
</code></pre>
</details>

---

## if statements

This is one of the most powerful programming methods. Cut-and-paste this code to the bottom of your program.
```python
if age<4:
    print('You are too young to be in school')
else:
    print('You are old enough to be in school.')
```
Which print command it runs depends on the value of `age`.

---

## Number Guessing Game

The computer will choose a number from 1 to 20, and your job is to guess it.

Cut-and-paste this code to get you started.
```python
import numpy as np  # loads some useful math stuff

# It chooses a random secret number
secret_number = np.random.randint(1, 21)

guess_str = input('Guess a number from 1 to 20. ')
guess = int(guess_str)

while guess!=secret_number:

    #=====
    
    guess_str = input(f'Guess a number: ')
    guess = int(guess_str)

print(f'YOU GOT IT! The number was {secret_number}')
```

Wouldn't it be easier if the program told you whether your guess was too high or too low?
**Add a few lines of code to replace the `#=====` line** telling the user if their guess was higher or lower than the secret number.

<details>
<summary>
Solution
</summary>
<pre><code>  if guess &lt secret_number:
      print('Your guess is too low.')
  elif guess &gt secret_number:
      print('Your guess is too high.')
</code></pre>
    Make sure you indent this code to align with the other lines in the <code>while</code> loop, like the <code>guess_str = ...</code> line.
</details>

## Challenges
- You can help the user by keeping track of the lowest and highest guesses and printing them before each guess.
- Try changing the game so that it randomly chooses a number between 1 and 128?
- What is the best strategy to play this game?
- Can you guarantee that you will guess the secret number in 8 guesses or less?
- How many more guesses would it take if the secret number was between 1 and 256?
