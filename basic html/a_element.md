# `<a>`

It's important for links to have meaningful names. When a user navigates a page while using a screen reader, the context of a link may get lost depending on how they are navigating. Having `To read our terms of service, <a href"...">click here</a>` may make sense in the context of that sentence, but if a user is navigating between all of the links on a page, the screen reader may only announce "click here". Where are we going when we click there? [Creating valid and accessible links](https://www.a11yproject.com/posts/2019-02-15-creating-valid-and-accessible-links/) can be important to learn due to that loss of context.

<br>

**Note:** When opening a link that redirects to a different page on the same site (such as with SPA's), the screen reader may or may not announce the contents of the new page. This may be more an issue with web sites that utilize React and routers or a similar feature, or pages that simply have different tabs acting as "pages" with JavaScript building each tab dynamically.

A possible fix to this issue so that screen reader users will know that they are on a new "page" is with the use of the `aria-live` attribute (this gets dove into further in the ARIA Live Regions section of this repo). Checkout the "Communicating to the User" section in [Accessible Routing in React](https://timwright.org/blog/2019/03/23/accessible-routing-in-react/) to see one exampe of how this could be done.

<br><br>

## Simple Link

    <a href="https://www.theodinproject.com">The Odin Project</a>

    <a href="https://www.theodinproject.com" type="text/html">The Odin Project</a>

    <a href="https://www.theodinproject.com" rel="external">The Odin Project</a>

**Screen reader (visited link):** "The Odin Project visited link"

**Screen reader (unvisited link):** "The Odin Project link"

**Screen reader (Edge - `ctrl` + `Enter` to open in a new tab):** "Opening new tab."

<br><br>

## Link - Opens in a New Tab/Window

    <a href="https://www.theodinproject.com" target="_blank">The Odin Project</a>

**Screen reader (Firefox - `Enter` key to open):** "Busy."

**Screen reader (Chrome - `Enter` key to open):** "Untitled Google Chrome. Document busy blank"

**Screen reader (Edge - `Enter` key to open):** "Loading page. Loading complete."

<br>

**Example notes:** The screenreader did not announce any indication that a link would open in a new tab/window when navigating through the page. It could be important to indicate this by adding '(opens in a new window)' to the text content of the `<a>` element, or using ARIA attributes.

<br><br>

## Download Link

    <a href="//unsplash.it/500" download>Download Image</a>

    <a href="./test-image.jpg" download>Download Image</a>

**Screen reader:** "download image link"

<br>

**Example notes:** When clicking the link in the first example (an absolute URL), the image simply opened in the browser. When clicking the link in the second example (a relative URL), the dialog to save the image popped up and the screen reader immediately began to read the contents of the dialog box (the dialog may depend on your browser and browser settings).
