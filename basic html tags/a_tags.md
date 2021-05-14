# `<a>`

    <a href="https://www.theodinproject.com">The Odin Project</a>

    <a href="https://www.theodinproject.com" target="_blank">The Odin Project</a>

    <a href="https://www.theodinproject.com" type="text/html">The Odin Project</a>

    <a href="https://www.theodinproject.com" rel="external">The Odin Project</a>

**Screen reader announces:** "The Odin Project visited link"

**Example note:** The screenreader did not announce any indication that a link would open in a new tab/window. It could be important to indicate this by adding '(opens in a new window)' either inside the `<a>` tags, or using ARIA attributes.

<br><br>

    <a href="//unsplash.it/500" download>Download Image</a>

**Screen reader announces:** "Download image link"

**Example note:** The screen reader did not announce what the image being downloaded is. Keep in mind that links should either explicitly state what they are linking to, or the context surrounding the link should state that.

<br>

**Note:** The "link" text that the screen reader announces simply lets the user know that the element is a link, and the same applies to the "visited" text (letting the user know whether the link is one they've visited before or not).
