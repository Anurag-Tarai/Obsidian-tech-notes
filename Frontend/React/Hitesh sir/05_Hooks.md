## Understating Why hooks ?

```jsx

function App() {

let a = 1; 

const addValue = () => {
a += 1;
console.log("adding vlaue", a);
};

return (
<>
<h1>Anurag Counter</h1>

<h2>Counter Value : {a}</h2>

<button onClick={addValue}>add</button>

<br />

<br />

<button>remove</button>
</>

);
}
```
Here onClick event the value of a is getting updated but value of a in UI remain same.

So, the updation of UI is controlled by `React` using `hooks`.

# Hook
In React, a **hook** is a special function that allows you to use React features, such as state and lifecycle methods, within functional components. Hooks enable you to manage component state, handle side effects, and reuse logic across components without the need for class-based components. Some common hooks include:

A `class-based component` in React is a type of component defined using JavaScript ES6 classes. Before the introduction of hooks in React 16.8, class components were the primary way to manage state, lifecycle methods, and other advanced features in React.

- `useState` for managing state.
- `useEffect` for performing side effects (e.g., fetching data or subscribing to events).
- `useContext` for accessing context.

Hooks follow certain rules, such as being called at the top level of a component and not inside loops, conditions, or nested functions.
## useState() 
---
The `useState()` hook is a fundamental React feature for managing state in functional components. It returns an array containing two elements:

1. **State value** (`value`): Holds the current state.
2. **Updater function** (`setValue`): Updates the state and triggers a re-render.

Example:
```jsx
const [value, setValue] = useState(0);
```
`setValue(newValue)` updates `value` and reflects the change in the UI.

