# Hook

## Thinking in React

**Summarize the five steps of thinking in react.**

- Step 1: Break the UI into a component hierarchy

Divide the UI mockup into distinct components and subcomponents.
Name each component and subcomponent based on their functionality.
Use techniques like the single responsibility principle to determine component boundaries.
Components should ideally match the data model structure.

- Step 2: Build a static version in React

Implement the app by creating a static version that renders the UI based on the data model.
Develop components that reuse other components and pass data using props.
Prioritize building the static version without interactivity first.
Avoid using state at this stage; components should only return JSX.

- Step 3: Find the minimal but complete representation of UI state

Identify the minimal set of changing data (state) needed to represent the interactive UI.
State should be DRY (Don't Repeat Yourself) and focus on the essentials.
Separate state from props and computations based on existing state or props.
State values are those that change over time and can't be computed from other values.

- Step 4: Identify where your state should live

Determine which components need to use the identified state.
Find the closest common parent component for the components using the state.
Decide where the state should reside based on common parent-child relationships.
State can be placed directly in the common parent or a component higher up the hierarchy.

- Step 5: Add inverse data flow

Allow user interactions to update the state by adding interactivity.
Implement data flow from child components to their parent components, updating state.
Pass functions from the parent component to child components for updating the state.
Use functions like useState to manage state and facilitate updates.


## State: A Component’s Memory

**What is one reason a local variable isn’t sufficient for managing a React component?**

Local variables are not sufficient for managing a React component's state because they do not trigger re-renders of the component when their values change.

**What is the argument to the useState hook, and what are the two parts of its return array?**

The argument to the useState hook is the initial value of the state. It defines the initial state value for the component.

The useState hook returns an array with two elements:

p The current state value (currentState): This is the current value of the state that you can read and use in your component.
- A function (setState): This function is used to update the state. When you call this function with a new value, React will re-render the component and update the state.

**How can Component A access state from Component B?**

If you have Component A and Component B, and you want them to share the same state, you can create a parent component (Component C) that holds the state and then pass the state and related functions down to both Component A and Component B as props.