# Introduction to Python

### These notes follow the structure of the js-intro notes.

---

## Where does Python come from?

- General purpose programming language developed by Guido van Rossum and released in 1991. The current version in use is Python3.

### Stated Goals

    1. an easy and intuitive language just as powerful as those of the major competitors;
    2. open source, so anyone can contribute to its development;
    3. code that is as understandable as plain English;
    4. suitable for everyday tasks, allowing for short development times.

---

## What is Python good for?

- Python is a general purpose programming language that's pretty good at a lot of things.
- In the context of web apps, Python is good at handling data in the back end.

---

## Let's write some Python

1. In the terminal, type `python`. This will bring up the _python shell_, where we can write and run Python code line by line. The Python prompt looks like this:
   `>>>`
2. Try entering
   ```py
   >>> color = "blue"
   >>> print(color)
   ```
   What do you expect to see?
3. Now try:

   ```py
   >>> a = 1
   >>> b = 2
   >>> print(a + b)
   ```

   What do you expect to see?

4. What similarities and differences do you observe already between JavaScript and Python? We will keep revisiting this question as we learn Python syntax.

---

## Printing output in the shell

```py
print("My favorite color is", color)
```

---

## Parts of almost every language

- Data types
- Variables
- Conditionals
- Loops
- Functions

Recall how these were represented in JavaScript.

---

## Data types in Python as compared to JavaScript

| Data Type | Python                             | JavaScript                         |
| --------- | ---------------------------------- | ---------------------------------- |
| numbers   | Integer `1, -3, 0`                 | Number `1, 200, -3.14`             |
|           | Float `6.5, 2.0, -8.9`             |
|           | Complex `6 + 3i`                   |
| strings   | `"hello there!"`, `'hello there!'` | `"hello there!"`, `'hello there!'` |
| boolean   | `True/False`                       | `true/false`                       |
| no value  | `None`                             | `undefined` or `null`              |

---

## Numbers

- There are three types of numbers in Python
  - Integer (positive & negative whole numbers and zero)
  - Float (decimals - but careful not to do money with them, use the `Decimal` class instead)
  - Complex (numbers with real and imaginary parts)
- Can do math with `+`, `-`, `*`, `/`, `%`, and `**`
- Can compare with `==`\*, `!=`, `>`, `>=`, `<`, and `<=`

  \* Python also has the `is` comparison operator, which is used to indicate when two objects point to the same location in memory. We will likely only use this when comparing a value to `None` as in `if x is not None:`. There is no exact equivalent to `is` in JavaScript.

---

## Math operators

- `+`, `-`, `*`, `/`
  add, subtract, multiply, divide

- `%` **modulo**
  The remainder of division.For example, `9 % 2` equals `1`

- `**` **power**
  Raise x to the power of y. For example, `2 ** 3` equals `8`

---

## Strings

For when you need to represent characters/letters, words, sentences,

- "I have 5 pets"
- "0"
- ""
- "^&#O%@"
- "919-439-0215"

---

## Comments in Python

```python
something = "This is just to have some valid Python code here"
# single line comments in Python
something_else = "Some more code to make a new line in the example"

'''multi-line comment in python
called a docstring when used in a function to explain what the
function does'''
```

---

## Variables

- Variables are a name given to a value
- One way to think of them is a box that holds a value
- Unlike JavaScript, Python does not use keywords to declare variables. Variables are declared and defined in the same line
  ```py
  my_variable = 16
  ```

---

## Variable assignment and reassignment

```python
  word = "apple"
  word = "anteater"
  sum = 0
  sum = 9 + 3.16
```

---

## Shortcut assignment

`=` is used to assign values to variables. There are shortcuts for using math and updating variables, though.

```python
points += 5 # same as points = points + 5
points *= 2 # same as points = points * 2
# sadly there is no ++ in Python
```

---

## Write some more Python

<!-- TODO add exercises -->

1. Clone the following repo:
   `https://github.com/momentum-team-8/examples/tree/main/js-hello-world-exercise`
2. Open the repo in VS Code. You'll be working on the exercises in `main.js`.
3. Open `index.html` in your browser.
4. In the browser, open the dev tools and go to the JavaScript console by clicking on the "Console" tab.
5. Work on exercises 1-8. Uncomment the necessary lines in each exercise as you work on it. When you make a change in the javascript file, save it and then reload the index.html page in the browser. You should see the `console.log()` output in the console.

---

## Expressions and statements in Python

In a computer language, a group of words, numbers, and operators that performs a specific task is a **statement**. We say a statement is "run" or "executed".

`a = b * 2`

- `a` and `b` are variables. They will be _evaluated_.
- `2` is a value
- `*` and `=` are operators
- `b * 2` is an expression that will be _evaluated_.

**Expressions** are individual parts of a statement that are evaluated to produce a value.
Statements are executed to make something happen.

---

## Programming in Python

- As with JavaScript, programs are a sequence of statements to execute.
- Whereas JavaScript runs in the browser, Python runs on the server, executing these statements one after another in the order they are written.
- Like JavaScript, Python has conditionals and loops that control the flow of execution.
- One notable difference is that Python functions must be defined in the program _above_ where they are called. Because of hoisting, JavaScript functions can be defined anywhere. Python simply reads from top to bottom of the program and does not have hoisting.

---

## Conditionals

One of the most basic things we need to do in programming in any language is say "if this thing is true, then do this other thing. (And if it's not true, then don't do it.)"

We use **if** and **if/else** statements for this in Python, too, but the syntax is slightly different than in JavaScript.

---

## `if` can be used by itself without `else`

```python
if points > 10:
  print("You win")

madeGoal = True
if madeGoal:
  points += 2;
  print("You made a goal!")
  madeGoal = False;
```

---

## `if/else`

```python
if points > 10:
  print("You win");
else:
  print("You lose");
```

```python
if predicate:
  code_block
else:
  other_code_block
```

---

## `if...elif..else`

In Python, `else if` is compressed into `elif`

```py
if your_points > their_points:
  print("You win")
elif their_points > your_points:
  print("You lose");
else:
  print("You tied");
```

---

## Comparison operators

- `==` - equality
- `!=` - inequality
- `>`, `>=`, `<`, `<=`
- `is` means "points to the exact same place in memory," used most with `None`

---

## ⚠️ Note that `=` is not for comparison!

### `=` is the _assignment_ operator in Python, as in JavaScript

```py
a = b # assigns the value of b to a
a == b #compares to see if a is equal to and the same type as b
```

## Note that for equality and inequality, there are one fewer `=` than in JS.

## Truthy and Falsy

Every value can _act_ like a boolean. When a value is treated like a boolean, we say that it is either **truthy** or **falsy**.

A single expression or value can be used in a conditional:

```py
if value:
  # do something, because the value is truthy
else:
  #don't, because the value is falsy
```

[Truthy and Falsy in Python](https://www.freecodecamp.org/news/truthy-and-falsy-values-in-python/)

---

## Falsy values in Python

Sequences and Collections:

    Empty lists []
    Empty tuples ()
    Empty dictionaries {}
    Empty sets set()
    Empty strings ""
    Empty ranges range(0)

Numbers

    Zero of any numeric type.
    Integer: 0
    Float: 0.0
    Complex: 0j

Constants

    None
    False

---

## Truthy values in Python

Everything that is not on the falsy list is truthy. By default, an object is considered true.

Truthy values include:

    Non-empty sequences or collections (lists, tuples, strings, dictionaries, sets).
    Numeric values that are not zero.
    True

---

## _Anything_ that evaluates to true or false can be used in an if statement.

⚠️ You can always check conditions in the console

```py
if 32:
  print("This is true!")
```

---

## Logical operators

### These let us combine conditions

`and` and
`or` or
`not` not

```python
a = True;
b = False;

a and b; # a AND b have to be True for this expression to evaluate as True
a or b; # a OR b have to be True for this expression to evaluate as True
not a; # "not a": if a is True, then this will evaluate to False
not b; # "not b": if b is False, then this will evaluate to True
```

---

## while and for loops

The next basic thing we need to do in programming in any language is repeat the same task over and over.

`while` and `for` are our tools for this.

---

## while loop

```python
# say hi 5 times
count = 0
while count < 5:
  print("Hi!");
  count += 1;
```

---

## while loop

A while loop will run its code block as long as its predicate is true.

```print
while predicate:
  code_block
```

---

## for loops

Python does not have the equivalent of JavaScript's `for` loops. Both the functions of `for` loops and `for of` loops are performed by `for in` loops, which we will look at in detail along with lists (Python's name for arrays).

---

## While loop example

### Finding the first 10 prime numbers

```python
prime_count = 0
current_number = 1

while prime_count < 10:
  if is_prime(current_number):
    print(current_number, "is prime")
    prime_count += 1
  current_number += 1
```

Note: this depends on a function named is_prime() that we don't have defined here.

---

## Example of what was a `for` loop in JavaScript

### FizzBuzz

```py
for i in range(101):
  #range() generates a list of numbers from 0 to 100
  if i % 3 == 0:
    print(" Fizz")
  elif i % 5 == 0:
    print(" Buzz")
  else:
    print(i)
```

---

## Functions in Python

As in javaScript, a function is a block of code that takes zero or more values and returns one value.

Functions can also have side effects, which are changes caused apart from the value that the function returns.

Python uses the keyword `return` as JavaScript does.

---

You **declare** a function in python with the keyword `def`.

```py
def say_hello(name):
  return "Hello, " + name + "!"
```

Then you can **call** the function, which will actually run the code that is indented after the first line. Whitespace in Python serves the purpose that `{}` did in JavaScript.

```py
say_hello("Charlie")
# Hello, Charlie!
```

---

## Notes about functions, mostly the same as for JavaScript except the keyword

- Function declarations: a block of code that you define once and then can "invoke," or "call," over and over from other places in your code.
- _Declaring_ the function and _calling_ the function are two separate steps.
- Declare a function with the `def` keyword.
- The indented code is executed when the function is called.
- To call a function, you need the name of the function and parentheses after it.
- Can optionally take _arguments_ (aka _parameters_), which are values you give to the function when you call it. When your function needs to receive some outside information to run, you need an argument. Can have multiple arguments. The position of the arguments matters.
- Functions can optionally return a value back. To return a value from the function, you need the `return` keyword.
- `return` also stops the function on that line and exits. Nothing in the body of the function after a `return` will be run.

---

## Creating and using functions

```py
def ordinal(num):
  if (num > 3 and num <= 20) or (num < -3 and num >= -20):
    return str(num) + "th"
    # note that unlike in JS, we have to convert num to a string type in order to be able to add it to another string
  elif abs(num % 10) == 1:
      return str(num) + "st"
  elif abs(num % 10) == 2:
      return str(num) + "nd"
  elif abs(num % 10) == 3:
      return str(num) + "rd"
  return str(num) + "th"
```

---

## Function arguments and variable names, same as in JavaScript

- Function arguments are like variables
- You can reassign them with new values
- If you pass variables to a function as arguments, they _do not_ have to have the same name

---

## Using different variable and argument names example

```py
ball_radius = 10
pi = 3.14159

def circle_area(radius) {
  return pi * radius * radius;
}

print(circle_area(ball_radius));
```

---

## Write some Python

Create a python file. In this file, write four functions as described below. You should be able to call these four functions later in the file. To run a Python program in the
Terminal, type `python your_file_name.py`

1. a function that takes a single argument and then prints that argument in the terminal.
2. a function called sum with two parameters that returns the sum of those 2 numbers.
3. a function called get_length that takes one argument (a string) and returns its length
4. a function that takes a character as an argument (i.e. a string of length 1) and returns True if it is a vowel, False otherwise.

---

## Scope

In your Python program, `name` refers to variables, constants, functions, classes, and any object that can be given a name. Not every name is accessible in every part of the program. Scope determines where in the program a name is accessible. Python looks up names in an order referred to as LEGB.

- Local (function)
- Enclosing (for nested functions)
- Global (module)
- Built-in (running a program or shell)

Note that the keyword `global` does exist in Python, but it does not cause the behavior you would expect and generally should be avoided.

## Scope Example

One important difference between Python and JavaScript regarding scope is that Python does not have hoisting. Functions in Python are available in the order that they are written. You cannot call a function above where it is defined in a program.

### global scope

```py
name = "Keelan"
score = 0

if score == 0:
  # new scope - name and score are available
  punctuation = "!"
  print_loss(name, punctuation)

def print_loss(name, punctuation):
  # new scope - name and punctuation are available from the arguments,
  # and score is available from the global scope
  message = "You lose, " + name + punctuation + " Score: " + str(score)
  print(message)
```
