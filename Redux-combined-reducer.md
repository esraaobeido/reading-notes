# Redux - Combined Reducers
## Multiple Reducers Example

**Why create multiple reducers?**

To manage different parts of the application's state independently, Also to enhance modularity and maintainability

**How would you combine multiple reducers?**

- Use Redux's combineReducers function.
- Provide an object where keys represent state slices and values are individual reducers.

**How will you manage state as an immutable object? why?**

Use techniques like Immutable.js or the spread operator (...) to create new state objects.
Ensures predictability, pure reducers, and enables time-travel debugging.
Helps prevent bugs related to unintentional state mutations.

---

## Redux Docs: Using Combined Reducers

**combineReducers is a utility function to simplify the most common use case when writing ___ _____ .**

- Redux reducers

**Explain how combineReducers assembles the new state tree.**

-  In order to assemble the new state tree, combineReducers will call each slice reducer with its current slice of state and the current action, giving the slice reducer a chance to respond and update its slice of state if needed. So, in that sense, using combineReducers does "call all reducers", or at least all of the slice reducers it is wrapping.

**How would you define initial state in an app using combineReducers?**

There are two ways to define the initial shape and contents of your store's state.
1. Using preloadedState when creating the store: 
When you create your Redux store using the createStore function, you can pass an optional preloadedState as its second argument.

2. Returning initial state in the root reducer:
Another way to define the initial state is by having your root reducer return the initial state value when the state argument is undefined. When an action is dispatched for the first time, the state will be undefined, and the root reducer should provide the initial state. 

---

## Redux Docs: Combined Reducer Syntax

**Why will you want to split your reducing functions as your app becomes more complex?**

Splitting your reducing functions as your app becomes more complex is a best practice in Redux and state management in general. It helps maintain a clean, organized, and maintainable codebase, making it easier to scale your application and collaborate with other developers.


**The _____ helper function turns an object whose values are different reducing functions into a single reducing function you can pass to ____.**

-  The helper function that ``combines individual`` reducers into a single reducer function that can be used with createStore to create ``the Redux store``.

**What is a popular convention when naming reducers?**

- A popular convention is to name reducers after the state slices they manage, so you can use ES6 property shorthand notation: combineReducers({ counter, todos }). This is equivalent to writing combineReducers({ counter: counter, todos: todos }).