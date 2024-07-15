# Learning Guide: Encryption

- [Learning Guide: Encryption](#learning-guide-encryption)
  - [Introduction](#introduction)
  - [Key Concepts](#key-concepts)
  - [Types of Encryption](#types-of-encryption)
  - [How Encryption Works](#how-encryption-works)
    - [Symmetric Encryption](#symmetric-encryption)
    - [Asymmetric Encryption](#asymmetric-encryption)
  - [Examples](#examples)
    - [Example 1: Symmetric Encryption in C#](#example-1-symmetric-encryption-in-c)
    - [Example 2: Asymmetric Encryption in C#](#example-2-asymmetric-encryption-in-c)
  - [Best Practices](#best-practices)
  - [Summary](#summary)

## Introduction

Encryption is a process that converts plaintext into ciphertext, making it unreadable to anyone who does not have the key to decrypt it. It is essential for protecting sensitive data in transit and at rest.

## Key Concepts

- **Plaintext**: The original readable data.
- **Ciphertext**: The encrypted data.
- **Encryption Key**: A key used to transform plaintext into ciphertext.
- **Decryption Key**: A key used to transform ciphertext back into plaintext.
- **Symmetric Encryption**: The same key is used for both encryption and decryption.
- **Asymmetric Encryption**: Different keys are used for encryption and decryption (public and private keys).

## Types of Encryption

| **Type**               | **Description**                                                                 |
|------------------------|---------------------------------------------------------------------------------|
| **Symmetric Encryption** | Uses a single key for both encryption and decryption. Efficient but requires secure key sharing. |
| **Asymmetric Encryption** | Uses a pair of keys (public and private). The public key encrypts data, and the private key decrypts it. More secure for key exchange. |
| **Hash Functions**       | Converts data into a fixed-size hash value. Primarily used for data integrity and password storage, not reversible. |

## How Encryption Works

### Symmetric Encryption

1. **Key Generation**: A secret key is generated.
2. **Encryption**: The plaintext is encrypted using the secret key.
3. **Decryption**: The ciphertext is decrypted using the same secret key.

### Asymmetric Encryption

1. **Key Pair Generation**: A pair of keys (public and private) is generated.
2. **Encryption**: The plaintext is encrypted using the public key.
3. **Decryption**: The ciphertext is decrypted using the private key.

## Examples

### Example 1: Symmetric Encryption in C#

```csharp
using System;
using System.IO;
using System.Security.Cryptography;
using System.Text;

public class SymmetricEncryptionExample
{
    public static void Main()
    {
        string original = "Sensitive data";
        using (Aes aesAlg = Aes.Create())
        {
            byte[] encrypted = EncryptStringToBytes_Aes(original, aesAlg.Key, aesAlg.IV);
            string decrypted = DecryptStringFromBytes_Aes(encrypted, aesAlg.Key, aesAlg.IV);
            Console.WriteLine($"Original: {original}");
            Console.WriteLine($"Encrypted (b64-encode): {Convert.ToBase64String(encrypted)}");
            Console.WriteLine($"Decrypted: {decrypted}");
        }
    }

    static byte[] EncryptStringToBytes_Aes(string plainText, byte[] Key, byte[] IV)
    {
        if (plainText == null || plainText.Length <= 0) throw new ArgumentNullException("plainText");
        if (Key == null || Key.Length <= 0) throw new ArgumentNullException("Key");
        if (IV == null || IV.Length <= 0) throw new ArgumentNullException("IV");
        byte[] encrypted;

        using (Aes aesAlg = Aes.Create())
        {
            aesAlg.Key = Key;
            aesAlg.IV = IV;
            ICryptoTransform encryptor = aesAlg.CreateEncryptor(aesAlg.Key, aesAlg.IV);
            using (MemoryStream msEncrypt = new MemoryStream())
            {
                using (CryptoStream csEncrypt = new CryptoStream(msEncrypt, encryptor, CryptoStreamMode.Write))
                {
                    using (StreamWriter swEncrypt = new StreamWriter(csEncrypt))
                    {
                        swEncrypt.Write(plainText);
                    }
                    encrypted = msEncrypt.ToArray();
                }
            }
        }
        return encrypted;
    }

    static string DecryptStringFromBytes_Aes(byte[] cipherText, byte[] Key, byte[] IV)
    {
        if (cipherText == null || cipherText.Length <= 0) throw new ArgumentNullException("cipherText");
        if (Key == null || Key.Length <= 0) throw new ArgumentNullException("Key");
        if (IV == null || IV.Length <= 0) throw new ArgumentNullException("IV");
        string plaintext = null;

        using (Aes aesAlg = Aes.Create())
        {
            aesAlg.Key = Key;
            aesAlg.IV = IV;
            ICryptoTransform decryptor = aesAlg.CreateDecryptor(aesAlg.Key, aesAlg.IV);
            using (MemoryStream msDecrypt = new MemoryStream(cipherText))
            {
                using (CryptoStream csDecrypt = new CryptoStream(msDecrypt, decryptor, CryptoStreamMode.Read))
                {
                    using (StreamReader srDecrypt = new StreamReader(csDecrypt))
                    {
                        plaintext = srDecrypt.ReadToEnd();
                    }
                }
            }
        }
        return plaintext;
    }
}
```

### Example 2: Asymmetric Encryption in C#

```csharp
using System;
using System.Security.Cryptography;
using System.Text;

public class AsymmetricEncryptionExample
{
    public static void Main()
    {
        string original = "Sensitive data";
        using (RSACryptoServiceProvider rsa = new RSACryptoServiceProvider())
        {
            string publicKey = rsa.ToXmlString(false);
            string privateKey = rsa.ToXmlString(true);

            byte[] encrypted = Encrypt(original, publicKey);
            string decrypted = Decrypt(encrypted, privateKey);

            Console.WriteLine($"Original: {original}");
            Console.WriteLine($"Encrypted (b64-encode): {Convert.ToBase64String(encrypted)}");
            Console.WriteLine($"Decrypted: {decrypted}");
        }
    }

    static byte[] Encrypt(string data, string publicKey)
    {
        using (RSACryptoServiceProvider rsa = new RSACryptoServiceProvider())
        {
            rsa.FromXmlString(publicKey);
            return rsa.Encrypt(Encoding.UTF8.GetBytes(data), false);
        }
    }

    static string Decrypt(byte[] data, string privateKey)
    {
        using (RSACryptoServiceProvider rsa = new RSACryptoServiceProvider())
        {
            rsa.FromXmlString(privateKey);
            return Encoding.UTF8.GetString(rsa.Decrypt(data, false));
        }
    }
}
```

## Best Practices

| **Practice**                    | **Description**                                                                 |
|---------------------------------|---------------------------------------------------------------------------------|
| **Strong Algorithms**           | Use strong encryption algorithms (e.g., AES, RSA).                              |
| **Key Management**              | Securely store and manage encryption keys.                                      |
| **Regular Key Rotation**        | Rotate encryption keys periodically to minimize the impact of key compromise.   |
| **Use TLS for Data in Transit** | Protect data in transit using TLS.                                              |
| **Encrypt Sensitive Data**      | Always encrypt sensitive data both in transit and at rest.                      |

## Summary

Encryption is a fundamental aspect of data security, ensuring that sensitive information remains confidential and protected from unauthorized access. By understanding the differences between symmetric and asymmetric encryption and following best practices, you can effectively implement encryption in your applications to safeguard data.
