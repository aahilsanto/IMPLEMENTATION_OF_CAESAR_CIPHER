# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:

```python
def caesar_encrypt(text, key):
    result = ""
    for c in text:
        if c.isupper():
            result += chr(((ord(c) - ord('A') + key) % 26 + 26) % 26 + ord('A'))
        elif c.islower():
            result += chr(((ord(c) - ord('a') + key) % 26 + 26) % 26 + ord('a'))
        else:
            result += c
    return result

def caesar_decrypt(text, key):
    return caesar_encrypt(text, -key)

message = input("Enter the message to encrypt: ")
key = int(input("Enter the Caesar Cipher key (an integer): "))

encrypted = caesar_encrypt(message, key)
print(f"Encrypted Message: {encrypted}")

decrypted = caesar_decrypt(encrypted, key)
print(f"Decrypted Message: {decrypted}")
```

## OUTPUT:

<img width="528" height="248" alt="image" src="https://github.com/user-attachments/assets/878a914b-e24d-4d04-8e93-b91b28324977" />


## RESULT:
Thus the implementation of ceasar cipher had been executed successfully.
