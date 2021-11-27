# React - Responding to Events

Just like HTML DOM events, React can perform actions based on user events.

React has the same events as HTML: `click`, `change`, `mouseover` etc.

- React events are named using camelCase, rather than lowercase.
- With JSX you pass a function as the event handler, rather than a string.

## Adding event handlers

To add an event handler, you will first define a function and then pass it as a prop to the appropriate JSX tag.

```jsx
export default function Button() {
  function handleClick() {
    alert("You clicked me!");
  }

  return <button onClick={handleClick}>Click me</button>;
}
```

- Event Handlers are usually defined inside your components.
- _by convention_ Event handlers names starts with `handle`, followed by the name of the event. `handleClick`, `handleChange`, `handleMouseOver` etc.

### you can define an event handler inline in the JSX:

```jsx
<button onClick={function handleClick() {
  alert('You clicked me!');
}}>
```

Or, more concisely, using an arrow function:

```jsx
<button onClick={() => {
  alert('You clicked me!');
}}>
```

**Note**: Functions passed to event handlers must be passed, not called. For example:

- correct way:
  - `<button onClick={handleClick}>` ✔️
  - `<button onClick={() => alert('...')}>` ✔️ # inline
- Wrong way:
  - `<button onClick={handleClick()}>` ❌
  - `<button onClick={alert('...')}>`❌ # inline

## Passing event handlers as props

you can pass event handlers as props from a parent component to a child component.

```jsx
function Button({ onClick, children }) {
  return <button onClick={onClick}>{children}</button>;
}

function StartButton() {
  return <Button onClick={() => alert("Start!")}>Sart Game</Button>;
}

function StopButton() {
  return <Button onClick={() => alert("Stop!")}>Stop Game</Button>;
}
```

Note: By convention, event handler props should start with `on`, followed by a capital letter. For example: `onClick`, `onRemove`, `onDelete` etc.

