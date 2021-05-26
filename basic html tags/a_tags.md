# `<a>`

It's important for links to have meaningful names. When a user navigates a page while using a screen reader, the context of a link may get lost depending on how they are navigating. Having `To read our terms of service, <a href"...">click here</a>` may make sense in the context of that sentence, but if a user is navigating between all of the links on a page, all their screen reader will announce is the "click here" text. Not very helpful. Check out [Creating valid and accessible links](https://www.a11yproject.com/posts/2019-02-15-creating-valid-and-accessible-links/) for a better understanding.

When opening a link that redirects to a different page on the same site (such as with SPA's), the screen reader may or may not announce the contents of the new page. This may be more an issue with web sites that utilize React and routers or a similar feature, or pages that simply have different tabs acting as "pages" with vanilla JavaScript building each tab dynamically.

A possible fix to this issue so that screen reader users will know that they are on a new "page" is with the use of the `aria-live` attribute. Checkout the "Communicating to the User" section in the [Accessible Routing in React article](https://timwright.org/blog/2019/03/23/accessible-routing-in-react/) to see one exampe of how this could be done.

<br>

    <a href="https://www.theodinproject.com">The Odin Project</a>

    <a href="https://www.theodinproject.com" type="text/html">The Odin Project</a>

    <a href="https://www.theodinproject.com" rel="external">The Odin Project</a>

**Screen reader (visited link):** "The Odin Project visited link"

**Screen reader (unvisited link):** "The Odin Project link"

**Screen reader (Edge - opening in a new tab with `ctrl` + `Enter`):** "Opening new tab."

<br><br>

    <a href="https://www.theodinproject.com" target="_blank">The Odin Project</a>
    
**Screen reader (Firefox - opening link with `Enter` key):** "Busy."

**Screen reader (Chrome - opening link with `Enter` key):** "Untitled Google Chrome. Document busy blank"

**Screen reader (Edge - opening link with `Enter` key):** "Loading page. Loading complete."

**Example notes:** The screenreader did not announce any indication that a link would open in a new tab/window when navigating through the page. It could be important to indicate this by adding '(opens in a new window)' either inside the `<a>` tags, or using ARIA attributes.
    
<br><br>

    <a href="//unsplash.it/500" download>Download Image</a>
    
    <a href="./test-image.jpg" download>Download Image</a>

**Screen reader:** "download image link"

**Example note:** The first example (an absolute URL) opened the image in the browser. When clicking the second example (a relative URL), the dialog to save the image popped up and the screen reader immediately began to read the contents of the dialog box (the dialog may depend on your browser settings).

