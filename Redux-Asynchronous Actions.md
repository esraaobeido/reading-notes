# Redux - Asynchronous Actions

## Async actions

**1. Why use Redux middleware?**

Redux middleware is used to handle asynchronous logic and side effects in a Redux application. Since Redux reducers are meant to be pure functions without side effects, any asynchronous operations like making HTTP requests or interacting with external APIs cannot be placed directly inside reducers


**2. Consider the Redux Async Data Flow Diagram. Describe the flow in your own words.**

The Redux Async Data Flow involves actions being dispatched, intercepted by middleware for asynchronous logic, processed by reducers to update the state, and finally reflected in the UI components connected to the Redux store.

**3. How are we accommodating async in our Redux app?**

Redux middleware allows us to separate asynchronous logic from reducers, keeping the Redux data flow clean and predictable while enabling us to handle complex asynchronous operations in our Redux application.

--- 

## Thunk middleware?

**1. Why would you need redux-thunk middleware?**

With a plain basic Redux store, you can only do simple synchronous updates by dispatching an action. Middleware extends the store's abilities, and lets you write async logic that interacts with the store.

Thunks are the recommended middleware for basic Redux side effects logic, including complex synchronous logic that needs access to the store, and simple async logic like AJAX requests.

**2. Redux Thunk middleware allows you to write action creators that return a ____ instead of an action.**

```function ```

**3. Describe how any return value from the inner thunk function will be made available.**

Any return value from the inner function will be available as the return value of dispatch itself. This is convenient for orchestrating an asynchronous control flow with thunk action creators dispatching each other and returning Promises to wait for each other’s completion.