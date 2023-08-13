# Component Based UI

## React Quick Start
**What are the building blocks of a React app?**

Elements and components.

**What is the difference between an HTML element and a React component?**

An HTML element is a standard part of the Document Object Model (DOM) used in web development. It's a predefined tag like ``<div> or <p>``.

A React component is a reusable piece of UI code, often defined using JSX, which can include multiple HTML elements and logic. React components allow for better modularization and reusability than plain HTML elements.

**What is JSX and why do we use it?**

It is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

JSX produces React “elements”. We will explore rendering them to the DOM in the next section. Below, you can find the basics of JSX necessary to get you started.

Why JSX? React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

**Describe the process of embedding JavaScript expressions in JSX.**

You can embed JavaScript expressions within curly braces {} in JSX. For example: ``<p>Hello, {name}!</p>`` where name is a JavaScript variable.

**Does React or JSX have any special features for iteration or conditional logic?**

React provides mapping over arrays using methods like .map() to create dynamic lists of components.

**How does React know to respond to a user’s inputs?**

React responds to user inputs through event handling. You attach event handlers to JSX elements, such as onClick, onChange, etc., which then trigger updates to the component's state or cause other actions.

**What word indicates that a React component manages data with a Hook?**

The word that indicates a React component manages data with a Hook is typically "useState". For example: useState is a Hook used to manage state in functional components.

**How can two react components share data?**

By using **props** One component can pass data down to another component through it, which are essentially parameters passed during component rendering. The receiving component can then access and utilize the passed data for rendering or internal logic, creating a data flow between the parent and child components.

---
## Render and Commit

**What are the three steps of refreshing a React UI?**

The steps involve triggering a render, rendering the component, and committing changes to the DOM.

**How do you trigger updates to a component after the initial render?**

To trigger updates to a component after the initial render, you typically interact with the component's state using methods like setState (in class components) or state updater functions (when using hooks like useState).

**Does React recreate DOM nodes on every rerender?**
No, It updates components based on state changes.

**After React has updated the DOM, what still needs to happen before the user sees the change?**

After React has updated the DOM, there is still one important step before the user sees the change such as Layout and Painting : Once React updates the DOM, the browser's rendering engine performs a "layout" step where it calculates the positioning and dimensions of elements. 