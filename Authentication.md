# Authentication
## Securing Passwords
1- Explain to a non-technical friend how you would safely hash and store a password.
- When you sign up for a service or create an account, the website takes your password, runs it through hashing algorithm, and stores the resulting hashed password in its database.

2- What is Bcrypt?
- Bcrypt is an algorithm that will allow your application to take the user inputted password and convert it into a hash, which can be thought of as a "digital fingerprint."

3- Why might you use something like Bcrypt?
- bcrypt is good for password hashing as it reduces the number of passwords by second an attacker could hash when ceafting a dictionary attack
---

## Basic Auth
1- What is Basic Authentication?
- is a method for an HTTP user agent to provide a user name and password when making a request.

2- What properties are necessary in the header of a Basic Auth request?
- The request contains a header field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of ID and password joined by a single colon : .

3- How are username:password in Basic Auth encoded?
- Concatenate username and password into a string with a colon between as shown: “username:password”
- Encode the resulting string in a Base64 variant
- Prefix the encoded string with “Basic ”; the space after Basic is required.

---
## OWASP auth cheatsheet
1- Define the authentication process to a non-technical recruiter.
- Authentication is the process of verifying the identity of someone. It is like showing your identification to prove who you are before being allowed to enter a restricted area or access certain information.

2- How should your error messaging respond (both HTTP and HTML)? Why?
- HTTP Error Responses: 
There are some status codes include 400 (Bad Request), 401 (Unauthorized), 404 (Not Found), and 500 (Internal Server Error). These codes help both the client and server understand what went wrong.
When an HTTP error occurs, it's crucial to include a meaningful error message in the response body. The error message should provide clear and concise information about the issue that occurred.
- HTML Error Messages: 
Error messages should be displayed prominently in a visually distinct manner so that users can easily identify them. This can include using different colors, icons, or even pop-up dialogs to grab attention.


### Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.
https://www.npmjs.com/package/bcrypt