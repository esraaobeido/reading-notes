# Express REST API

## Intro to JWT

**1. What is a JSON Web Token (JWT)?**
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.


**2. When should we use JSON Web Tokens?**
It is mostly used for authentication, authorization, and information exchange.

**3. Claims are expected in which structural component of a JWT?**
In the payload component.

---

## Are JWTs Secure?
**1. If I get a JWT and I can decode the payload, how can we call that secure?**

JWTs can be either signed, encrypted or both. If a token is signed, but not encrypted, everyone can read its contents, but when you don't know the private key, you can't change it. Otherwise, the receiver will notice that the signature won't match anymore, that mean it is secure.

**2. If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.**
- Shared Secret Key : The secret key is used by the sender to sign the JWT and by the receiver to verify the signature.
- Algorithm : Both parties need to support and understand the chosen algorithm.
- Token Structure : The sender and receiver should have a clear understanding of the structure of the JWT.

**3. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.**

In the digital world, the concatenated content could be a message, data, or a JWT. The secret combination could be a password or a shared cryptographic key known to both parties. By combining the content and the secret, the sender can ensure that the information remains secure and only accessible to the intended recipient. The recipient, who possesses the secret, can decrypt or unlock the content, ensuring confidentiality.

---
## JWTs Explained
<br>

**1. Why use JWT?**

There are benefits to using JWTs:
- More compact: JSON is less verbose than XML, so when it is encoded, a JWT is smaller than a SAML token. This makes JWT a good choice to be passed in HTML and HTTP environments.
- More common: JSON parsers are common in most programming languages because they map directly to objects. Conversely, XML doesn't have a natural document-to-object mapping. This makes it easier to work with JWT than SAML assertions.
- Easier to process: JWT is used at internet scale. This means that it is easier to process on users' devices, especially mobile.

**2. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.**

By using a JWT, you can carry your digital identity and relevant information securely and conveniently. It simplifies interactions, reduces the need for external lookups, and ensures that your information remains intact and trustworthy throughout the process.

**3. What are the three components (the structure) of a JWT signature?**

A JWT is a string made up of `three parts`, separated by dots (.), and serialized using base64. In the most common serialization format, compact serialization, the JWT looks something like this: `xxxxx.yyyyy.zzzzz`. 

- Header : Header is comprised of a set of Header Parameters that typically consist of a name/value pair: the hashing algorithm being used (e.g., HMAC SHA256 or RSA) and the type of the JWT.

```
{
      "alg": "HS256",
      "typ": "JWT"
    }
```
- Payload : it contain claims.
````
{
      "sub": "1234567890",
      "name": "John Doe",
      "admin": true
    }
````
- Signature : It is combine base64 Header and base64 Payload with secrest.
```
HMACSHA256(
      base64UrlEncode(header) + "." +
      base64UrlEncode(payload),
      secret)
```