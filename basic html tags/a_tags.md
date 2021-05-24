# `<a>`

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

The screen reader did not announce what the image being downloaded is. Keep in mind that links should usually explicitly state what they are linking to in some way, either via ARIA attributes or the actual link description. Check out [this article on accessible links from the A11y Project](https://www.a11yproject.com/posts/2019-02-15-creating-valid-and-accessible-links/) for a better understanding.

<hr>

**Note:** The "link" and "visited link" text that the screen reader announces simply lets the user know that the element is a link. Other elements may have a similar announcement (such as a button being announced with "button").

When opening a link that redirects to a different page on the same site, the screen reader may or may not announce the contents of the new page. Based on my limited testing, this may have to do with whether the site was created using React routers or a similar feature. Keep in mind this is only an assumption based on the few sites that look to be using React and may be using routers/a similar feature.
