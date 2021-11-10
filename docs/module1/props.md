# Props

- components are like JavaScript functions. They accept single input/argument
- The argument is an object of called _`props`_ short for properties

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

## Passing Props to a Component

```jsx
<Welcome name="Ahmed" />
```

- React components use props to communicate with each other.
- Every parent component can pass some information to its child components by giving them props.
- Props might remind you of HTML attributes, but you can pass any JavaScript value through them, including `objects`, `arrays`, and `functions`.

### destructuring props

```jsx
function Welcome({ name }) {
  return <h1>Hello, {name}</h1>;
}
```

### Specifying a default value for a prop

```jsx
function Welcome({ name = "Guest" }) {
  return <h1>Hello, {name}</h1>;
}
```
