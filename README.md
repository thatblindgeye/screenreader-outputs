# Screen Reader Outputs

The purpose of this repo is to help give some context to non-screen reader users about how screen readers may announce the contents of a web page. The examples provided include basic HTML tags (simple links, buttons, etc.), nested HTML tags (images used as links, icons inside of a button, etc.), and HTML with ARIA attributes.

Each example will include the actual HTML code (to see which tags and attributes are being used), a screenshot of the rendered HTML (when a visual might be helpful), and what a screen reader may actually announce to the user. Some examples will include interactive elements, such as buttons, and list both the initial output (when the screen reader reaches that element) and any additional outputs (announcing any changes made to the page from the button click).

This repo does not take into consideration the different types of navigation a screen reader may provide, such as navigating between all links, buttons, tables, landmarks, etc. Semantic HTML tags should be used whenever possible, including tags such as main, aside, header, footer, etc., which aids landmark navigation.

All outputs are based on the NVDA screen reader only. Please keep this in mind, as other screen readers may announce things differently and different settings may affect what is announced, whether it be slightly or drastically. This repo is only meant to give non-screen reader users a general idea of how their HTML may be announced by a screen reader.

For more in depth information regarding web accessibility, please visit the [Web Accessibility Initiative](https://www.w3.org/WAI/). There you can find plenty of best practices, tutorials, tools to evaluate accessibility, and more.
