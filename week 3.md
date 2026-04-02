Week 3  

Week 3 – Modern Encryption (DES, AES and Modes) 
 
## Topic 
This week I learned about modern encryption using DES and AES, and how encryption modes like ECB and CBC work. 
 
## What I Did 
I created a message and encrypted it using OpenSSL in Linux. 
For example, I encrypted a file using DES and AES: 
openssl enc -e -des-cbc -in file1.txt -out file1.enc -k key  
openssl enc -e -aes-192-cbc -in file1.txt -out file1.enc -k key -iv iv 
<img width="610" height="636" alt="image" src="https://github.com/user-attachments/assets/9b422de7-1887-40e6-bc20-d9effef957c1" />
I also generated a key using: 
 
openssl rand -hex 8  
 
After encrypting, I viewed the encrypted content using tools like `xxd`, which showed the message in hexadecimal format. 
 
Then I used the same key to decrypt the file and recover the original message.
<img width="585" height="307" alt="image" src="https://github.com/user-attachments/assets/b5952cc3-4665-44e9-9a85-cc2b7cc65e82" />
My Understanding 
Encryption converts readable text into unreadable data using a key.  
The key is required to decrypt and get the original message back. 
 
AES is more secure than DES, and is widely used today.  
Encryption modes like CBC improve security by hiding patterns. 
 
## Difficulties 
I found it confusing to understand how the key and IV work together.  
Also, reading encrypted data in hexadecimal format was not easy at first. 
 
## Security Insight 
If the key is weak or exposed, the encrypted message can be decrypted by an attacker.  
DES is insecure because of its small key size, while AES is stronger. 
 
ECB mode can leak patterns, while CBC is more secure. 
 
## Insight 
This week helped me understand how real encryption works in practice.  
Creating a message, encrypting it, and then decrypting it showed me how important key management is in cybersecurity. 

Reflection 
 
The most difficult part this week was understanding how keys and IV values are used in encryption. I improved by testing commands and seeing how changing values affects the output. 
 
AES is more secure than DES because it uses stronger keys. DES can be broken with brute force, while AES is still secure in real systems. 
 
Possible attacks include brute force on weak keys and pattern analysis in ECB mode. These attacks work if encryption is not implemented properly, but using AES with secure modes makes them much harder. 
