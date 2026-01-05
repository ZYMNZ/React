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
### Rendering Code
To _render_ a JSX expression means to make it _appear_ on screen.
```js
import React from 'react';
import { createRoot } from 'react-dom/client';

const container = document.getElementById('app');
const root = createRoot(container);
root.render(<h1>Hello world</h1>);
```
<hr>

```js
//old way
var React = require("react");
var ReactDOM = require("react-dom");
//new way
import React from "react";
import ReactDOM  from "react-dom";

ReactDOM.render(<h1>Hello meows</h1>, document.getElementById("root"));
```
> ReactDOM.render(WHAT TO SHOW, WHERE TO SHOW IT,we can a callback function to tell us when it's completed); <br>
> 'root' is main div where all the react code gets implemented <br>
> we are displaying a ```h1``` inside the #root div

<img width="50%" height="182" alt="image" src="https://github.com/user-attachments/assets/2260758b-154e-42ae-9f15-ae80b34b9c52" />
<br>
<br>

>Note: Inside the JS modul there is a Javascript compiler called "Babel". Babel is a toolchain that is mainly used to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript in current and older browsers or environments. <br>
<strong>Basucally saying: The same code can also work on older website versions! This works because it rewrites JSX as plain old javascript.</strong>

<hr>

### Syntax
```js
// using a variable 
const name = "Conan";
const fName = "conan"; 
const lName = "edugawa"; 
ReactDOM.render(<h1>Hello {name}</h1>, document.getElementById("root"));
ReactDOM.render(<h1>Hello {fName + " " + "lName"}</h1>, document.getElementById("root"));
ReactDOM.render(<h1>Hello {`${fName}` `${lName}`}</h1>, document.getElementById("root")); //string interpolation
```
#### CSS
> When using `style` attribute within the HTML in react, it is slighty different regarding the naming scheme. In react we use the Javascript attribute names!

<br>
For example: 
