The script contains 3 main parts:
1) Implementation of the RC4 cipher
Function RC4_Init(key) effectuates the Key Scheduling Algorithm (KSA) and RC4_Keystream_Generator(data_len, S) implements the Pseudo-Random Generation Algorithm (PRGA) of RC4.

2) Demonstration of the second‑byte bias in RC4’s keystream
The second keystream byte is more likely to be 0x00 than expected.
In an ideal stream cipher, each byte of the keystream is uniformly distributed, so the probability of any specific byte (including 0x00) is: P(byte = 0x00)= 1/256 ≈ 0.00391.
However, RC4 exhibits a known bias in the second byte of the keystream. Experiments show that the probability of the second byte being 0x00 is roughly: P(second byte = 0x00) ≈ 0.006
This means that 0x00 is about 50% more likely to appear than in a uniform distribution, demonstrating a subtle but exploitable vulnerability in RC4.

3) Simulation of the Fluhrer–Mantin–Shamir attack used against WEP
The FMS attack exploits weaknesses in the key scheduling algorithm of RC4 when used in the WEP protocol. In WEP, the RC4 key for each packet is formed by concatenating a 3‑byte Initialization Vector (IV) with the secret key. Certain weak IVs of the form (3, 255, V) cause biases in the first byte of the RC4 keystream, leaking information about the first byte of the secret key. By collecting many packets that use these weak IVs and analyzing the resulting keystream bytes, an attacker can statistically recover the first byte of the WEP key and eventually reconstruct the entire key.