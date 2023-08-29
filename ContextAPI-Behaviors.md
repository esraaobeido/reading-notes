# Context API - Behaviors

## Scaling Up with Reducer and Context

**How do useReducer and useContext work together to simplify state management in a React application? (At least two paragraphs of prose.)**

- Step 1: Create the context. 
Create a context using the createContext function. This context will serve as the central hub where you can put your state and dispatch function.

```
const AppContext = createContext();
```

- Step 2: Put state and dispatch into context.

Wrap your component tree with a context provider. Inside the provider, use useReducer to manage your state and create a dispatch function. Then, provide both the state and dispatch through the context value.

- Step 3: Use context anywhere in the tree.
Now you can use the context you've created anywhere in your component tree. Components can access the state and dispatch function without the need for prop drilling.
