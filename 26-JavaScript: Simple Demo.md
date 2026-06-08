# JavaScript: Simple Demo - Concepts

## What is JavaScript?

JavaScript is a high-level, general-purpose programming language primarily used for web development. It can run inside web browsers and on servers using Node.js.


# Variables

Variables are used to store data that can change during program execution.

```javascript
let tries = 0;
let guess = 0;
```

* Declared using `let`
* Value can be modified later


# Constants

Constants store values that should not change.

```javascript
const secret = 10;
```

* Declared using `const`
* Value cannot be reassigned


# Random Number Generation

JavaScript uses `Math.random()` to generate random numbers.

```javascript
Math.random()
```

To generate a random integer between 1 and 20:

```javascript
Math.floor(Math.random() * 20) + 1
```

# Output

The `console.log()` method is used to display information on the screen.

```javascript
console.log("Hello World");
```


# User Input

The `rl.question()` method is used to receive input from the user.

```javascript
const text = await rl.question("Take a guess: ");
```

Input is received as text (string).


# Type Conversion

The `parseInt()` function converts text into an integer.

```javascript
guess = parseInt(text, 10);
```

Example:

```javascript
parseInt("15", 10);
```

Output:

```text
15
```


# Conditional Statements

Conditional statements allow programs to make decisions.

## if

Executes code when a condition is true.

```javascript
if (guess < secret) {
    console.log("Too low");
}
```

## else if

Checks another condition if the previous condition is false.

```javascript
else if (guess > secret) {
    console.log("Too high");
}
```

## else

Executes when all previous conditions are false.

```javascript
else {
    console.log("Correct");
}
```


# Comparison Operators

| Operator | Meaning               |
| -------- | --------------------- |
| <        | Less than             |
| >        | Greater than          |
| <=       | Less than or equal    |
| >=       | Greater than or equal |
| ==       | Equal                 |
| !=       | Not equal             |
| ===      | Strict equal          |
| !==      | Strict not equal      |

# Logical OR Operator

The OR operator is represented by `||`.

```javascript
guess < 1 || guess > 20
```

Returns true if at least one condition is true.


# Loops

Loops are used to repeat code multiple times.

## While Loop

A while loop continues running as long as its condition remains true.

```javascript
while (guess !== secret) {
    // code
}
```

The loop stops when the condition becomes false.


# Guess the Number Game Logic

1. Generate a random number between 1 and 20.
2. Ask the user for a guess.
3. Convert the input into an integer.
4. Increase the attempt counter.
5. Compare the guess with the secret number.
6. Display:

   * Out of range
   * Too low
   * Too high
   * Correct
7. Repeat until the user guesses correctly.


# Important JavaScript Keywords

| Keyword | Purpose              |
| ------- | -------------------- |
| let     | Declare variable     |
| const   | Declare constant     |
| if      | Decision making      |
| else if | Additional condition |
| else    | Default action       |
| while   | Repetition           |


# Important Functions

| Function      | Purpose                   |
| ------------- | ------------------------- |
| console.log() | Display output            |
| rl.question() | Read user input           |
| parseInt()    | Convert string to integer |
| Math.random() | Generate random value     |
| Math.floor()  | Remove decimal part       |


# Key Concepts Learned

* Variables and constants
* User input and output
* Random number generation
* Type conversion
* Conditional statements
* Comparison operators
* Logical operators
* While loops
* Program flow and decision making
