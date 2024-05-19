# JSON Web Tokens (JWTs)

**Definition**:
JSON Web Tokens (JWTs) are a compact, URL-safe means of representing claims to be transferred between two parties. The claims in a JWT are encoded as a JSON object that is used as the payload of a JSON Web Signature (JWS) structure or as the plaintext of a JSON Web Encryption (JWE) structure, enabling the claims to be digitally signed or integrity protected with a Message Authentication Code (MAC) and/or encrypted.

## Structure of JWT

A JWT consists of three parts, separated by dots (`.`):

1. **Header**: 
   - **Algorithm and Token Type**: Typically specifies the signing algorithm and token type.
   - Example:
     ```json
     {
       "alg": "HS256",
       "typ": "JWT"
     }
     ```

2. **Payload**:
   - **Claims**: Contains the claims. There are three types of claims: registered, public, and private.
   - Example:
     ```json
     {
       "sub": "1234567890",
       "name": "John Doe",
       "iat": 1516239022
     }
     ```

3. **Signature**:
   - **Verification**: Ensures the token's integrity and authenticity.
   - Example:
     ```plaintext
     HMACSHA256(
       base64UrlEncode(header) + "." +
       base64UrlEncode(payload),
       secret
     )
     ```

The resulting JWT looks like this:
```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c
```

## Types of Claims

1. **Registered Claims**:
   - Predefined claims which are not mandatory but recommended, to provide a set of useful, interoperable claims.
   - Examples: `iss` (issuer), `exp` (expiration time), `sub` (subject), `aud` (audience).

2. **Public Claims**:
   - Claims that can be defined at will by those using JWTs.
   - Should be collision-resistant or be defined in the IANA JSON Web Token Registry to avoid collisions.

3. **Private Claims**:
   - Custom claims agreed upon between parties sharing the JWTs.

## Use Cases

- **Authentication**: Commonly used in authentication mechanisms. Upon successful login, a server generates a JWT and sends it to the client. The client then sends this token in subsequent requests, typically in the `Authorization` header with a `Bearer` scheme.
- **Information Exchange**: Securely transmit information between parties. The integrity and authenticity of the information can be verified.
- **Authorization**: Manage user permissions and access control.

## Example Workflow

```mermaid
sequenceDiagram
    participant User
    participant Server

    User->>Server: User Login
    Server->>Server: Generate JWT
    Server-->>User: Send JWT
    User->>User: Store JWT
    User->>Server: Include JWT in request
    Server->>Server: Verify JWT
    Server-->>User: Response
```

## Advantages and Disadvantages

| **Aspect**                    | **Advantages**                                                                                      | **Disadvantages**                                                                                   |
|-------------------------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| **Compact**                   | Small size makes them efficient to transmit over HTTP.                                              | Can become large if too many claims are included.                                                   |
| **Self-contained**            | Contains all necessary information about the user, reducing the need for database lookups.          | Sensitive information must be handled carefully to avoid exposure.                                  |
| **Stateless**                 | Server does not need to store session information, reducing server-side complexity.                 | Token revocation is challenging because tokens are stateless and self-contained.                    |
| **Scalable**                  | Suitable for distributed systems and microservices architectures.                                   | Must ensure tokens are securely stored and managed on the client side to prevent security issues.   |
| **Secure**                    | Can be signed and encrypted to ensure integrity and confidentiality.                                | Proper implementation is critical to prevent vulnerabilities like token tampering and misuse.       |

## Summary

**JSON Web Tokens (JWTs)** are a versatile and secure way to transmit information between parties, commonly used for authentication and authorization purposes. They are compact, self-contained, and stateless, making them well-suited for modern web applications and microservices architectures. However, careful handling and implementation are crucial to maintain security and prevent common pitfalls such as token tampering and misuse.