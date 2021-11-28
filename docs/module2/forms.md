# Forms in React

Just like in HTML, React uses forms to allow users to interact with the web page.

adding forms to your React app is easy same as adding forms to your HTML.

```jsx
function MyForm() {
  return (
    <form>
      <input type="text" name="name" id="name" />
      <button>Submit</button>
    </form>
  );
}
```

The default behavior when submitting a form is form to post the result and move on to another page. But this is generally not what we want to happen in React.

We want to prevent this default behavior and let React control the form.

## Handling Form Submission

you can use the onSubmit attribute to handle the form submission.

In React, form data is usually handled by the components.

When the data is handled by the components, all the data is stored in the component state.

```jsx
function MyForm() {
  const handleSubmit = (event) => {
    event.preventDefault();
    console.log("Form submitted");
  };

  return (
    <form onSubmit={handleSubmit}>
      <input type="text" name="name" id="name" />
      <button>Submit</button>
    </form>
  );
}
```

## Handling Form inputs

you can use the onChange attribute to handle the form inputs.

```jsx
function MyForm() {
  const [value, setValue] = useState("");

  const handleChange = (event) => {
    setValue(event.target.value);
  };

  return (
    <form>
      <input
        type="text"
        name="name"
        id="name"
        value={value}
        onChange={handleChange}
      />
      <button>Submit</button>
    </form>
  );
}
```
