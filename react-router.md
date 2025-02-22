# React Router

React Router is a popular library for handling navigation in React applications. It allows you to define routes, manage browser history, and create dynamic, single-page applications (SPAs) with client-side routing.

#### 📌 **Installation**

To use React Router, install it using npm or yarn:

```bash
npm install react-router-dom
# or
yarn add react-router-dom
```

***

#### 📌 **Basic Setup**

In a React app, you typically configure routes inside `App.js` or a similar file:

**1️⃣ Setting up Routes**

```jsx
import React from "react";
import { BrowserRouter as Router, Route, Routes } from "react-router-dom";
import Home from "./Home";
import About from "./About";
import Contact from "./Contact";

const App = () => {
  return (
    <Router>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </Router>
  );
};

export default App;
```

📌 **Key Points:**

* `<BrowserRouter>`: Wraps the entire app to enable routing.
* `<Routes>`: Acts as a container for all the `<Route>` components.
* `<Route>`: Defines a path and the corresponding component.

***

In react, whenever we try to redirect to a new URL from the root URL, the webpage undergoes a refresh. We have to prevent, which is where Router comes in.

![](https://i.imgur.com/VV0wPF6.png)

> React router is used to prevent refreshing the page incase of any changes in the URL.

* In `App.js`, I have included three components, let say three webpages.

![](https://i.imgur.com/w455YKA.png)

![](https://i.imgur.com/bIzAx0X.png)

* But, they all appear on the same webapge.

![](https://i.imgur.com/6VaGxGt.png)

* In my case, I don't want them all to appear in the same webpage. Instead, I want them to be displayed in different webpages.
* In order to achieve this, we need something called `BrowserRouter`.
* For using the `BrowserRouter`, we have to install the `react-router-dom`.
* Upon installing the `react-router-dom`, we can access the `BrowserRouter`.

Let's begin by installing the `react-router-dom`,

```bash
npm i react-router-dom
```

![](https://i.imgur.com/y9wKaD9.png)

As you install `react-router-dom`, you have to import the following,

1. BrowserRouter
2. Routes
3. Route

![](https://i.imgur.com/f30hlOC.png)

![](https://i.imgur.com/6d3ZEGF.png)

> \[!Warning] Incase of any errors, ensure that your versions of react components are same.

* Once this has been set up, We could see that each component is displayed in individual webpage.

![](https://i.imgur.com/dAkxFxb.png)

![](https://i.imgur.com/R8FlKPE.png)

![](https://i.imgur.com/e5lqPTS.png)

* Further, this navigation of webpages can be done through links which makes it much easier and convenient.
