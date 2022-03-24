# March 24, 2022

## User Input

Sometimes, you want the user to input some information. The program can ask a question, and it will
wait for the user to type something in and hit `Enter`. For example, this line of code,
```python
name = input('What is your name? ')
```
will assign whatever the user typed to the variable `name`. Try it. Then follow it with a print
command. Something like...
```python
print(f'{name} is a future coder.')
```

The output looks like this:
```
Jeff is a future coder.
```

---
Have the user enter their age.
```python
age_str = input('How old are you? ')
```
Then print how old they will be in 10 years. But notice that `age_str` is a **string**, not a number (we added `_str` to the name to remind us). You can't do math with a string. Instead, you can convert the string to a number using
```python
age = int(age_str)
```

<details>
<summary>Solution</summary>
<pre><code>age = int(age_string)
print(f'Ten  years from now, you will be {age-10} years old.')
</code></pre>
</details>
