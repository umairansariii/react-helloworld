# react-helloworld
## Saying hello 👋 with react.js

In the core of React, there are three building-blocks to make it happens magically 🔮

- Parser (Babel.js) ✨
- Converter (React) ⚙️
- Renderer (ReactDOM) 📄

🔗 For a quick setup, you can use **React.js** using CDN

Read the documentation [here](https://reactjs.org/docs/cdn-links.html), also add **`crossorigin`** attribute in script tags.
```
https://unpkg.com/react@17/umd/react.production.min.js
https://unpkg.com/react-dom@17/umd/react-dom.production.min.js
```
🔗 You will also require to include **Babel.js** via CDN

Read the documentation [here](https://babeljs.io/docs/en/babel-standalone), also set the type attribute to **`text/babel`** or **`text/jsx`** since you are using JSX in React.js
```
https://unpkg.com/@babel/standalone/babel.min.js
```
## React.js under the hood 🤜🤛
The code below is somehow responsible for printing **Hello World 👋** on the screen.
```
ReactDOM.render(
    <h1 className="greeting">Hello World 👋</h1>,
    document.getElementById('root')
);
```
Whenever you 📺 render something, **ReactDOM** will call to **React.createElement()** to create a VirtualDOM before rendering to the RealDOM.
```
React.createElement(
    'h1',
    {className: 'greeting'},
    'Hello World 👋'
);
```
It creates an object like DOM Hierarchy ✨ are called React Elements.
```
{
  type: 'h1',
  props: {
    className: 'greeting',
    children: 'Hello World 👋'
  }
}
```
Which is then traditionally created using 💜 Web APIs and added to the DOM.
```
var element = document.createElement('h1');
    element.className = 'greeting';
    element.innerText = 'Hello World 👋';

document.getElementById('root').appendChild(element);
```
## Congratulations! 🥳🎉
You have printed the **Hello World** on the screen using React.js

🔗 But there's more you can read on https://reactjs.org/docs/introducing-jsx.html
