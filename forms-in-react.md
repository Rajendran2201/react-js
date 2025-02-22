# Forms in React

Forms in React can be handled in two main ways:

1. **Controlled Components** (Recommended)
2. **Uncontrolled Components**

***

#### ✅ **1. Controlled Components** (Using `useState`)

Controlled components store form data in React state and update it on user input.

**📌 Example: Simple Contact Form**

```jsx
import { useState } from "react";

function ContactForm() {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
    message: ""
  });

  // Handle input change
  const handleChange = (e) => {
    setFormData({ ...formData, [e.target.name]: e.target.value });
  };

  // Handle form submission
  const handleSubmit = (e) => {
    e.preventDefault();
    console.log("Form Data:", formData);
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" name="name" value={formData.name} onChange={handleChange} required />
      </label>
      <br />
      
      <label>
        Email:
        <input type="email" name="email" value={formData.email} onChange={handleChange} required />
      </label>
      <br />
      
      <label>
        Message:
        <textarea name="message" value={formData.message} onChange={handleChange} required />
      </label>
      <br />

      <button type="submit">Submit</button>
    </form>
  );
}

export default ContactForm;
```

🛠 **Key Points:**

* Form data is stored in `useState`.
* `handleChange` updates state when the user types.
* `handleSubmit` prevents page refresh and logs form data.

***

#### ✅ **2. Uncontrolled Components** (Using `useRef`)

Uncontrolled components use **`useRef`** instead of React state.

**📌 Example: Uncontrolled Form**

```jsx
import { useRef } from "react";

function UncontrolledForm() {
  const nameRef = useRef();
  const emailRef = useRef();
  const messageRef = useRef();

  const handleSubmit = (e) => {
    e.preventDefault();
    console.log("Name:", nameRef.current.value);
    console.log("Email:", emailRef.current.value);
    console.log("Message:", messageRef.current.value);
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" ref={nameRef} required />
      </label>
      <br />

      <label>
        Email:
        <input type="email" ref={emailRef} required />
      </label>
      <br />

      <label>
        Message:
        <textarea ref={messageRef} required />
      </label>
      <br />

      <button type="submit">Submit</button>
    </form>
  );
}

export default UncontrolledForm;
```

🛠 **Key Points:**

* Uses `useRef()` to access input values directly.
* More performant but harder to manage for large forms.

***

#### ✅ **3. Handling Form Validation** (Basic Example)

To validate the form before submission:

```jsx
const handleSubmit = (e) => {
  e.preventDefault();
  
  if (!formData.name || !formData.email) {
    alert("Please fill in all required fields!");
    return;
  }

  console.log("Form Submitted:", formData);
};
```

***

#### ✅ **4. Handling Form Reset**

To reset the form after submission:

```jsx
const handleSubmit = (e) => {
  e.preventDefault();
  console.log("Form Data:", formData);
  
  // Reset form
  setFormData({ name: "", email: "", message: "" });
};
```

***

#### ✅ **5. React Hook Form (Best for Large Forms)**

For complex forms, use **react-hook-form** (lightweight & optimized).

📌 Install:

```bash
npm install react-hook-form
```

📌 Example:

```jsx
import { useForm } from "react-hook-form";

function HookForm() {
  const { register, handleSubmit, formState: { errors } } = useForm();

  const onSubmit = (data) => console.log(data);

  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <input {...register("name", { required: true })} placeholder="Name" />
      {errors.name && <p>Name is required</p>}
      
      <input {...register("email", { required: true })} placeholder="Email" />
      {errors.email && <p>Email is required</p>}
      
      <button type="submit">Submit</button>
    </form>
  );
}

export default HookForm;
```

***

#### 🚀 **Which Method to Choose?**

| Method                                 | When to Use                         |
| -------------------------------------- | ----------------------------------- |
| **Controlled Components (`useState`)** | Small forms, easy state management. |
| **Uncontrolled Components (`useRef`)** | Performance-critical, simple forms. |
| **React Hook Form**                    | Large forms, built-in validation.   |

***

## Let's work it out!

The forms can be create in react as follows.

![](https://i.imgur.com/3DhVMQa.png)

![](https://i.imgur.com/aX1624B.png)

![](https://i.imgur.com/WTDqgiZ.png)

***

#### Getting input value to the state

![](https://i.imgur.com/Tg4WofC.png)

![](https://i.imgur.com/4P59MCw.png)

***

#### Submitting forms

![](https://i.imgur.com/N6aRkRk.png)

![](https://i.imgur.com/LbgusjG.png)

***

#### Handling multiple inputs

![](https://i.imgur.com/y4VlqpG.png)

![](https://i.imgur.com/sMhDVje.png)

***

![](https://i.imgur.com/uXIDu8d.png)

![](https://i.imgur.com/EahfonH.png)

![](https://i.imgur.com/6YvmIpx.png)

![](https://i.imgur.com/oyhbjlz.png)

***

#### Simplifying onChange handler

![](https://i.imgur.com/HBq6jtb.png)

![](https://i.imgur.com/XBOJ0F4.png)

***

![](https://i.imgur.com/jRT96qE.png)

![](https://i.imgur.com/Nl1ofCg.png)

***

#### Setting Initial Values

![](https://i.imgur.com/9vYlwiU.png)

![](https://i.imgur.com/SurcfG2.png)

![](https://i.imgur.com/cB1R4eb.png)

![](https://i.imgur.com/7Exxgoh.png)

![](https://i.imgur.com/9tiBMGI.png)

![](https://i.imgur.com/A4O9S4h.png)

![](https://i.imgur.com/1dFd8WI.png)

***

#### TextArea

![](https://i.imgur.com/kaw5mgz.png)

![](https://i.imgur.com/dEFgKly.png)
