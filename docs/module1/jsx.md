# JSX

- **What is JSX**. JSX is a syntax extension for JavaScript that lets you write HTML-like markup inside a JavaScript file.
- **Why use it**. You can opt out of using JSX but almost no one does, and it does make your life simpler.

## What & Why

- JSX is pretty much you writing HTML in JavaScript. It's a _pre processor_ step. You don't have to have it, but it makes life a whole lot easier.
- React recommends using JSX.

### Simple example

This is a simple example on one line of code:

```js
const Elem = <h1>Some title</h1>;

// and you can use it in React like so:
<div>
  <Elem />
</div>;
```

The above declaration of `Elem` looks like HTML in JavaScript. So what happens? When it is being processed, it is turned into the following ES5 code:

```js
React.createElement("Elem", null, "Some title");
```

Ok so calling `createElement`, here are the parameters:

- **First parameter, element name**.`Elem` becomes the element name.
- **Second parameter, attributes**. the second argument above is `null` and represents our element attributes, which we don't have any.
- **Third parameter, element value**. The third and last argument is the elements value.

#### With attribute example

Let's look at an example below where we give it an attribute:

````js
const Elem = <h1 title="a title" id='heading'>Some title</h1>;



The above would become the following code:

```js
React.createElement(
  "Elem",
  {
    title: "a title",
    id: 'heading'
  },
  "Some title"
);
````

now we have added attributes to the element, title and id.

```jsx
const element = <img src={user.avatarUrl}></img>;
```

### Multiline

Most of the time, you will define JSX over several different rows and starting out new, it might stump you why it doesn't work.

The solution is to wrap multiple elements in a parenthesis `()`, like so:

```jsx
const Elem = (
  <div>
    <h1>Some title</h1>
    <div>Some content</div>
  </div>
);
```

### One parent

JSX needs to have one parent. The following would be **incorrect**:

```html
<!-- would be incorrect, no parent element -->
const Elem = (
<h1>Some title</h1>
<div>Some content</div>
)
```

You can fix this by either:

- **Wrapping it in an element**. You can wrap your content in a div element like so:

  ```html
  const Elem = (
  <div>
    <h1>Some title</h1>
    <div>Some content</div>
  </div>
  )
  ```

- **Use `React.Fragment`**. You can wrap it in a `React.Fragment`, like so:

  ```html
  const Elem = (
  <React.Fragment>
    <h1>Some title</h1>
    <div>Some content</div>
  </React.Fragment>
  )
  ```

`React.Fragment` would be the parent element instead of us using a `div`.

## JSX Variables and Expressions

- We can add variables and expressions to our JSX using curly brackets `{}`.
- Anything inside of these brackets `{ }` is evaluated as JavaScript.

```jsx
function App() {
  const name = "Ali";
  const age = 30;

  return (
    <h1>
      My name is {name}, and I am {age} old
    </h1>
  );
}
```

## JSX vs HTML

- Use of **className** instead of **class** attribute
- all elements should be closed `<img src="#" />`, `<br/>`
- JSX is self closing like `<div id='root' />`
- Event listeners in JSX are written in camelCase `onClick`

## Summary

This is pretty much all we need to know on the topic of JSX to be able to work with it:

- It's like HTML that gets translated to `React.createElement()` calls.
- Multiline needs parenthesis to work.
- You need to have one parent element, `React.Fragment` is good option for that.
