`Go Tailwind CSS official page -> Get started -> Frameworks Guide-> For Vite


## Props in React

- **Definition**: Props (short for "properties") are used to pass data from a parent component to a child component.
- **Read-Only**: Props are immutable, meaning they cannot be modified by the child component.
- **Usage**: They make components reusable by allowing different values to be passed to them.
- **Access**: Child components access props using `props.propertyName`.
- **Example**:
    
```jsx
function Parent() {
  return <Child name="Alice" />;
}

function Child(props) {
  return <p>{props.name}</p>;
}

```