# Code 401 - Reading Class - 02

1- Explain middleware, answer as though I were a non-technical recruiter:in web development, middleware functions sit between the incoming request and the response from the server. They can perform tasks like logging information, validating user authentication, modifying data, handling errors, or even adding extra functionality to the request or response. After each middleware does its job, it passes the request to the next middleware or the final destination, which could be a route handler responsible for generating the appropriate response.
2- Express the most popular __ __ __. Node.js web frameworks.
3-Express is “unopinionated.” What does that mean? it means that Express does not enforce strict rules or impose a specific way of doing things, it does not dictate a particular architecture or set of conventions for structuring your web applications.
4-What is a module and why is modularity useful to us as developers?
Module refers to a self-contained unit of code that encapsulates specific functionality. It is a way of organizing code into separate, independent units that can be easily managed and reused. Modules can contain variables, functions, classes, or even larger components of an application.

## What is NPM?
- What version of npm are you running on your machine? npm -v : 9.6.7

- What command would you type to install a library/package called ‘jshint’ into your node project?
“npm install jshint”

## What is TDD?
- Explain why tests are important. Please explain as though I were your non technical elder.
Tests are important because they help ensure that software works correctly and meets our expectations. Imagine if you were baking a cake. You would want to taste a small sample before serving it to others, right? Tests are like tasting the cake to make sure it's delicious and safe to eat.

- What are three expected benefits of testing
1. Improved Software Quality: Testing helps identify bugs, errors, and issues in the software. By running tests, we can catch these problems early and fix them before the software is released to users.
2. Enhanced Reliability and Stability: Through testing, we can verify that the software behaves as expected under different scenarios and inputs. This increases the reliability and stability of the software.
3. Cost and Time Savings: While it may seem counterintuitive, testing actually saves time and money in the long run. By detecting and fixing bugs early in the development process, we prevent them from reaching the production stage where they can be more costly and time-consuming to address.

- Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.
1. Partial adoption : It's important for the whole team to recognize the value of testing and make it a collaborative effort. Encouraging and fostering a testing culture within the team is crucial to ensure comprehensive and reliable test coverage.
2. Poor maintenance of the test suite: Over time, test suites can become large and complex, making it challenging to maintain and update them effectively.

## CI/CD
- What are three benefits of Continuous Integration?

1. Early Detection of Integration Issues: CI helps identify integration issues early by continuously merging and testing code changes in a shared environment. This proactive approach allows teams to detect and resolve conflicts, compatibility issues, or broken dependencies before they impact the stability of the software.
2. Faster Feedback Loop: CI provides rapid feedback on code changes. With each integration, automated tests are executed, and potential issues or regressions are identified promptly.
3. Code Quality: CI promotes collaboration among developers by integrating their code changes into a shared repository frequently.

- What is the difference between Continuos Delivery and Continuous Deployment?
Continuous Delivery is a software development approach where the application is always in a release-ready state, allowing it to be deployed at any time with a manual release decision. Continuous Deployment, on the other hand, automatically deploys new features or changes to the production environment as soon as they pass the necessary tests and criteria, without the need for manual interventio.

- Explain how GitHub fits into this process assuming the listener comes from a non-technical background.
gitHub acts as a central hub for version control, collaboration, and integration with CI/CD tools. It facilitates collaboration among team members.