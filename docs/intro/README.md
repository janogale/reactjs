# Welcome To React JS Course

You will learn in this course, React JS Library. This course is for beginners.

## PREREQUISITES

There are a few things you should know in advance before you start learning React.

- knowledge of HTML & CSS.
- Basic knowledge of JavaScript and programming.
- Basic understanding of the DOM.
- Familiarity with ES6 syntax and features.

## Required Tools

- Code Editor: VS Code
- Node.js and npm installed globally.
- Browser: Chrome or Edge

## Module 1: React Fundemantals

- React Initial Setup
- React Elements
- JSX
- component
- Styling React
- Adding Images
- Props
- State
- Conditional Rendering
- Rendering Lists

# What is React?

- React is a JavaScript library for building user interfaces.
- It is maintained by Facebook and a community of individual developers and companies.

Official React site: https://reactjs.org/

## user interfaces

A user interface (**UI**) is anything we put in front of users to have them interact with a machine.

## Why should I learn React as JavaScript Developer?

- Working with the DOM API is hard.
- React is "just JavaScript"
- React can be developed with Andriod and iOS Apps
- React is most used UI Library in the world today
- React Developers are in demand in the world
- React is a very popular framework in the world

## What can you do with React?

- Build Web Apps - ReactJS
- Build Mobile Apps - React Native
- Build Desktop Apps - ElectronJS
- Build Virtual Reality Apps - React VR

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

1. run your app with Integrated Web Server in VS Code. `live server` will start a server on port 3000.

> The drawbacks to the above approach is that everything is compiled at runtime which is horribly slow but its great for learning React - but please don't put it like this in production.

## create-react-app

The **`create-react-app`** is an excellent tool which allows you to create and run React project very quickly. It does not take any configuration manually. This tool is wrapping all of the required dependencies like Webpack, Babel for React project itself and then you need to focus on writing React code only. This tool sets up the development environment, provides an excellent developer experience, and optimizes the app for production.

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
