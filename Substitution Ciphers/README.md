This code implements a simple substitution cipher encryption/decryption system and demonstrates cryptanalysis using frequency analysis and hill climbing:
- Implemented a random substitution cipher to encrypt plaintext.
- Performed frequency analysis and mapped high-frequency ciphertext letters to common English letters for an initial key guess.
- Applied hill climbing with bigram/trigram scoring to iteratively refine the key and improve plaintext recovery.
- Successfully demonstrated automatic key and plaintext recovery from ciphertext, showcasing classical cryptanalysis techniques.