# Character Encoding Notes

## What is Character Encoding?

Computers store everything as numbers and bits.

Character Encoding is a standard that maps:

```text
Character ↔ Number ↔ Binary
```

Example:

```text
A → 65 → 01000001
```

Without encoding, computers would not know which number represents which character.

# Representation vs Encoding

## Representation

How data is stored inside a computer.

Example:

```text
01000001
```


## Encoding

Rules that define what the stored number means.

Example:

```text
65 = A
```


# ASCII

ASCII stands for:

```text
American Standard Code for Information Interchange
```

Created in:

```text
1963
```


## Features

* Uses 7 bits
* Supports 128 characters
* Values range from:

```text
0 - 127
```

Supports:

* English letters
* Digits
* Punctuation symbols
* Control characters



# Common ASCII Values

| Character | Decimal | Hex |
| --------- | ------- | --- |
| A         | 65      | 41  |
| B         | 66      | 42  |
| Z         | 90      | 5A  |
| a         | 97      | 61  |
| b         | 98      | 62  |
| z         | 122     | 7A  |
| 0         | 48      | 30  |
| 9         | 57      | 39  |
| @         | 64      | 40  |
| #         | 35      | 23  |


# ASCII Example

Word:

```text
TryHackMe
```

ASCII Hex:

```text
54 72 79 48 61 63 6B 4D 65
```

ASCII Binary:

```text
01010100
01110010
01111001
01001000
01100001
01100011
01101011
01001101
01100101
```

# Limitations of ASCII

ASCII only supports English characters.

Cannot properly represent:

```text
ñ
€
あ
ب
😊
```


# Extended ASCII

Uses:

```text
8 bits
```

Provides:

```text
256 characters
```

Examples:

* ISO-8859-1 (Latin-1)
* ISO-8859-2 (Latin-2)

Problem:

Different systems may display characters incorrectly if different encodings are used.

Example:

```text
Saved in Latin-1
Opened in Latin-2
```

Result:

```text
Gibberish characters
```


# Unicode

Unicode is a universal character standard.

Purpose:

```text
One encoding system for all languages.
```

Every character gets a unique code point.

Format:

```text
U+XXXX
```

Examples:

| Character | Unicode |
| --------- | ------- |
| A         | U+0041  |
| Ω         | U+03A9  |
| あ         | U+3042  |
| ت         | U+062A  |
| ☕         | U+2615  |
| 😊        | U+1F60A |


# Benefits of Unicode

* Supports all major languages
* Supports symbols
* Supports emojis
* Eliminates encoding conflicts
* Allows multilingual text

# Unicode Examples

## Latin

```text
A = U+0041
```

## Greek

```text
Ω = U+03A9
```

## Japanese

```text
あ = U+3042
```

## Chinese

```text
龍 = U+9F8D
```

## Arabic

```text
ت = U+062A
```

## Emoji

```text
😊 = U+1F60A
```


# UTF

UTF means:

```text
Unicode Transformation Format
```

UTF converts Unicode characters into bytes for storage and transmission.

Main types:

```text
UTF-8
UTF-16
UTF-32
```


# UTF-8

Most common encoding on the Internet.

Uses:

```text
1 to 4 bytes
```

Advantages:

* Space efficient
* Compatible with ASCII
* Most websites use UTF-8

Examples:

```text
A → 1 byte
Ω → 2 bytes
😊 → 4 bytes
```


# UTF-16

Uses:

```text
2 or 4 bytes
```

Examples:

```text
A → U+0041
```

```text
😊 → U+D83D U+DE0A
```

Advantages:

* Good balance between size and compatibility


# UTF-32

Uses:

```text
4 bytes for every character
```

Examples:

```text
A → U+00000041
```

```text
😊 → U+0001F60A
```

Advantages:

* Simple

Disadvantage:

* Uses more memory


# Comparison

| Encoding | Bytes Used |
| -------- | ---------- |
| UTF-8    | 1–4 Bytes  |
| UTF-16   | 2–4 Bytes  |
| UTF-32   | 4 Bytes    |


# Common Unicode Characters

| Character | Unicode |
| --------- | ------- |
| ☕         | U+2615  |
| ♘         | U+2658  |
| ♞         | U+265E  |
| ツ         | U+30C4  |
| シ         | U+30B7  |
| 😌        | U+1F60C |
| 😊        | U+1F60A |


# Why Gibberish Appears?

Occurs when:

```text
File saved using one encoding
File opened using another encoding
```

Example:

```text
Saved: ISO-8859-1
Opened: ISO-8859-2
```

Result:

```text
Incorrect characters displayed
```

This is called:

```text
Character Encoding Mismatch
```

---
