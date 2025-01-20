# Introduction to React

React is a JavaScript-based UI development library. Although React is a library rather than a language, it is widely used in **web development**. The library first appeared in May 2013 and is now one of the most commonly used frontend libraries for web development.

> It eliminates the need of browser loading.

![](https://i.imgur.com/LApNZkQ.png)

* Even in ReactJS, this happens as same for the first time.

![](https://i.imgur.com/BX6kh4F.png)

* But for further retrievals of data, the browser is not involved.

![](https://i.imgur.com/ZOrTE0U.png)

***

### Using React in HTML

1. [**CDN Links**](https://legacy.reactjs.org/docs/cdn-links.html)

```html
<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
```

2. [**Babel CDN**](https://babeljs.io/docs/babel-standalone)

```html
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
```

**Create a HTML Page including these links**

![](https://i.imgur.com/8miGeMc.png)

Create a function named `helloWorld`.

![](https://i.imgur.com/XeMoWnd.png)

* Calling the function `helloWorld` and displaying the content in the browser.

![](https://i.imgur.com/AsdJrQN.png)

![](https://i.imgur.com/6hRlu5I.png)

> No output is displayed.

> \[!Reason] This is because,
>
> 1. The provided code contains a minor issue in how the `helloWorld` component is used. In React, functional components must start with an uppercase letter by convention when rendered as JSX.
> 2. The babel link is missing.

**Corrected Version of Code**

![](https://i.imgur.com/JsSpkq3.png)

![](https://i.imgur.com/uL6zSl0.png)

![](https://i.imgur.com/R0ZCD2E.png)

* The React helps us in augmenting the HTML code dynamically.

Though using React in HTML is possible, it becomes complicated when we build bigger projects. So, We have to create a React App for our codebase.
