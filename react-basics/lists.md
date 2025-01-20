---
icon: list-radio
---

# Lists

The Lists in React are used to display multiple similar items dynamically, typically from an array. React makes rendering lists simple by leveraging JavaScript array methods like `map()`.

**For Example,** Let's create a list named `carList` and we shall try to display the statement for all the cars in the list.

![](https://i.imgur.com/tLPonvx.png)

The `map()` function helps us to unmap the list and display the output as below.

![](https://i.imgur.com/ns1Xau1.png)

![](https://i.imgur.com/nPdaKa0.png)

Although we got our desired output, there is a problem. It caused some error in the console. In order to resolve these errors, we need to do something.

![](https://i.imgur.com/djyik2M.png)

We have to provide a key to the list. Here, We have given the `brand` of the cars as the key.

![](https://i.imgur.com/tnJ5GId.png)

Now the error is resolved and the console looks clear.

![](https://i.imgur.com/bTpL2q9.png)

**What is there's nothing unique to use as a key?**

In such cases, we can make use of the index of the elements in the list.

![](https://i.imgur.com/LXhrRuQ.png)

* Each child in a list must have a `key` that uniquely identifies it among its siblings. This allows React to optimize rendering by efficiently identifying what has changed.

**Why Not Use Array Index always?**

* While you can use the array index (`key={index}`), it is not recommended for dynamic lists where items might be added or removed. Using `index` can lead to rendering bugs since React relies on `key` for efficient updates.

***
