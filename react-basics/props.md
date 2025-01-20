---
icon: plug-circle-check
---

# Props

**Props** are used to pass data from parent to child components. They are read-only and cannot be modified by the child component.

> \[!tip] Use back ticks \`\` incase of string interpolation.

![](https://i.imgur.com/8T0NMKz.png)

![](https://i.imgur.com/kmnCXph.png)

This is very useful in certain cases. Assume that the code `const brand = 'Ford';` has been moved from `Car.jsx` to `Garage.jsx`. In such a case, we can use props.

![](https://i.imgur.com/xcaId7k.png)

![](https://i.imgur.com/Nn2bAUZ.png)

![](https://i.imgur.com/UhuefPy.png)

***

#### Exercise: Try with another prop

Let's try this using a color prop for the car component.

![](https://i.imgur.com/NSVbCVj.png)

![](https://i.imgur.com/YESwuZr.png)

![](https://i.imgur.com/V4xenTK.png)

***

**Think about this!**

Giving these props individually as variables is a tedious process. Consider making it simple and compact.

Of course, we can do it using JavaScript objects.

![](https://i.imgur.com/kyjh1y4.png)

![](https://i.imgur.com/9ivFQQw.png)

![](https://i.imgur.com/GkHn8Kh.png)

> btw, `const { carInfo } = props;` This is called as destructuring.

***
