# children prop - props.children

React provides special prop that is used to pass content between the start and ending tags.

in JSX, the content between start and ending tags is passed as a special prop: `props.children`.

html content

```html
<p>Children of p</p>

<div>
  <p>This is children content of div and p tags</p>
</div>
```

in JSX, the Avatar component is a child of Card

```jsx
function Card({ children }) {
  return <div>{children}</div>;
}

function Avatar({ photo }) {
  return <img src={photo} />;
}

<Card>
  <Avatar />
</Card>;
```
