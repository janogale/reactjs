# Conditional Rendering

You Application will often need to display different things depending on different conditions

In React, you can conditionally render JSX using JavaScript syntax like `if` statements, `&&`, and `? :` operators

lets render todo list conditionally

```jsx
const todos = [
  {
    text: "Learn HTML & CSS",
    completed: true,
  },
  {
    text: "Learn JavaScript",
    completed: true,
  },
  {
    text: "Learn React Native",
    completed: false,
  },
  {
    text: "Learn React",
    completed: true,
  },

  {
    text: "Learn React Native",
    completed: false,
  },
  {
    text: "Learn Node JS",
    completed: false,
  },
];
```

render the list and add tick mark if todo is completed using `if` statement

```jsx

function TodoItem(props) {
    const { todos } = props;

    if(todos.completed){
        return <li>{todos.text} ✔️</li>
    }

    return  return <li>{todos.text} ✖️ </li>
}

function TodoList(props) {
    const { todos } = props;

    return (
        <ul>
           <TodoItem />
        </ul>
    )
}
```

Render todos using ternary operator `? :`

```jsx
function TodoItem(props) {
  const { todos } = props;

  return (
    <li>
      {todos.completed ? (
        <span>{todos.text} ✔️</span>
      ) : (
        <span>{todos.text} ✖️</span>
      )}
    </li>
  );
}
```

Render only completed todos using `&&` logical AND operator

```jsx
function TodoItem(props) {
  const { todos } = props;

  return <li>{todos.completed && <span>{todos.text} ✔️</span>}</li>;
}
```

_Note_: `&&` is used to check if both conditions are true.

_Note_: if you return `null` or `false` from a Component, it will not render anything.
