# Cryptanalysis-Lab
Laboratory projects demonstrating cryptanalysis techniques, cipher vulnerabilities, and practical exploitation in Python.

Project Summary:
This project explores a wide range of cryptography algorithms, encryption schemes, and cryptanalysis techniques, combining classical ciphers, modern symmetric algorithms, and RSA-based attacks. It demonstrates encryption, decryption, key recovery, and security analysis in both theoretical and practical contexts.

Components and Implementations
1. Classical Ciphers
- Substitution Cipher
  - Implements random monoalphabetic substitution.
  - Supports encryption, decryption, and key recovery via frequency analysis and hill-climbing algorithm.
  - Uses unigram, digram, and trigram statistics to improve key guessing.
- Vigenère Cipher
  - Implements polyalphabetic encryption with random or custom keys.
  - Supports key length estimation via Index of Coincidence (IC).
  - Recovers encryption keys using Mutual Index of Coincidence (MIC).
    
2. Symmetric Encryption: RC4 and Double DES
- RC4 Cipher
  - Implements the RC4 algorithm with Key Scheduling Algorithm (KSA) and keystream generator.
  - Demonstrates the bias in the second keystream byte experimentally.
  - Includes FMS attack simulation to recover the first byte of a WEP key from weak IVs.
- Double DES (2DES)
  - Implements DES encryption with two independent keys.
  - Includes Meet-in-the-Middle (MITM) attack demonstration.
  - Shows why 2DES does not provide 112-bit security due to MITM vulnerability.

3. Number-Theoretic Algorithms and Discrete Logarithms
4. -Extended Euclidean Algorithm and modular inverse computation.
- Baby-step Giant-step (BSGS) for discrete logarithms.
- Chinese Remainder Theorem (CRT) for solving simultaneous congruences.
- Pohlig-Hellman Algorithm for computing discrete logarithms modulo composite numbers.

4. RSA Cryptography and Attacks
- Weak RSA key generation
  - Generates RSA keys vulnerable to Wiener’s attack with small private exponents.
- Wiener Attack
  - Recovers private exponent d from a public key (n, e) when d is small.
- CRT Fault Attack (Lenstra)
  - Simulates faulty RSA signatures using CRT.
  - Demonstrates factorization of n using a single faulty signature and public information.

5. Primality Testing and Random Prime Generation
- Miller-Rabin probabilistic primality test.
- Random prime generation for RSA key creation.

6. Experimental and Analytical Features
- Statistical analysis of ciphertexts: frequency, IC, MIC.
- Key recovery using hill-climbing optimization with simulated annealing.
- Demonstrations of cryptanalytic attacks on both classical and modern ciphers.
- Educational insights into cryptography vulnerabilities and practical attacks.

7. File Handling and Text Preprocessing
- Supports input from text files.
- Normalizes plaintext to uppercase letters and removes non-alphabet characters.
- Processes large texts efficiently (up to 100,000 characters in substitution cipher analysis).

Technologies Used:
- Python 3.x
- Libraries: random, string, collections, re, math, secrets

Applications:
- Educational tool for learning cryptography and cryptanalysis.
- Practical demonstrations of attacks on classical ciphers, RC4, 2DES, and RSA.
- Experimental verification of theoretical vulnerabilities (biases, weak keys, faulty signatures).
