# Computer Representation of Colors and Numbers

## Why Computers Use Binary?

Humans use the **decimal system (base-10)** because we have 10 digits:

```text
0 1 2 3 4 5 6 7 8 9
```

Computers use the **binary system (base-2)** because electronic components only have two states:

```text
0 = OFF
1 = ON
```

Examples:

* Low voltage = 0
* High voltage = 1
* Light OFF = 0
* Light ON = 1

Everything inside a computer is ultimately represented using 0s and 1s.


# Bit and Byte

## Bit

A bit is the smallest unit of data.

```text
0 or 1
```

A bit can represent only **2 states**.

Examples:

```text
ON / OFF
TRUE / FALSE
YES / NO
```


## Byte

A byte consists of 8 bits.

```text
1 Byte = 8 Bits
```

Example:

```text
10101010
```

A byte can represent:

```text
2^8 = 256 values
```

Range:

```text
0 - 255
```

# Computer Color Representation

Computers create colors using:

```text
RGB
```

Where:

* R = Red
* G = Green
* B = Blue


# 8 Color System

Suppose each color can only be:

```text
0 = OFF
1 = ON
```

We need 3 bits:

```text
RGB
```

Possible combinations:

| Binary | Color   |
| ------ | ------- |
| 000    | Black   |
| 001    | Blue    |
| 010    | Green   |
| 011    | Cyan    |
| 100    | Red     |
| 101    | Magenta |
| 110    | Yellow  |
| 111    | White   |

Total colors:

```text
2 × 2 × 2 = 8 Colors
```

or

```text
2^3 = 8 Colors
```

# Modern Color Representation

Using only 8 colors is insufficient.

Modern computers use:

```text
8 bits for Red
8 bits for Green
8 bits for Blue
```

Total:

```text
24 bits
```

or

```text
3 Bytes
```


## Color Formula

```text
RGB = 8 + 8 + 8 bits
```

```text
24 bits total
```

Each color channel:

```text
0 - 255
```


## Total Number of Colors

```text
256 × 256 × 256
```

```text
16,777,216 colors
```

More than 16 million colors.


# Binary Number System

Binary uses only:

```text
0 and 1
```

Base:

```text
Base 2
```

## Binary Place Values

Each position represents a power of 2.

```text
128 64 32 16 8 4 2 1
```

Example:

```text
1001
```

Calculation:

```text
1×8 + 0×4 + 0×2 + 1×1
```

```text
8 + 1
```

```text
9
```

Therefore:

```text
1001₂ = 9₁₀
```

# Common Binary Values

| Binary | Decimal |
| ------ | ------- |
| 0000   | 0       |
| 0001   | 1       |
| 0010   | 2       |
| 0011   | 3       |
| 0100   | 4       |
| 0101   | 5       |
| 0110   | 6       |
| 0111   | 7       |
| 1000   | 8       |
| 1001   | 9       |
| 1010   | 10      |
| 1011   | 11      |
| 1100   | 12      |
| 1101   | 13      |
| 1110   | 14      |
| 1111   | 15      |


# Binary to Decimal Conversion

Formula:

```text
Binary Digit × 2^(Position)
```

Example:

```text
1101
```

Calculation:

```text
1×8 + 1×4 + 0×2 + 1×1
```

```text
8 + 4 + 0 + 1
```

```text
13
```

Therefore:

```text
1101₂ = 13₁₀
```

# Hexadecimal Number System

Hexadecimal uses:

```text
0-9 and A-F
```

Base:

```text
Base 16
```

# Why Hexadecimal?

Binary numbers become very long.

Example:

```text
101000111110101000101010
```

Hexadecimal shortens them:

```text
A3EA2A
```

This makes reading and writing easier.


# Hexadecimal Table

| Decimal | Hex | Binary |
| ------- | --- | ------ |
| 0       | 0   | 0000   |
| 1       | 1   | 0001   |
| 2       | 2   | 0010   |
| 3       | 3   | 0011   |
| 4       | 4   | 0100   |
| 5       | 5   | 0101   |
| 6       | 6   | 0110   |
| 7       | 7   | 0111   |
| 8       | 8   | 1000   |
| 9       | 9   | 1001   |
| 10      | A   | 1010   |
| 11      | B   | 1011   |
| 12      | C   | 1100   |
| 13      | D   | 1101   |
| 14      | E   | 1110   |
| 15      | F   | 1111   |


# Binary ↔ Hex Conversion

Every:

```text
4 Binary Bits
```

becomes:

```text
1 Hex Digit
```

Example:

```text
1111
```

=

```text
F
```

Example:

```text
1111 1111
```

Split into groups:

```text
1111 = F
1111 = F
```

Result:

```text
FF
```

# Hex to Decimal Conversion

Formula:

```text
Digit × 16^(Position)
```

Example:

```text
AB
```

A = 10

B = 11

Calculation:

```text
10×16 + 11×1
```

```text
160 + 11
```

```text
171
```

Therefore:

```text
AB₁₆ = 171₁₀
```

# Color in Hexadecimal

Colors are commonly written as:

```text
#RRGGBB
```

Examples:

```text
#FF0000
```

Red


```text
#00FF00
```

Green


```text
#0000FF
```

Blue


```text
#FFFFFF
```

White


```text
#000000
```

Black


# Octal Number System (Optional)

Octal uses:

```text
0-7
```

Base:

```text
Base 8
```


## Octal Binary Mapping

| Octal | Binary |
| ----- | ------ |
| 0     | 000    |
| 1     | 001    |
| 2     | 010    |
| 3     | 011    |
| 4     | 100    |
| 5     | 101    |
| 6     | 110    |
| 7     | 111    |


# Key Formulas

## Number of States

```text
2^n
```

where n = number of bits

Examples:

```text
1 bit = 2 states
```

```text
2 bits = 4 states
```

```text
3 bits = 8 states
```

```text
8 bits = 256 states
```


## RGB Colors

```text
256 × 256 × 256
```

```text
16,777,216 colors
```


## Byte

```text
1 Byte = 8 Bits
```

## Color Size

```text
RGB = 24 bits = 3 bytes
```

---
