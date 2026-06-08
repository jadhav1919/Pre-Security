# Python Basics Notes

## What is Python?

Python is a:

* High-level programming language
* General-purpose programming language
* Easy to read and write
* Popular in cybersecurity, automation, web development, AI, and data science

### Why Python?

* Simple syntax
* Beginner friendly
* Large number of libraries
* Cross-platform support


# Program Goal: Guess the Number Game

The game works as follows:

1. Computer chooses a random number between 1 and 20.
2. User enters a guess.
3. Program checks the guess.
4. Program gives a hint:

   * Too high
   * Too low
   * Correct
5. Repeat until the correct number is guessed.


# Variables

## What is a Variable?

A variable is a container used to store data.

### Example

```python
secret = 10
tries = 0
guess = 0
```

### Variables Used

| Variable | Purpose                  |
| -------- | ------------------------ |
| secret   | Stores the random number |
| guess    | Stores user input        |
| tries    | Counts attempts          |


# Importing Modules

Python can use libraries (modules) to perform tasks.

### Example

```python
import random
```

This imports the random module.


# Random Numbers

### randint()

Used to generate a random integer.

Syntax:

```python
random.randint(start, end)
```

Example:

```python
secret = random.randint(1, 20)
```

Returns a number between 1 and 20.


# Displaying Output

### print()

Used to display text on the screen.

Syntax:

```python
print("Hello")
```

Example:

```python
print("I'm thinking of a number between 1 and 20")
```

Output:

```text
I'm thinking of a number between 1 and 20
```

# Taking User Input

### input()

Used to read input from the user.

Syntax:

```python
input("Enter value:")
```

Example:

```python
text = input("Take a guess: ")
```

Important:

```python
input()
```

always returns text (string).


# Converting Data Types

### int()

Used to convert text into an integer.

Example:

```python
guess = int(text)
```

Input:

```text
10
```

Stored as:

```python
10
```

(integer)


# Arithmetic Operations

### Incrementing a Variable

Increase value by 1.

Example:

```python
tries = tries + 1
```

If:

```python
tries = 3
```

After execution:

```python
tries = 4
```


# Conditional Statements

Used to make decisions.

### if

Syntax:

```python
if condition:
    statement
```


### elif

Means:

```text
else if
```

Syntax:

```python
elif condition:
    statement
```


### else

Executed when all previous conditions are false.

Syntax:

```python
else:
    statement
```

# Comparison Operators

| Operator | Meaning               |
| -------- | --------------------- |
| ==       | Equal to              |
| !=       | Not equal to          |
| <        | Less than             |
| >        | Greater than          |
| <=       | Less than or equal    |
| >=       | Greater than or equal |

Examples:

```python
guess < secret
```

```python
guess > secret
```

```python
guess != secret
```

# Logical Operators

## or

Returns True if at least one condition is True.

Example:

```python
guess < 1 or guess > 20
```

Checks if the number is outside the valid range.


# Guess Checking Logic

### Out of Range

```python
if guess < 1 or guess > 20:
```

Output:

```text
That number is out of range. Try again.
```


### Too Low

```python
elif guess < secret:
```

Output:

```text
Too low, try again.
```

### Too High

```python
elif guess > secret:
```

Output:

```text
Too high, try again.
```


### Correct Guess

```python
else:
```

Output:

```text
You got it!
```


# Loops

## What is a Loop?

A loop repeats a block of code until a condition changes.

Example:

```text
Keep asking until user guesses correctly.
```


# while Loop

Used when repetition depends on a condition.

Syntax:

```python
while condition:
    statements
```


### Example

```python
while guess != secret:
```

Meaning:

```text
Continue while guess is not equal to secret.
```

# Loop Execution

### Secret = 10

User enters:

```text
5
```

Condition:

```python
5 != 10
```

Result:

```text
True
```

Loop continues.


User enters:

```text
10
```

Condition:

```python
10 != 10
```

Result:

```text
False
```

Loop stops.


# Program Flow

```text
Start
 ↓
Generate random number
 ↓
Display message
 ↓
User enters guess
 ↓
Increase try count
 ↓
Check:
    Out of range?
    Too low?
    Too high?
    Correct?
 ↓
If not correct → repeat
 ↓
If correct → end
```


# Important Functions

| Function         | Purpose                 |
| ---------------- | ----------------------- |
| print()          | Display output          |
| input()          | Read user input         |
| int()            | Convert text to integer |
| random.randint() | Generate random number  |


# Important Keywords

| Keyword | Purpose         |
| ------- | --------------- |
| import  | Import module   |
| if      | First condition |
| elif    | Else if         |
| else    | Default action  |
| while   | Loop            |


# Key Concepts Learned

## Variables

Store data.

Example:

```python
secret = 15
```


## Input

Get data from user.

Example:

```python
input()
```


## Output

Show information.

Example:

```python
print()
```


## Type Conversion

Convert one data type to another.

Example:

```python
int("10")
```


## Conditional Statements

Allow decision-making.

Example:

```python
if
elif
else
```

## Loops

Repeat code.

Example:

```python
while
```


## Random Numbers

Generate unpredictable values.

Example:

```python
random.randint(1,20)
```

---

