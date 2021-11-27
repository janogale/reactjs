# State

state is the memory of the React Components

State consists of any data your application needs to know about, that can change over time. You want your apps to respond to state changes and present an updated UI when necessary.

React offers a nice solution for the state management of modern web applications.

## Adding a state variable using `useState` Hook

`useState` provides two things:

- A state variable to retain the data between renders.
- A state setter function to update the variable and trigger React to render the component again.

- Hooks are special functions that start with _use_. They let you use React features like state.

to use `useState` you need to import it from the React

`import { useState } from 'react';`

```jsx
function Counter() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}

<Count />;
```

When you call `useState`, you are telling React that you want this component to remember something:

- you can use `useState` multiple times in your component.

```jsx
function Counter() {
  const [count, setCount] = useState(0);
  const [message, setMessage] = useState("hey there");

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
      <p>{message}</p>
      <button onClick={() => setMessage("hello Coders")}>Click me</button>
    </div>
  );
}
```
