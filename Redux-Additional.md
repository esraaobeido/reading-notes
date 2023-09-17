# Redux - Additional Topics

## Redux Toolkit (RTK)

**1. What concerns are addressed by Redux Toolkit?**

The Redux Toolkit package is intended to be the standard way to write Redux logic. It was originally created to help address three common concerns about Redux:

"Configuring a Redux store is too complicated"
"I have to add a lot of packages to get Redux to do anything useful"
"Redux requires too much boilerplate code"

**2. What does configureStore() do?**

``configureStore()`` wraps createStore to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.


**3. How would I use createSlice()?**

``createSlice()``: accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.


## MobX

**1. What is Mobx?**

MobX is a simple, scalable and battle tested state management solution. This tutorial will teach you all the important concepts of MobX in ten minutes. MobX is a standalone library, but most people are using it with React and this tutorial focuses on that combination.

**2. How does MobX make it “impossible” to produce an inconsistent state?**

MobX makes state management simple again by addressing the root issue: it makes it impossible to produce an inconsistent state. The strategy to achieve that is simple: Make sure that everything that can be derived from the application state, will be derived. Automatically.


**3. How would we build a reactive user interface?**

By applying the observer HoC and organizing your code around MobX observables, you've effectively created a reactive user interface where components automatically update in response to changes in the underlying state. This approach minimizes the need for manual state management and allows you to focus on the declarative structure of your UI components.