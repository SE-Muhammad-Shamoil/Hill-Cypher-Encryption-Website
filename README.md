# Hill Cypher Encryption Website

A modern web application for encrypting and decrypting messages using the Hill Cipher algorithm, a polygraphic substitution cipher based on linear algebra.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Hill Cipher Algorithm](#hill-cipher-algorithm)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Technology Stack](#technology-stack)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Contributing](#contributing)
- [License](#license)

## 📖 Overview

This project provides an interactive web-based interface for the Hill Cipher encryption algorithm. The Hill Cipher is a block cipher that encrypts plaintext in blocks and uses matrix multiplication for encryption and decryption. This tool makes it easy to understand and experiment with this classical cryptographic technique.

## ✨ Features

- **Encrypt & Decrypt**: Convert plaintext to ciphertext and vice versa using Hill Cipher
- **Interactive UI**: User-friendly interface for easy encryption/decryption
- **Real-time Processing**: Instant encryption and decryption results
- **Educational**: Learn how the Hill Cipher algorithm works with visual feedback
- **Customizable Keys**: Generate or input your own encryption key matrices
- **Copy to Clipboard**: Easily copy encrypted or decrypted text
- **Input Validation**: Automatic validation of input parameters

## 🔐 Hill Cipher Algorithm

The Hill Cipher is a polygraphic substitution cipher where:

- **Encryption Formula**: C = (P × K) mod 26
  - C: Ciphertext
  - P: Plaintext block (as a vector)
  - K: Key matrix
  - mod 26: Operations performed modulo 26 (for 26 letters in the English alphabet)

- **Decryption Formula**: P = (C × K⁻¹) mod 26
  - Requires computing the modular inverse of the key matrix

### Characteristics:

- Block-based encryption (typically 2×2 or 3×3 matrices)
- Requires the key matrix to be invertible (determinant ≠ 0 mod 26)
- Provides better security than simple substitution ciphers
- Vulnerable to known plaintext attacks

## 🚀 Getting Started

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/SE-Muhammad-Shamoil/Hill-Cypher-Encryption-Website.git
   cd Hill-Cypher-Encryption-Website
   ```

2. **Open the application**:
   - Open `index.html` in your web browser
   - No additional dependencies or installation required!

### Usage

1. **Input Your Text**: Enter the plaintext you want to encrypt or ciphertext to decrypt
2. **Set Key Matrix**: Input your 2×2 or 3×3 key matrix values
3. **Encrypt/Decrypt**: Click the respective button to process your text
4. **View Results**: See the encrypted/decrypted output
5. **Copy Results**: Use the copy button to easily save the output

## 📁 Project Structure

```
Hill-Cypher-Encryption-Website/
├── index.html          # Main HTML structure
├── style.css          # Styling and UI components
├── script.js          # Encryption/decryption logic
├── README.md          # Documentation (this file)
└── assets/            # Optional images and icons
```

## 🛠 Technology Stack

- **Frontend**: HTML, CSS, JavaScript
- **Algorithm**: Linear algebra-based Hill Cipher implementation
- **Browser Compatibility**: Works on all modern browsers (Chrome, Firefox, Safari, Edge)

## 🔄 How It Works

### Encryption Process:
1. Convert plaintext to numbers (A=0, B=1, ..., Z=25)
2. Split text into blocks (matching key matrix size)
3. Multiply each block by the key matrix
4. Apply modulo 26 to results
5. Convert back to letters

### Decryption Process:
1. Convert ciphertext to numbers
2. Calculate the modular inverse of the key matrix
3. Multiply ciphertext blocks by the inverse matrix
4. Apply modulo 26 to results
5. Convert back to letters

## 📝 Example

**Plaintext**: "HELLO"  
**Key Matrix** (2×2):
```
[17  8]
[3  19]
```

**Ciphertext**: (result of encryption process)

## ⚙️ Technical Details

- **Language Composition**: 64.6% JavaScript, 35.4% HTML, CSS
- **Block Size**: Configurable (default 2×2 matrix)
- **Character Set**: English alphabet (A-Z)
- **Modulus**: 26 (for English letters)

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add improvement'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Open a Pull Request

## 📚 Learning Resources

- [Hill Cipher on Wikipedia](https://en.wikipedia.org/wiki/Hill_cipher)
- Linear Algebra basics for cryptography
- Modular arithmetic concepts

## ⚠️ Disclaimer

This implementation is for **educational purposes only**. The Hill Cipher is a classical cipher and is not secure for protecting sensitive information in production environments. For real-world security needs, use modern cryptographic standards like AES.

## 📧 Contact & Support

For questions or issues, please open a GitHub issue or contact the project maintainer.

---

**Happy Encrypting! 🎓**
