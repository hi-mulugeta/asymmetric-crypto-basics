# Asymmetric Cryptography Basics

A clear, practical Node.js implementation of core asymmetric (public-key) cryptography operations using the built-in `crypto` module. This project focuses on understanding the fundamentals of data encryption and digital signatures for identity verification.

## Overview

This repository contains a minimal, educational implementation of RSA-based asymmetric cryptography. It provides functions to generate key pairs, encrypt/decrypt data, and create/verify digital signatures—the foundational building blocks for secure communication and authentication in digital systems.

## Features

- **Key Pair Generation**: Create RSA public/private key pairs.
- **Data Encryption & Decryption**: Encrypt data using a public key and decrypt it with the corresponding private key.
- **Digital Signatures**: Create signatures with a private key and verify them with a public key to ensure data authenticity and integrity.
- **Zero Dependencies**: Built solely with Node.js core modules for transparency and educational clarity.

## Installation & Usage

1.  Clone the repository:
    ```bash
    git clone https://github.com/YOUR_USERNAME/asymmetric-crypto-basics.git
    cd asymmetric-crypto-basics
    ```
2.  The project uses Node.js core modules (`crypto`), so no `npm install` is required.
3.  Run the example scripts to see the core concepts in action:
    ```bash
    node examples/encryption-demo.js
    node examples/signature-demo.js
    ```

## Core Implementation

### 1. Encryption/Decryption

```javascript
// Example: Securing a message
const { publicKey, privateKey } = generateKeyPair();
const secretMessage = "Confidential Data";
const encrypted = encrypt(secretMessage, publicKey);
const decrypted = decrypt(encrypted, privateKey);
console.log(decrypted === secretMessage); // true
```
