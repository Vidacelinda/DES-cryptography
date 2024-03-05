#Created by Carlo Leiva

#DES cryptography

project on github 
https://github.com/Vidacelinda/DES-cryptography

DES cryptography Encryption and Decryption made from scratch.

The Data Encryption Standard (DES) is a symmetric-key encryption algorithm that encrypts digital data through several key steps:

1. Initial Permutation (IP): Rearranges the 64-bit plaintext input using a fixed table to prepare for encryption.
2. Subkey Generation: Generates 16 subkeys from the main 56-bit key through permutations and shifts, one for each encryption round.
3. 16 Rounds of Processing: Each round includes expansion of the right half of the data, XOR with a subkey, substitution via S-boxes, permutation, and mixing with the left half. This process ensures diffusion and confusion in the data.
4. Final Permutation: Applies the inverse of the initial permutation to the output of the last round to produce the 64-bit ciphertext.
5. Decryption: Follows the encryption steps in reverse order, using the subkeys in reverse to retrieve the original plaintext.

Each of these steps is designed to ensure that small changes in the plaintext or the key produce significant changes in the ciphertext, a property known as diffusion. Additionally, the process ensures that the relationship between the plaintext and ciphertext is highly non-linear, contributing to the security of the encrypted message.

how I made the sub keys (the plan I drew)

<img width="500" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/2b2dfa77-33c9-43f1-8e82-1b8e73f56a2d">


How I did the encryption and bit manipulation process . (F Block is in the orange doted)

<img width="732" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/5e7afe39-413b-4d32-a5e7-c34fe68f8f14">

My plan for the decryption was to use one round since I had the first Right and first Left binary output along with the first sub key so all i had to do was plug it in.

<img width="170" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/9dbabee2-75fa-42dc-b1fb-651402745507">



Terminal output 

<img width="612" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/8d2cabe7-1bc2-4387-9786-5f0a227aeb7f">
