# Screen Reader Outputs

The purpose of this repo is to help give some context to non-screen reader users about how screen readers may announce the contents of a web page. The examples provided include basic HTML tags (simple links, buttons, etc.), nested HTML tags (images used as links, icons inside of a button, etc.), and HTML with ARIA attributes.

Each tag or scenario will include at least two examples, usually one with less semantic tags being used and one with the semantic tags.

Each example will contain the actual HTML code (to see which tags and attributes are being used) and the results from the screen reader itself. Text within quotes will signify what the screen reader actually announces, while non-quoted text will simply be my own notes.

Some scenarios will include interactive elements, such as checkboxes, and show both the initial output (when the screen reader reaches that element) and any additional outputs (such as the element itself or anything else on the page changing/updating as a result of the interaction).

**All outputs are based on the NVDA screen reader with default settigns, using FireFox and/or Chrome**. Please keep this in mind, as other screen readers may announce things differently, and different settings or browsers may also affect what is announced. This repo is only meant to give non-screen reader users a general idea of how their HTML may be announced by a screen reader.

For more in depth information regarding web accessibility, please visit the [Web Accessibility Initiative](https://www.w3.org/WAI/). There you can find plenty of best practices, tutorials, tools to evaluate accessibility, and more.
