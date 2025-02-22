# State with Obbject

The previous method of declaring multiple state variables individually is quite hard. So, we can provide those data in the form of object.

For example,

![](https://i.imgur.com/nhRuK1b.png)

![](https://i.imgur.com/kmjEs3j.png)

![](https://i.imgur.com/YGaEJV7.png)

***

#### Updating Object in State

The data of the state variables are previously changed using their respective methods. But now, we don't have them. When we try to change a particular value, it is changed leaving the remaining values as empty.

![](https://i.imgur.com/IgqPzTm.png)

![](https://i.imgur.com/hj0yKAC.png)

> How do we solve this problem?

This can be solved by keeping a copy of the object. The copy of the object can be taken using the spread operator `...`

This is done in the following way.

![](https://i.imgur.com/YT1g19z.png)

![](https://i.imgur.com/MAY8fgO.png)

Now, the other values remain unchanged whereas only the `color` attribute has been changed.

***

### Updating Object in Class Component

We can also update the object in class component as follows.

![](https://i.imgur.com/GSAMk6S.png)

![](https://i.imgur.com/NpjyQqa.png)

![](https://i.imgur.com/3pduIDQ.png)

As we have done in the previous case, this can also be achieved using the callback function.

![](https://i.imgur.com/zeXkFEs.png)

![](https://i.imgur.com/gu3RxgT.png)

![](https://i.imgur.com/mbMU7Bc.png)

***

### Updating Arrays in State

In order to update the array in state, we can do as below.

Let's begin by creating a new component `List` which contains a group of items.

![](https://i.imgur.com/7mUErZs.png)

![](https://i.imgur.com/mS9c7To.png)

We encounter an error in the console which we have dealt with in the previous examples. So, we clearly know that this error occurs due to the missing `key` attribute.

![](https://i.imgur.com/GK0RYDa.png)

Let's add the `key` attribute to our list.

![](https://i.imgur.com/E1nH3a7.png)

As we include the `key` attribute, the error vanishes and we could see the console is clear now.

![](https://i.imgur.com/Brv9YeB.png)

> Now, let's learn to add items to the list in a dynamic way.

![](https://i.imgur.com/TALUa7b.png)

![](https://i.imgur.com/d2QIxqM.png)

By this, we can add items into the list dynamically as we click on the button.

![](https://i.imgur.com/ejhSeia.png)

![](https://i.imgur.com/Nfj6E84.png)

![](https://i.imgur.com/vBxyQfy.png)

![](https://i.imgur.com/UZfTj8R.png)

***
