# Learning React
[cheatsheet](https://www.codecademy.com/learn/react-101/modules/react-101-jsx-u/cheatsheet)
# JSX
> Docs JavaScript XML (JSX) is a syntax extension of JavaScript that provides highly functional and reusable markup code. It is used to create DOM elements which are then rendered in the React DOM. JSX provides a neat visual representation of the UI.
```js
const h1 = <h1>Hello world</h1>;
```
### Attribute
```js
const p1 = <p id='large'>foo</p>;
const panda = <img src='images/panda.jpg' alt='panda' width='500px' height='500px'>;
```
### Nested JSX
A JSX expression that spans multiple lines must be wrapped in parentheses: `( )`
```js
const myDiv = (
  <div>
    <h1>Hello world</h1>
  </div>
);
```
#### JSX expression must have exactly _ONE_ outermost element
```js
const paragraphs = (
  <div id="i-am-the-outermost-element">
    <p>I am a paragraph.</p>
    <p>I, too, am a paragraph.</p>
  </div>
);
```

