# RSA Cryptosystem Demonstration

A Python implementation of the RSA (Rivest–Shamir–Adleman) Cryptosystem demonstrating public key encryption and decryption using prime number validation, modular arithmetic, and ASCII-based plaintext processing.

---

## Project Overview

RSA is one of the most widely used asymmetric cryptographic algorithms.  
This project demonstrates:

- RSA key generation
- Public and private key creation
- Encryption of plaintext messages
- Decryption back to original message
- Prime number validation
- Modular multiplicative inverse using Extended Euclidean Algorithm
- ASCII-based message handling

The program also performs strict input validation to prevent invalid RSA parameters.

---

## Features

- Prime number verification for `p` and `q`
- Validation for invalid and duplicate prime numbers
- Extended Euclidean Algorithm implementation
- Automatic selection of encryption key `e`
- Modular inverse calculation for private key `d`
- ASCII conversion for plaintext processing
- Encryption and decryption of complete strings
- Proper error handling and validation messages
- Prevents plaintext input when RSA parameters are invalid

---

## RSA Algorithm Used

### Key Generation

Given two prime numbers:

```math
p \quad and \quad q
```

Calculate:

```math
n = p \times q
```

```math
\phi(n) = (p-1)(q-1)
```

Choose encryption key:

```math
gcd(e,\phi(n)) = 1
```

Generate decryption key:

```math
d \equiv e^{-1} \pmod{\phi(n)}
```

---

### Encryption

```math
C = M^e \mod n
```

Where:

- `M` = plaintext ASCII value
- `C` = ciphertext

---

### Decryption

```math
M = C^d \mod n
```

---

## Technologies Used

- Python 3
- Mathematical Algorithms
  - Euclidean Algorithm
  - Extended Euclidean Algorithm
  - Modular Arithmetic

---

## Project Structure

```text
RSA-Cryptosystem/
│
├── rsa.py
├── README.md
```

---

## How to Run

### Step 1: Clone Repository

```bash
git clone https://github.com/aayushbhardwaj003/RSA-Cryptosystem.git
```

### Step 2: Open Project Folder

```bash
cd RSA-Cryptosystem
```

### Step 3: Run Program

```bash
python rsa.py
```

---

## Sample Execution

```text
Enter prime number p: 11
Enter prime number q: 13

RSA Key Generation Successful
--------------------------------
Public Key (e, n):  (7, 143)
Private Key (d, n):  (103, 143)

Enter plaintext message: HELLO

Encrypted Ciphertext:
[19, 108, 54, 54, 40]

Decrypted Message:
HELLO
```

---

## Input Validations Included

The program checks:

- Integer input validation
- Prime number validation
- Positive number validation
- Duplicate prime number restriction
- Minimum prime size check
- Empty plaintext validation
- ASCII value compatibility with RSA modulus `n`

If invalid values are entered, RSA execution stops immediately.

---

## Learning Outcomes

This project helps in understanding:

- Public key cryptography
- RSA encryption and decryption process
- Importance of prime numbers in cryptography
- Modular arithmetic operations
- ASCII-based encryption techniques
- Secure key generation concepts

---

## Future Improvements

- Large prime number generation
- GUI-based RSA simulator
- File encryption support
- Digital signature implementation
- Secure padding techniques
- Multi-block message encryption

---

##Images
![Output1](images/output1.png)
![Output2](images/output2.png)
![Output3](images/output3.png)

---

## Author

**Aayush Bhardwaj**

GitHub: https://github.com/aayushbhardwaj003

---
```