# Router Links

Previously, we have seen about navigating between the webpages by manually entering their URLs. But this kind approach isn't very efficient, which is why we go for links.

Now, using Router links, the use can directly navigate to the other webpages by clicking on the links in the root webpage.

* In order to make this work, we have to use a tag called `<Link>` which is similar to `<a>` in HTML and the `to` parameter instead of `href`.
* To use `<Link` tag, we have to import it from the `react-roouter-dom` package.

```python
 import { Link } from 'react-router-dom'
```

![](https://i.imgur.com/mBs8o2t.png)

![](https://i.imgur.com/QPgMh0T.png)

Now, we can navigate the webpages through the links.

***

### Route Parameters

Sometimes, we might require some parameters to be shown in the URLs. This includes user Id's, Slugs or anything.

This can be done as follows.

For example,

If we have a component called `User`, we can display their id in the URL.

![](https://i.imgur.com/hiSsvwz.png)

![](https://i.imgur.com/xwzRAWQ.png)

* To display the ID in the URL, we have to use a hook function called `UseParams()`.

![](https://i.imgur.com/4KOGzg7.png)

![](https://i.imgur.com/aVk28bE.png)

![](https://i.imgur.com/y9KexBL.png)

***
