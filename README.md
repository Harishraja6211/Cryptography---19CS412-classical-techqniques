Name:Harish
Reg no:212223220031
Hill Cipher
Hill Cipher using with different key values

AIM:
To develop a simple C program to implement Hill Cipher.

DESIGN STEPS:
Step 1:
Design of Hill Cipher algorithnm

Step 2:
Implementation using C or pyhton code

Step 3:
Testing algorithm with different key values.

PROGRAM:
PROGRAM:

def vigenere_encrypt(plaintext, key):
    key = key.upper()
    plaintext = plaintext.upper()
    encrypted_text = ""
    
    for i in range(len(plaintext)):
        if plaintext[i].isalpha():
            shift = ord(key[i % len(key)]) - ord('A')
            encrypted_text += chr((ord(plaintext[i]) - ord('A' )+ shift) % 26 + ord('A'))
        else:
            encrypted_text += plaintext[i]

    return encrypted_text

key = "KEY"
message = "HELLO WORLD"
encrypted = vigenere_encrypt(message, key)
print("Encrypted Message:", encrypted)
OUTPUT:
OUTPUT: image

RESULT:
The program is executed successfully
