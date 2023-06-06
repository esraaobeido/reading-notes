# Express REST API

### Review: ES6 Classes

1. Classes are a template for creating ____.
- Objects.
2. Can a class declaration be hoisted?
- No, class declarations cannot be hoisted in JavaScript.
3. How would you describe a constructor and contextual “this” to a non-technical friend?
- What is an Express Router?
A constructor is like a set of instructions for creating objects, and the "this" is a way for the constructor to refer to the object it's creating and work with its properties and methods.

### Using Express Routing

1. Within Express, what does routing refer to?
- Routing refers to how an application’s endpoints (URIs) respond to client requests.
2. What is the difference between a route path and a route method?
- A route path defines the URL or endpoint of a route, route method on the other hand, defines the HTTP method that is used to access a particular route such as (GET, POST, PUT, DELETE).
3. When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?
- It is appropriate to add next as a parameter to a route handler when you want to control the execution and pass the request to the next middleware or route handler
If next has been passed to your middleware as a parameter, it means that we should call next() to pass the control to the next middleware.

### Express Routing
1. What is an Express Router?
- Express Router provides a way to create modular, route handlers in your Express application, making it easier to organize and manage your routes.

2. By what mean do we initialize express.Router() in an express server?
- initializing const router = express.Router() first, then we can reuse it more than once.
3. What do we use route middleware for?
- The Express routing middleware is a function that performs a task before the request is sent, using for authentication, caching, logging information.

- What are your learning goals after reading and reviewing the class README?
learning about classes, express routing and middleware.



