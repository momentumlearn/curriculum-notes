# Introduction to Programming with JavaScript

---

## Where does Python come from?

- General purpose programming language developed by Guido van Rossum and released in 1991.

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
- There does exist a `global` keyword that can be used for declaring variables, but it's behavior is not what you would expect and generally not what you would ever want.

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
points += 5; // same as points = points + 5
points *= 2; // same as points = points * 2
# sadly there is no ++ in Python
```

---

## Write some Python 2

<!-- TODO add examples -->

1. Clone the following repo:
   `https://github.com/momentum-team-8/examples/tree/main/js-hello-world-exercise`
2. Open the repo in VS Code. You'll be working on the exercises in `main.js`.
3. Open `index.html` in your browser.
4. In the browser, open the dev tools and go to the JavaScript console by clicking on the "Console" tab.
5. Work on exercises 1-8. Uncomment the necessary lines in each exercise as you work on it. When you make a change in the javascript file, save it and then reload the index.html page in the browser. You should see the `console.log()` output in the console.

---

## Expressions and statements in JavaScript

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
- Like JavaScript, Python has conditionals and loops.

---

## Conditionals

One of the most basic things we need to do in programming is say "if this thing is true, then do this other thing."

# We use **if/else** statements for this.

One of the most basic things we need to do in programming is say "if this thing is true, then do this. (And if it's not true, then don't do it.)"

Sometimes we also want to say "And if it's not true, then do that."

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
  codeBlock
else:
  otherCodeBlock
```

---

## `if...elif..else`

In Python, `else if` is compressed into `elif`

```py
if yourPoints > theirPoints:
  print("You win")
elif theirPoints > yourPoints:
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

---

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

`&&` and
`||` or
`!` not

```js
let a = true;
let b = false;

a && b; // a AND b have to be true for this expression to evaluate as true
a || b; // a OR b have to be true for this expression to evaluate as true
!a; // "not a": if a is true, then this will evaluate to false
!b; // "not b": if b is false, then this will evaluate to true
```

---

## while and for loops

The next basic thing we need to do in programming is repeat the same task over and over.

`while` and `for` are our tools for this.

---

## while loop

```js
// say hi 5 times
let count = 0;
while (count < 5) {
  console.log("Hi!");
  count += 1;
}
```

---

## while loop

A while loop will run its code block as long as its predicate is true.

```js
while (predicate) {
  codeBlock;
}
```

---

## for loop

```js
// say hi 5 times
for (let count = 0; count < 5; count++) {
  console.log("Hi!");
}
```

---

## for loops

A for loop combines its setup, predicate, and updating in one statement. It will run its code block as long as its predicate is true.

```js
for (setup; predicate; update) {
  codeBlock;
}
```

---

## When do I use a while loop vs a for loop?

- A for loop is for when you need to go through a limited list of numbers, always increasing (or decreasing) by the same amount, and ending at a specified point.
- A while loop is for everything else.
- You might think you'd use more while loops than for loops, but that's not usually the case.

---

## While loop example

### Finding the first 10 prime numbers

```js
let primeCount = 0;
let currentNumber = 1;

while (primeCount < 10) {
  if (isPrime(currentNumber)) {
    console.log(currentNumber, "is prime");
    primeCount += 1;
  }
  currentNumber += 1;
}
```

Note: this depends on a function named isPrime() that we don't have defined here.

---

## For loop example

### FizzBuzz

```js
for (let i = 1; i <= 100; i++) {
  if (i % 3 === 0) {
    console.log(" Fizz");
  } else if (i % 5 === 0) {
    console.log(" Buzz");
  } else {
    console.log(i);
  }
}
```

---

## What is a function?

A function is a block of code that takes zero or more values and returns one value.

This block of code isn't executed immediately, but later when it is _called_.

---

## Think about a recipe - black beans and rice

1. **Chop** an _onion_.
2. **Mince** _two cloves of garlic_.
3. **Heat** _1 teaspoon olive oil_ in a _stockpot_ over _medium-high heat_.
4. **Add** the _onion_ and _garlic_ and **saute** for _4 minutes_.
5. **Add** the _rice_ and **saute** for _2 minutes_.
6. **Add** _1.5 cups of vegetable broth_ and **boil** _the mixture_.
7. **Lower the heat** and **cook** for _20 minutes_.
8. **Add** _the spices_ and _3.5 cups black beans_.

---

## How to chop a vegetable

1. If the _vegetable_ is an onion, **peel back** the _papery skin_ and **cut off** the _top_.
2. **Cut** the _vegetable_ in _half_.
3. **Place** _each half_ cut-side down and **slice** the _vegetable_ _lengthwise_ in _parallel cuts_.
4. **Cut** the _vegetable_ with _several horizontal cuts parallel to the board_.
5. **Cut** through the _vegetable_ at _right angles to the board_.

- Each work in recipe vocabulary (chop, mince, saute, boil, etc) contains several sub-steps. These are _functions_!
- How you do each of these things is dependent on what you're doing it to (the _arguments_!)

---

You need to **declare** the function first.

```js
function sayHello(name) {
  return "Hello, " + name + "!";
}
```

Then you can **call** the function, which will actually run the code inside the curly braces.

```js
sayHello("Charlie");
// Hello, Charlie!
```

---

## Notes about functions

- Function declarations: a block of code that you define once and then can "invoke," or "call," over and over from other places in your code.
- _Declaring_ the function and _calling_ the function are two separate steps.
- Declare a function with the `function` keyword.
- The code inside the curly braces is executed when the function is called.
- To call a function, you need the name of the function and parentheses after it.
- Can optionally take _arguments_ (aka _parameters_), which are values you give to the function when you call it. When your function needs to receive some outside information to run, you need an argument. Can have multiple arguments. The position of the arguments matters.
- Functions can optionally return a value back. To return a value from the function, you need the `return` keyword.
- `return` also stops the function on that line and exits. Nothing in the body of the function after a `return` will be run.

---

## Creating and using functions

```js
function ordinal(num) {
  if ((num > 3 && num <= 20) || (num < -3 && num >= -20)) {
    return num + "th";
  } else if (Math.abs(num % 10) === 1) {
    return num + "st";
  } else if (Math.abs(num % 10) === 2) {
    return num + "nd";
  } else if (Math.abs(num % 10) === 3) {
    return num + "rd";
  }
  return num + "th";
}
```

---

## Function arguments and variable names

- Function arguments are like variables
- You can reassign them with new values
- If you pass variables to a function as arguments, they _do not_ have to have the same name

---

## Using different variable and argument names example

```js
let ballRadius = 10;
let pi = 3.14159;

function circleArea(radius) {
  return pi * radius * radius;
}

console.log(circleArea(ballRadius));
```

---

## Write some Javascript 3

Create a javascript file and link it to an html page (or use one the you created earlier). In the js file, write four functions as described below. You should be able to call these four functions in the console.

1. a function that takes a single argument and then logs that argument to the console.
2. a function called sum with two parameters that returns the sum of those 2 numbers.
3. a function called getLength that takes one argument (a string) and returns its length
4. a function that takes a character as an argument (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.

---

## Scope

Variables have a _scope_ -- a defined area of the code where they exist and can be used. If you define a variable outside of any code block (an area surrounded by curly braces), it is available throughout your code. If you define a variable within a code block, it is available in that code block and all code blocks nested under it.

---

## Scope Example

```js
// global scope
let name = "Keelan";
let score = 0;

if (score === 0) {
  // new scope - name and score are available
  let punctuation = "!";
  printLoss(name, punctuation);
}

function printLoss(name, punctuation) {
  // new scope - name and punctuation are available from the arguments,
  // and score is available from the global scope
  let message = "You lose, " + name + punctuation;
  console.log(message);
}
```
