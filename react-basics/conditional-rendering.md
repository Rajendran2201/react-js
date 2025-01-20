---
icon: face-viewfinder
---

# Conditional Rendering

Conditional rendering in React allows you to decide what to display based on a certain condition. It's similar to using `if` statements in JavaScript but applied to render different JSX elements or components.

For example, If the `carInfo` attribute doesn't contain any value, the output would be not as we expected. We could see the missing values as `undefined`. This might cause an ambiguity to the client. In order to prevent this, we can use conditional rendering.

![](https://i.imgur.com/V3dWg9T.png)

![](https://i.imgur.com/g5ZokPs.png)

![](https://i.imgur.com/pxNz8Ek.png)

#### Using Conditional Rendering

> The Conditional Rendering can be implemented using the ternary operator.

If the `false block` is executed, we would see the output as follows.

![](https://i.imgur.com/4PD64zA.png)

![](https://i.imgur.com/gWZff9R.png)

If the `true block` is executed, we would see the output as follows.

![](https://i.imgur.com/vQV3KX6.png)

![](https://i.imgur.com/JSOVqS4.png)

***

#### Let's try another example

![](https://i.imgur.com/ekVZwJR.png)

![](https://i.imgur.com/iERG0Ui.png)

![](https://i.imgur.com/8TICWAZ.png)

![](https://i.imgur.com/2WyVdMw.png)

***

#### We also have another method.

This can also be implemented using the `&&` symbol. This can be used when there is no false block.

![](https://i.imgur.com/ZzWQbnG.png)

![](https://i.imgur.com/F8uGISA.png)

***
