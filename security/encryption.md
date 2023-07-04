# Encryption

## Definition

Encryption is used to protect data from being stolen, changed, or compromised and works by scrambling data into a secret code that can only be unlocked with a unique digital key.

Encrypted data can be protected while at rest on computers or in transit between them, or while being processed, regardless of whether those computers are located on-premises or are remote cloud servers.

## How does encryption work?

- Encryption takes plain text, like a text message or email, and scrambles it into an unreadable format — called “cipher text.” This helps protect the confidentiality of digital data either stored on computer systems or transmitted through a network like the Internet. 
- When the intended recipient accesses the message, the information is translated back to its original form. This is called decryption. 
- To unlock the message, both the sender and the recipient have to use a “secret” encryption key — a collection of algorithms that scramble and unscramble data back to a readable format. 

## What are the three types of encryption?

- DES, AES, and RSA are the three primary encryption types. A more recent 3DES is a block cipher that is still in use today. 
- The Triple Data Encryption Standard (3DES) does exactly what its name says. For triple protection, it employs three independent 56-bit keys rather than a single 56-bit key. 
- The Advanced Encryption Standard (AES) is used for confidential communications by governments, security groups, and common enterprises. 
- "Rivest-Shamir-Adleman," or RSA, is another common encryption system. It is frequently used to encrypt data transferred over the internet and depends on a public key to do so. Those receiving the data will be given their own private key to decode the communications.

## Symmetric vs Asymmetric Encryption

| Area | Symmetric | Asymmetric |
| ---- | --------- | ---------- |
| Keys | Uses a single key | Uses a pair of keys |
| Speed | Faster encryption process. | Slower encryption process. |
| Key Length | The length of the keys used are typically 128, 192, or 256 bits. | The length of the keys used are typically 1024 or 2048 bits. |
| Function | Transfers large chunks of data. | Transfers smaller chunks of data to authenticate and establish a secure communication channel prior to the actual data transfer. |
| Security | Sharing a single key among multiple users increases the risk of data theft. | No need to share keys. Two keys are separately made for encryption and decryption, improving overall security.  |
| Used for | Wireless networks, VPNs, and SSL. | SSH, SSL, and TLS. |

### Symmetric Encryption

![Symmetric Encryption](https://ico.org.uk/media/images/other/2260256/symmetric.gif)

### Asymmetric Encryption

![Asymmetric Encryption](https://ico.org.uk/media/images/other/2260261/asymmetric.gif)

## Sources

- <https://cloud.google.com/learn/what-is-encryption>
- <https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/security/encryption/what-types-of-encryption-are-there>
- <https://www.simplilearn.com/data-encryption-methods-article>
- <https://us.norton.com/blog/privacy/what-is-encryption>