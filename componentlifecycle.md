# Component Lifecycle / useEffect Hook

## useEffect hook

**What is the main intended use case for the useEffect hook?**
The main intended use case for the useEffect hook is to manage side effects in a React component. Side effects can include tasks such as data fetching, DOM manipulation, subscriptions, and more. 
**How does the effect’s logic interact with the component?**
useEffect hook interacts with the component through a defined sequence of steps.
Mounting Phase
Effect Execution
Updating Phase
Unmounting Phase

**What is the importance of the return value from the effect’s logic function?**
The function passed to useEffect can optionally return a cleanup function. This cleanup function runs when:
The component is unmounted (similar to componentWillUnmount in class components). Before re-running the effect due to a change in its dependencies. 