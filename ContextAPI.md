# Context API

## Choosing the State Structure

**Summarize the five principles for structuring state.**
1. Grouping Related State: Combine state variables that are frequently updated together, into a single state variable to improve manageability.

2. Avoiding Contradictions: Organize state to prevent conflicting or contradictory information, reducing the chance of errors due to inconsistencies.

3. Minimizing Redundancy: Do not store data in state that can be computed from component props or existing state, to maintain a lean and efficient state structure.

4. Reducing Duplication: Prevent data duplication between different state variables or nested objects to avoid synchronization issues and maintain data integrity.

5. Avoiding Deep Nesting: Keep the state structure relatively flat and avoid excessive levels of nesting, as deep hierarchies can complicate state updates and management.

## Passing State Deeply with Context

**What problem do Contexts aim to solve?**

Contexts in React aim to solve the problem of having to pass data through multiple layers of components (prop drilling) by allowing a parent component to share information with any component deeper in the component tree, without needing to pass that information explicitly through every level of components using props.


**What is one technique to try before useContext?**

Passing probs.

**What hook complements useContext for complex applications?**

useReducer().

