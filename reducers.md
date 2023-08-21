# Advanced State with Reducers

## Extracting State Logic into a Reducer

**What is the motivation for adding a reducer?**

The motivation for adding a reducer is to provide a more structured and controlled way to manage the state of a component or application.

**What are actions in the context of a reducer? How are they different than setting state directly?**

Move from setting state to dispatching actions, write a reducer function and use the reducer from your component.

**What common list operation is useReduce named for, and why?**

useReducer is named after the common list operation called "reduce" or "fold" in functional programming.

**When should you switch from useState to useReducer?**

When your state logic becomes more complex, involving multiple actions that result in different state changes. 