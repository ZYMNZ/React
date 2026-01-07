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
>Variable: Camel casing

```js
// using a variable 
const name = "Conan";
const fName = "conan"; 
const lName = "edogawa"; 
ReactDOM.render(<h1>Hello {name}</h1>, document.getElementById("root"));
ReactDOM.render(<h1>Hello {fName + " " + "lName"}</h1>, document.getElementById("root"));
ReactDOM.render(<h1>Hello {`${fName}` `${lName}`}</h1>, document.getElementById("root")); //string interpolation
```
#### CSS
> When using attributes within HTML in react, it is slighty different regarding the naming scheme. In react we use the Javascript attribute names!
<br>
Regular HTML <br>
<img width="45%" height="45" alt="image" src="https://github.com/user-attachments/assets/7e00b54d-895d-4bc6-a042-22a3fcb49cc1" />  <br>
HTML attributes in React <br>
<img width="45%" height="86" alt="image" src="https://github.com/user-attachments/assets/a59da8ff-0374-4104-878e-9bca9e79d502" />

<br>

[HTML Global Attributes](https://www.w3schools.com/tags/ref_standardattributes.asp)

<img width="50%" height="42" alt="image" src="https://github.com/user-attachments/assets/ab344db6-3ce1-462d-bc64-5d0ffdc1eb2c" />

<br><br>

The closing of the `img` tag matters in React, without the website will crash. <br>
<img width="200" height="41" alt="image" src="https://github.com/user-attachments/assets/b89618d8-3ba9-477e-a08b-1cacad295a16" /> 

<br>
We can add parameters to an image: <br>
<img width="462" height="38" alt="image" src="https://github.com/user-attachments/assets/214290ce-95c7-40a1-b965-76aa4c3f5ae5" />

<br><br>

**Using the style property:**

Javascript Object: <br>
<img width="15%" height="15%" alt="image" src="https://github.com/user-attachments/assets/b496aa4f-0815-4909-a0fd-23e3ed494c50" />

> We will be using the JS object in the `style` attribute

[CSS Properties](https://www.w3schools.com/CSSref/index.php)
<br>
<img width="45%" height="320" alt="image" src="https://github.com/user-attachments/assets/52331b41-86e8-4660-a941-21fea7a845eb" />

One of the biggest advantages of using ***inline styling*** is that you can update it at anytime without touching the style property! <br>
<img width="408" height="62" alt="image" src="https://github.com/user-attachments/assets/bf44a726-b7e7-4f8c-bb27-1a6050bd9385" />

<hr>

### React Components
[Airbnb React/JSX Style Guide](https://github.com/airbnb/javascript/tree/master/react)

> Function's name: Pascal casing

```js
import React from "react";

function Heading() {
  return <h1>Fav Food</h1>;
}

// to just export the function name, without exe its return because we want to use it as a component
// we use `default` because when a file's primary purpose is to export a single main component
export default Heading;
```
We import the file that has the custom tag, and we use an orphan tag when using it: <br>
> Note: in the new version of react, we dont need to include the extension of the file

<img width="45%" height="158" alt="image" src="https://github.com/user-attachments/assets/c3420cb8-bcb7-477d-bfa3-88977e7f9538" />
<br>
<br>

Usually in the index.js file is just the `App` file getting rendered. The App file contains all the custome tags. <br>

<img width="40%" height="318" alt="image" src="https://github.com/user-attachments/assets/8a8c9b45-f70c-40d1-9ed1-3c010603d681" />

Inside the APP file: <br>

<img width="40%" height="564" alt="image" src="https://github.com/user-attachments/assets/e9e15d99-cb01-4ce1-9166-03ad8c7fe0bc" />

## Import/Export

When importing the `default` function name from another file, we can custoimize the name. <br>
<img width="334" height="157" alt="image" src="https://github.com/user-attachments/assets/08a328e9-d000-44b6-8624-2128b3b971eb" />






