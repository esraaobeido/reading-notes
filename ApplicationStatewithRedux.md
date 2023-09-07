# Application State with Redux

## Dan Abramov Redux Tutorials

**What is the first principle of Redux?**

- The first principle of Redux, which is that, everything that changes in your application, including the data and the UI state, is contained in a single object, we call the state or the state tree

**what is a store and what do we use our reducers for within that store?**

- A store is an immutable object tree in Redux. A store is a state container which holds the application’s state. Redux can have only a single store in your application. Whenever a store is created in Redux, you need to specify the reducer.

- Reducers are pure functions in Redux that specify how the application's state changes in response to dispatched actions. They take the current state and an action as input and return a new state.


**Name three Redux store methods given to us by createStore and describe their use.**

1. GetState() 
2. Dispatch() 
3. Subscribe()


**Explain to a non-technical recruiter what combineReducers() does and why it is useful.**

combineReducers() is a tool in Redux that helps keep things tidy. Imagine it's like sorting your emails into different folders. It helps organize and manage different parts of your app's data so you can work on them separately, making your code cleaner and easier to understand.