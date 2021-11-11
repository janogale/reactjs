# Adding Images to your Project

there is two ways to add images to your project.

## option 1: inside `src/` folder

- using static assets like images works similarly to CSS.
- the images should be under `src/` folder. so that they can be accessed by the webpack.

```jsx
import logo from "../logo.svg";

function App() {

    return (
      <div className="row">
        <div className="logo">
          <img src={logo} width="100" height="50" />
        </div>
      </div>
    );
  }
}

```

## option 2: inside `public/` folder

create folder `public/` and put your images there.

```jsx
function Home() {
  return (
    <div>
      <img src="images/logo.jpg" alt="logo" />
    </div>
  );
}
```

## option 3: using external images

adding external images is also possible. you can use any image from the internet by referencing its URL.

```jsx
function Home() {
  return (
    <div>
      <img src="https://example.com/images/logo.jpg" alt="logo" />
    </div>
  );
}
```
