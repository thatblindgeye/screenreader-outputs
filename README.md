# Screen Reader Outputs

## Table of Contents
[Basic HTML Tags](https://github.com/thatblindgeye/screenreader-outputs/tree/main/basic%20html%20tags)
<br>
[HTML with ARIA](https://github.com/thatblindgeye/screenreader-outputs/tree/main/html%20with%20aria)
<br>
[Nested HTML Tags](https://github.com/thatblindgeye/screenreader-outputs/tree/main/nested%20html%20tags)

<br>

The purpose of this repo is to help give some context to non-screen reader users about how screen readers may announce the contents of a web page. The examples provided include basic HTML tags (simple links, buttons, etc.), nested HTML tags (images used as links, icons inside of a button, etc.), and HTML with ARIA attributes.

Each tag/scenario will usually include multiple examples, such as a tag with different attributes or comparing less semantic tags against the more appropriate, semantic tags.

Each example will contain the actual HTML code (to see which tags and attributes are being used) and the output from the screen reader itself. The output may state whether the output is for a specific browser only or based on a specific action. If there is no specific browser/action stated, assume that the output is for all browsers tested.

Some scenarios will include interactive elements, such as checkboxes, and show both the initial output (when the screen reader reaches that element) and any additional outputs (such as the element itself or anything else on the page changing/updating as a result of the interaction).

The announcement of some elements may differ depending on whether the screen reader is announcing all content on a page on initial load or if a user is tabbing or using a shortcut key to navigate to the next element on a page. Unless the difference is significant, only one output will be provided since the context would remain generally the same. For example, in my testing the screen reader may announce an `<a>` tag as "link Google", but manually navigating the page via keyboard may announce, "Google link",

**All outputs are based on the NVDA screen reader with default settings, using FireFox 88.0.1, Chrome 90.0.4430.212, and Microsoft Edge 90.0.818.66 on Windows 10**. Please keep this in mind, as other screen readers may announce things differently, and different settings or browsers may also affect what is announced. This repo is only meant to give non-screen reader users a general idea of how their HTML may be announced by a screen reader.

For more in depth information regarding web accessibility, please visit the [Web Accessibility Initiative](https://www.w3.org/WAI/). There you can find plenty of best practices, tutorials, tools to evaluate accessibility, and more.

## Quick notes

ARIA Landmarks are the `<aside>`, `<footer>`, `<form>`, `<header>`, `<main>`, `<nav>`, and `<section>` HTML elements. Landmarks can help screen reader users navigate through a web page using keyboard shortcuts based on the screen reader being used. The W3 page on [HTML5 Sectioning Elements](https://www.w3.org/TR/2017/NOTE-wai-aria-practices-1.1-20171214/examples/landmarks/HTML5.html) page has information regarding what default ARIA role each HTML element is, as well as buttons to toggle an outline around each landmark or heading on the page.

Screen readers may also have other keyboard shortcuts for navigating through a page. For example, with the NVDA screen reader, pressing the `k` key will navigate the user to the next link on the page (this is a reason why giving links meaningful names is important; navigating through a page's links and hearing "link click here" is not helpful to users of assistive technologies).
