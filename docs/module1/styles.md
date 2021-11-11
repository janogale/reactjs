# Styling React Components

there are several ways to add style to your React components.

- inline styles
- stylesheets
- css modules
- css in js - e.g. styled components

## Inline Styles

in html, you can add inline styles to elements like this:

```jsx
<div style="margin-top: 20px; background-color: blue;"></div>
```

in react, you can add inline styles to elements like this:

```jsx
<div style={{ marginTop: 20, backgroundColor: "blue" }}></div>
```

> Note that in react the {{ and }} is actually a combination of a JSX expression and an object expression.

**Note:** you can also add inline styles to elements like this:

```jsx
const myStyles = { marginTop: 20, backgroundColor: "blue" };
<div style={myStyles} />;
```

**Note** all the CSS property names are camelCased in react like DOM properties.

> use `className` instead of `class` in react.

---

### Exercise

create custom Component that renders a button element, that accepts size and color props.
dynamically render the div with the props.

like this

```jsx
<Button size="small" color="red" />
<Button size="medium" color="green" />
<Button size="large" color="blue" />
```

## Stylesheets

- Regular CSS is a common approach, arguably one step better than inline CSS.
- The styles can be imported to any number of pages and elements unlike inline CSS, which is applied directly to the particular element.

you can create normal css file like this

```css
/* styles.css */

a:link {
  color: gray;
}
a:visited {
  color: green;
}
a:hover {
  color: rebeccapurple;
}
a:active {
  color: teal;
}
```

than import it like this in your component

```jsx
import styles from "./styles.css";
<a className={styles.link}>link</a>;
```

## CSS Modules

- CSS Modules allows the scoping of CSS Styles by automatically creating a unique classname
- they solve Style conflicts.

`create-react-app` supports css modules by default.

to enable css modules, your css file should end with `.module.css`

**Note:** CSS Modules are turned on for files ending with the `.module.css` extension.

```css
/*Button.module.css*/

.button {
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}

.color-red {
  background-color: #f44336; /* Red */
}
.bg-blue {
  background-color: #2196f3; /* Blue */
}
.bg-green {
  background-color: #4caf50; /* Green */
}
```

than import it like this in your component

```jsx
import styles from "./Button.module.css";
<button className={styles.button}>Click Me</button>;
```

## CSS in JS

CSS-in-JS is a technique which enables you to use JavaScript to style components. When this JavaScript is parsed, CSS is generated (usually as a <style> element) and attached into the DOM.

```

```
