# Welcome To React JS Course

You will learn in this course, React JS Library. This course is for beginners.

## PREREQUISITES

There are a few things you should know in advance before you start learning React.

- knowledge of HTML & CSS.
- Basic knowledge of JavaScript and programming.
- Basic understanding of the DOM.
- Familiarity with ES6 syntax and features.
- Node.js and npm installed globally.

## Setting up new React JS project

There are mostly 2 ways to set up a new React project:

- **Script tags**, it is possible to just use script tags and point to React, React DOM and Babel.
- **CRA, Create React App**, this tool helps us generate a React project. This is probably the most common set up.

## Script tags

This version is simplest to start with if you are a beginner. It enables you to dive straight into React and learn its features.

### Create a React project with script tags and CDN

1. Create a file _app.js_ and give it the following content:

   ```js
   // app.js

   class Application extends React.Component {
     render() {
       return <div>App</div>;
     }
   }

   ReactDOM.render(<Application />, document.getElementById("app"));
   ```

1. Next, create a file _index.html_ and give it this content:

   ```html
   <!-- index.html -->

   <html>
     <body>
       <!-- This is where our app will live -->
       <div id="app"></div>

       <!-- These are script tags we need for React, JSX and ES2015 features -->
       <script src="https://fb.me/react-15.0.0.js"></script>
       <script src="https://fb.me/react-dom-15.0.0.js"></script>
       <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.34/browser.min.js"></script>
       <script type="text/babel" src="app.js"></script>
     </body>
   </html>
   ```

   You should now have an app with the following files:

   ```output
   -| app.js
   -| index.html
   ```

1. Run `npx http-server -5000` in the terminal:

   ```bash
   npx http-server -p 5000
   ```

   This will serve up your application on `http://localhost:5000`.

1. Navigate to `http://localhost:5000` in your browser, you should see the text **App**.

> The drawbacks to the above approach is that everything is compiled at runtime which is horribly slow but its great for learning React - but please don't put it like this in production.

## create-react-app

Create React App, CRA is a scaffolder developed by Dan Abramov. With it you are able to scaffold a React application with ease and will get you up and running in no time.

### 📌 Create a React project using npx and Create React App

To scaffold a project using `npx` and Create React App it's just a one liner command.

1. Create a new React project running this command in a terminal:

   ```bash
   npx create-react-app my-app
   ```

   > Currently you need Node >= 8.10 and NPM >= 5.6 on your machine.

1. Navigate to your project

   ```bash
   cd my-app
   ```

1. Run the following command to serve it up:

   ```bash
   yarn start
   ```

   or

   ```bash
   npm run start
   ```

   This starts a development server at `http://localhost:3000`.

1. In your browser, navigate to `http://localhost:3000`. You should see the following:

`Create React App` is an officially supported way to create single-page React applications. It offers a modern build setup with no configuration [https://github.com/facebook/create-react-app](https://github.com/facebook/create-react-app)

---

let's start coding. 🚀
