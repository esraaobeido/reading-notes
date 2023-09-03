# API Integration

## Review API Server Build

**Explain the different between a query string parameter and a path parameter.**

The path parameter defines the resource location, while the query parameter defines sort, pagination, or filter operations. The user's input (the query) is passed as a variable in the query parameter, while each path parameter must be substituted with an actual value when the client makes an API call.

**What would our API URL with a path id parameter be given the following information:**
**Domain: http://our-site.com**
**v3**
**model name: stuff**
**id: things**

http://our-site.com/v3/stuff/things

**We have created a dynamic API with an “interface”. Describe how that interface works to a non-technical friend.**
Think of our dynamic API with an "interface" as a versatile toolbox. When we need a specific tool, we open the box, and it gives us exactly what we asked for. If we need a hammer, it provides a hammer, It's like having a toolbox that magically knows what tool to hand us based on what we want to do.

---
## Review Auth Server Build

**Describe how you would use middleware to implement basic and bearer auth.**

Using Middleware for Basic and Bearer Authentication:

In our Express/Node.js-based server, we've set up middleware to handle different types of authentication: Basic, Bearer, and OAuth.

Basic Authentication: Users can sign in using their username and password. This happens at the /signin route, and the basicAuthentication middleware checks and validates the user's credentials.

Bearer Authentication: For routes that require a logged-in user, we use Bearer Authentication. Users provide a token in the Authorization header to access these routes. The tokenAuthentication middleware verifies the token's validity and allows or denies access.

**Describe the handshake necessary to implement OAuth.**

OAuth Handshake:

OAuth is used for users to log in using third-party providers like Google or GitHub. When a user wants to log in via OAuth, here's what happens:

1. The user initiates the process by clicking a "Login with Google" or "Login with GitHub" button on our site.
2. Our server, which has an OAuth route at /oauth, handles the handshake process with the third-party OAuth provider (e.g., Google or GitHub).
3. If the user grants permission, our server creates or updates a local user account and provides the user with a re-authentication token.
4. This token is used for further interactions on our site, and the user is automatically assigned the role of "user."

**Describe how Role Based Access Control works to a non-technical friend.**

Think of Role-Based Access Control (RBAC) like a game with different levels:

Admins: They are like the game masters. They can do everything, go anywhere, and control the game.

Editors: They are like the players with special powers. They can do many things, but not everything.

Writers: They are like the players with fewer powers. They can only do specific things.

Users: They are like the regular players. They can have fun but can't change the game.