# Created by Carlo Leiva

# DES cryptography 

DES cryptography Encryption and Decryption made from scratch.

The Data Encryption Standard (DES) is a symmetric-key encryption algorithm that encrypts digital data through several key steps:

1. The 64-bit plaintext input is initially permuted using a fixed table. This step rearranges the bits to produce a permuted input that is fed into the main DES algorithm. It's a straightforward, non-encryption step that prepares the data for the subsequent processes.
2. DES uses a single 56-bit key from which it generates 16 subkeys, one for each round of the main encryption process. The original key is first permuted according to a fixed table, then split into two halves. Each half is rotated left by a certain number of positions (which varies for each round), and then a 48-bit subkey is generated from this result by another permutation.
3. 16 Rounds of Processing: Each round includes expansion of the right half of the data, XOR with a subkey, substitution via S-boxes, permutation, and mixing with the left half. This process ensures diffusion and confusion in the data.
4. Final Permutation: Applies the inverse of the initial permutation to the output of the last round to produce the 64-bit ciphertext.
5. Decryption mirrors the encryption process but proceeds in reverse. Initially, the ciphertext undergoes the initial permutation. Following this, it passes through the 16 rounds, utilizing the subkeys in reverse sequence. To conclude, the final permutation is executed, resulting in the recovery of the original plaintext.

Each of these steps is designed to ensure that small changes in the plaintext or the key produce significant changes in the ciphertext, a property known as diffusion. Additionally, the process ensures that the relationship between the plaintext and ciphertext is highly non-linear, contributing to the security of the encrypted message.

how I made the sub keys (the plan I drew)

<img width="500" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/2b2dfa77-33c9-43f1-8e82-1b8e73f56a2d">

## Encryption -
How I did the encryption and bit manipulation process for all 16 rounds .the F-Block is in the red doted box.

<img width="712" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/c77eff00-a2dc-4876-91e3-b3564f5b9e91">

## Decryption -
I intended to execute the decryption using a single round, since I had the initial Right and Left binary outputs along with the first subkey, requiring only their integration in the decrption since its just a miror of the encrption round 1. Despite repeated attempts, a persistent issue arose during the decryption process. After numerous rounds of refactoring, the problem remained unresolved. Consequently, I opted to disclose all my decryption strategies, which I believe to be accurate, and have fully implemented them in my code.

<img width="170" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/9dbabee2-75fa-42dc-b1fb-651402745507">

<img width="453" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/78381a57-b7c4-4ed0-b193-cd9a8d0eaed1">


### Ruining Code -
All the user has to do is run the code since I gave a inital string of 16 hexidecimal and a secret key of lenght 16 hexidecimal aswell to produce a cipher text which will then be decrypted back to the orginal message. (Note:The decryption had issues and I attmepted mutiple times to fix it but for some reason it was not working properly and due to time constrant i was not able to work on it fully due to midterms of outher classes)
<img width="1029" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/f251ab77-2643-4bb8-896d-2bcd3271550b">
<img width="419" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/98d3f287-3bea-4bde-b309-d57c7dd98b52">


## Terminal output (still testing ) -

<img width="612" alt="image" src="https://github.com/Vidacelinda/DES-cryptography/assets/87499194/8d2cabe7-1bc2-4387-9786-5f0a227aeb7f">
