# Cryptography Fundamentals

## What is Cryptography?

Cryptography is the practice of protecting information by converting readable data into an unreadable format so that only authorized people can access it.

It helps protect:

* Confidentiality
* Integrity


# Why Cryptography Matters

Data travels through many devices and networks before reaching its destination.

Without cryptography, attackers could:

* Read the data
* Modify the data
* Steal sensitive information

Cryptography protects data while it is being transmitted.


# Key Terms

## Plaintext

Readable and understandable data.

Example:

```text
HELLO
Patient Name: Alice Smith
```

## Ciphertext

Scrambled and unreadable version of data.

Example:

```text
KHOOR
```

Only someone with the correct key can convert it back to plaintext.


## Key

A secret value used during encryption and decryption.

Think of it as a password that controls the encryption process.

Example:

```text
Key = 3
```

## Algorithm

A set of rules or steps used to encrypt and decrypt data.

Important:

```text
Algorithm = Public
Key = Secret
```

Security depends on protecting the key, not hiding the algorithm.


# Encryption Process

```text
Plaintext + Algorithm + Key
            ↓
       Ciphertext
```

Example:

```text
HELLO
  ↓
KHOOR
```


# Decryption Process

```text
Ciphertext + Algorithm + Key
             ↓
         Plaintext
```

Example:

```text
KHOOR
  ↓
HELLO
```


# Caesar Cipher

## Definition

A simple encryption method that shifts each letter by a fixed number of positions.

Example:

```text
Key = 3

A → D
B → E
C → F
```


## Example

Plaintext:

```text
HELLO
```

Encryption using key 3:

```text
H → K
E → H
L → O
L → O
O → R
```

Ciphertext:

```text
KHOOR
```


## Decryption

```text
K → H
H → E
O → L
O → L
R → O
```

Result:

```text
HELLO
```


# Symmetric Encryption

## Definition

The same key is used for both encryption and decryption.

```text
Encrypt  → Same Key
Decrypt  → Same Key
```


## Characteristics

### Advantages

* Fast
* Efficient
* Suitable for large amounts of data

### Disadvantages

* Key distribution problem
* Both parties need the same secret key


## Lockbox Analogy

```text
One key locks the box.
The same key unlocks the box.
```

Alice and Bob both need identical copies of the key.


# Key Distribution Problem

Problem:

```text
How can Alice and Bob safely share the secret key?
```

If an attacker obtains the key, all encrypted messages can be read.

This is the biggest weakness of symmetric encryption.



# Asymmetric Encryption

## Definition

Uses two different keys:

1. Public Key
2. Private Key


## Public Key

Can be shared with everyone.

Used for:

```text
Encryption
```


## Private Key

Must remain secret.

Used for:

```text
Decryption
```


## Rule

```text
Encrypt with Public Key
Decrypt with Private Key
```

Example:

```text
Alice encrypts using Bob's Public Key.
Only Bob's Private Key can decrypt it.
```


# Mailbox Analogy

Public Key:

```text
Mailbox slot
Anyone can put letters inside.
```

Private Key:

```text
Mailbox key
Only the owner can open it.
```



# How Asymmetric Encryption Solves the Problem

1. Bob creates Public Key and Private Key.
2. Bob shares Public Key.
3. Alice encrypts using Bob's Public Key.
4. Bob decrypts using his Private Key.

No secret key needs to be exchanged.



# HTTPS and Cryptography

When visiting a website:

1. Browser requests website's Public Key.
2. Website sends Public Key inside a Certificate.
3. Browser and website securely create a shared symmetric key.
4. Communication continues using symmetric encryption.



# Certificates

## Definition

A digital document that proves ownership of a Public Key.

Contains:

* Public Key
* Website Identity
* Certificate Authority Signature



## Certificate Authority (CA)

A trusted organization that verifies website identities and signs certificates.

Browsers trust certificates issued by trusted CAs.



# Symmetric vs Asymmetric Encryption

| Feature     | Symmetric            | Asymmetric                  |
| ----------- | -------------------- | --------------------------- |
| Keys        | One Key              | Public + Private Key        |
| Speed       | Fast                 | Slower                      |
| Key Sharing | Difficult            | Easy                        |
| Usage       | Bulk Data Encryption | Key Exchange & Certificates |



# Real-World Usage

Modern systems use both methods.

### Step 1

Asymmetric Encryption:

```text
Securely exchange a symmetric key.
```

### Step 2

Symmetric Encryption:

```text
Encrypt all communication.
```

Used in:

* HTTPS
* VPNs
* Secure Messaging Apps

