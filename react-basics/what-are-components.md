---
icon: hashtag
---

# What are Components?

**Components** are the building blocks of **React** applications. They are reusable pieces of code that define how a UI element (or a group of UI elements) should behave and appear. Components allow you to break down your application into smaller, manageable parts, making it easier to develop, maintain, and reuse code.

**Types of Components in React**

There are two main types of components in React:

1. **Functional Components**
2. **Class Components**

**Creating a component**

Firstly, we'll see about the functional components.

![](https://i.imgur.com/yBHcmbl.png)

![](https://i.imgur.com/UWDZo1G.png)

Let's create another component.

![](https://i.imgur.com/MDrmDQs.png)

![](https://i.imgur.com/bVea4Zg.png)

#### Nested Components

![](https://i.imgur.com/ai7uPki.png)

> Always use a `div` or any other element (usually empty angular braces `<>`) to return multiple children.

![](https://i.imgur.com/lP1dp1T.png)

![](https://i.imgur.com/PHoxTgC.png)

***

#### Creating components in separate files

Let's try creating a component in a separate file and import it in the `main.jsx` file.

To do this, create a new folder named `components` in the `src` folder within which we'll be creating out component files. In this folder, create the file for your desired component. Let say, `Bike.jsx`.

![](https://i.imgur.com/vAnXCoY.png)

To use this component in the `main.jsx` file, we have to import it in the first place.

![](https://i.imgur.com/tyGcbEB.png)

***

### Exercise

Let's try to put all the components in individual files and augment them.

> \[!tip] Ensure that you give the file path correctly, otherwise you might encounter some errors.

![](https://i.imgur.com/secKOn8.png)

![](https://i.imgur.com/6TuU0Lk.png)

***

#### Class Components

Class components were the traditional way to create components in React before the introduction of **Hooks**. Class components offer more functionality, like lifecycle methods, but functional components with hooks have largely replaced them in modern React development.

![](https://i.imgur.com/mVw7zOF.png)

![](https://i.imgur.com/RJpvBPe.png)

![](https://i.imgur.com/wXfvtJY.png)

***
