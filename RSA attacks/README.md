This project demonstrates RSA key generation, vulnerabilities, and cryptographic attacks. It covers both theoretical and practical aspects of number-theoretic cryptanalysis.
Key features include:
- Prime generation & primality testing: Probabilistic Miller–Rabin test and random prime generation for RSA keys.
- Weak RSA keys & Wiener's attack: Generates RSA keys with small private exponent d and recovers d using continued fractions.
- Standard RSA with CRT: Implements RSA key generation and signing using Chinese Remainder Theorem for efficiency.
- Faulty RSA-CRT signatures & Lenstra attack: Simulates hardware faults during CRT signing and recovers prime factors from a single faulty signature.
- Demonstrations: Encrypts/decrypts messages, tests Wiener's attack, and shows factor recovery from faulty signatures.

This project illustrates how implementation choices and hardware faults can compromise RSA security, highlighting the importance of proper key selection and secure implementations.