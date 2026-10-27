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
```
#include <stdio.h> 
#include <string.h> 
void encrypt(char text[], int key) { 
 for (int i = 0; text[i] != '\0'; i++) { 
 if (text[i] >= 'A' && text[i] <= 'Z') 
 text[i] = (text[i] - 'A' + key) % 26 + 'A'; 
 else if (text[i] >= 'a' && text[i] <= 'z') 
 text[i] = (text[i] - 'a' + key) % 26 + 'a'; 
 } 
} 
void decrypt(char text[], int key) { 
 for (int i = 0; text[i] != '\0'; i++) { 
 if (text[i] >= 'A' && text[i] <= 'Z') 
 text[i] = (text[i] - 'A' - key + 26) % 26 + 'A'; 
 else if (text[i] >= 'a' && text[i] <= 'z') 
 text[i] = (text[i] - 'a' - key + 26) % 26 + 'a'; 
 } 
} 
int main() { 
 char text[100]; 
 int key; 
 printf("Enter text: "); 
 fgets(text, sizeof(text), stdin); 
 printf("Enter key: "); 
 scanf("%d", &key); 
 encrypt(text, key); 
 printf("Encrypted Text: %s", text); 
 decrypt(text, key); 
 printf("Decrypted Text: %s", text); 
 return 0; 
}
```
## OUTPUT:
<img width="348" height="265" alt="Screenshot 2026-10-22 092219" src="https://github.com/user-attachments/assets/844a035e-bc31-4076-96b3-254614174193" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
