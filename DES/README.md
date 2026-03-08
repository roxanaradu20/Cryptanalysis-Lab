The script contains three main parts:

1) Implementation of Data Encryption Standard(DES) from scratch:
- key schedule (determine_16_subkeys)
- Feistel rounds
- S‑boxes
- permutations
- encryption and decryption

2) Implementation of Double DES(2DES) by applying DES encryption twice using 2 separate keys. While it was originally assumed to provide double the security, it is vulnerable to a Meet-in-the-Middle attack, so the effective security is much lower.

3) Meet-in-the-Middle(MITM) attack:
The function MITM_attack(plaintext, ciphertext) implements the Meet-in-the-Middle attack. The idea is: instead of brute-forcing both keys simultaneously (2^56 × 2^56 = 2^112), the attacker first encrypts the plaintext with all possible values of the first key k1 and stores the results in a table. Then, the attacker decrypts the ciphertext with all possible values of the second key k2 and checks if any result matches an entry in the table. If a match is found, the corresponding (k1, k2) pair is a candidate key.
This approach reduces the number of operations from 2^112 (full brute force) to approximately 2^56 + 2^56. Due to this vulnerability, Double DES does not provide 112-bit security as initially expected. 