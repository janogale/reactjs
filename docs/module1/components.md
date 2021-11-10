# Components: UI building blocks

- Components are one of the core concepts of React
- Components let you split the UI into independent, reusable pieces
- Conceptually, components are like JavaScript functions.
- React Component is JavaScript function that returns React elements

React Components Example:

```jsx
<PageLayout>
  <NavigationHeader>
    <SearchBar />
    <Link to="/docs">Docs</Link>
  </NavigationHeader>
  <Sidebar />
  <PageContent>
    <TableOfContents />
    <DocumentationText />
  </PageContent>
</PageLayout>
```

## Creating a React component

There are 2 ways to create a React component:

- **Class based**. A class based component is made up of a class that inherits from `React.Component`.

- **Function based**. Function based component consists of nothing but a JS function that needs to return JSX.

## What component type to choose

Which type of component do I choose, class based or function based?

- The reason for using a class based component is that you want to use state.
- since **React v16.8**, function components support state.
- function components are now recommended way to create components.

Let's show both types however, if you maintain an older code base, it might not make sense to mix styles and rather stick with the chosen approach.

### Creating components using functions

```jsx
function Button() {
  // Returns a DOM/React element here. For example:

  return <button type="submit">like</button>;
}

// To render a Button element in the browser

ReactDOM.render(<Button />, mountNode);
```

> The Component name has to start with a capital letter

### Creating components using classes

```jsx
class Button extends React.Component {
  render() {
    return <button type="submit">like</button>;
  }
}
```

## You can reuse components!

```jsx
<div>
  <Button />
  <Button />
  <Button />
</div>
```
