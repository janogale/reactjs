# React Elements

- Elements are the smallest building blocks of React apps.
- An element describes what you want to see on the screen.
- It’s a virtual element describing a DOM element

```jsx
// using JSX
const element = <h1>Hello, Developers</h1>;
```

or

```js
// using plain JS
  const element = React.createElement(
    'h1',
    null,
    'Hello, Developers',
  ),
```

## Rendering an Element into the DOM

```jsx
const element = <h1>Hello, Developers</h1>;
ReactDOM.render(element, document.getElementById("root"));
```

The `ReactDOM.render` and `React.createElement` methods are the core API methods in a React application.

- `ReactDOM.render(whatToRender, WhereToRender)` This is basically the entry point for a React application into the browser’s DOM. I

- `React.createElement` creates a virtual DOM element. JavaScript Objects.

## Nesting React Elements

```js
ReactDOM.render(
  React.createElement(
    "div",

    null,

    "Hello React ",

    React.createElement("input"),

    React.createElement(
      "pre",

      null,

      new Date().toLocaleTimeString()
    )
  ),

  document.getElementById("root")
);
```

## Updating React Elements

- React Only Updates What’s Necessary
- React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.
