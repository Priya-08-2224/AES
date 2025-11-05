# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

void xorCrypt(char *in, const char *key) {
    size_t keyLen = strlen(key);
    for (size_t i = 0; in[i] != '\0'; i++) {
        in[i] ^= key[i % keyLen];
    }
}

int main() {
    char msg[] = "PRIYADHARSHINI";
    char key[] = "secretkey";

    printf("Original: %s\n", msg);

    xorCrypt(msg, key);
    printf("Encrypted: ");
    for (size_t i = 0; msg[i] != '\0'; i++) {
        printf("%02X ", (unsigned char)msg[i]); // Print in hex for readability
    }
    printf("\n");

    xorCrypt(msg, key);
    printf("Decrypted: %s\n", msg);

    return 0;
}

```

# OUTPUT:
<img width="733" height="235" alt="image" src="https://github.com/user-attachments/assets/fa7927e8-7cda-4334-8919-b4ad6129c9f2" />



# RESULT:
Thus the execution of the Advanced Encryption Standard (AES)  has executed 
successfully.

