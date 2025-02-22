# useEffect

The `useEffect` Hook in React is used to handle side effects in functional components. Side effects can include tasks like fetching data, subscribing to events, manually changing the DOM, or performing cleanup actions.

#### Basic Syntax:

```jsx
import React, { useEffect } from 'react';

useEffect(() => {
  // Side effect logic goes here

  return () => {
    // Cleanup logic (optional) goes here
  };
}, [dependencies]);
```

***

#### Key Concepts:

1. **Effect Callback:**
   * The first argument to `useEffect` is a function that contains the side-effect logic.
   * This function runs after the component renders.
2. **Dependencies Array:**
   * The second argument is an array of dependencies that determines when the effect runs.
   * It tells React to re-run the effect only if one or more dependencies change.
   * Examples:
     * `[]` (empty array): Runs only once after the initial render.
     * `[dependency1, dependency2]`: Runs whenever `dependency1` or `dependency2` changes.
     * Omitted: Runs after every render (not recommended for performance reasons).
3. **Cleanup Function (Optional):**
   * If your effect subscribes to something (e.g., an event listener or a timer), you can clean it up by returning a function inside the effect.
   * React calls this cleanup function before the effect runs again and when the component unmounts.

![](https://i.imgur.com/ptqj8Nr.png)

![](https://i.imgur.com/7YR22if.png)

![](https://i.imgur.com/h7VoSC3.png)

![](https://i.imgur.com/2pSrsvQ.png)

![](https://i.imgur.com/A7LaWLN.png)

But, in console the are no changes. This could be resolved as follows.

![](https://i.imgur.com/8i9gfrx.png)

![](https://i.imgur.com/BZ6izWn.png)

![](https://i.imgur.com/OHIrQ7J.png)

![](https://i.imgur.com/8aM2Ksl.png)

***
