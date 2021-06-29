# Screen Reader Outputs

## Table of Contents

[Basic HTML](https://github.com/thatblindgeye/screenreader-outputs/tree/main/basic%20html)
<br>
[Nested HTML](https://github.com/thatblindgeye/screenreader-outputs/tree/main/nested%20html)
<br>
[HTML with ARIA](https://github.com/thatblindgeye/screenreader-outputs/tree/main/html%20with%20aria)

<br>

The purpose of this repo is to help give some context to non-screen reader users about how screen readers may announce the contents of a web page. The three main sections include basic HTML (simple links, buttons, etc.), nested HTML (images used as links, icons inside of a button, etc.), and HTML with ARIA attributes.

Each scenario will usually include multiple examples, such as an element with different attributes or comparing less semantic elements against the more appropriate semantic ones.

Each example will contain the actual HTML code (to see which elements and attributes are being used) and the output from the screen reader itself. The output may state whether the output is for a specific browser only or based on a specific action (loading the page, tabbing through the page, etc). If there is no specific browser/action stated, assume that the output is for all browsers tested and any action.

Some scenarios will include interactive elements, such as checkboxes, and show both the initial output (when the screen reader reaches that element from user navigation or on iniital page load) and any additional outputs (such as the element itself or anything else on the page changing/updating as a result of the interaction).

The announcement of some elements may differ depending on whether the screen reader is announcing all content on a page on initial page load or if a user is tabbing/using a shortcut key to navigate to the next element on a page. Unless the difference is significant, only one output will be provided since the context would remain generally the same. For example, in my testing the screen reader may announce `<a href="...">Google</a>` as "link Google" when the page loads, but manually navigating the page via keyboard may cause it to announce "Google link",

**All outputs are based on the NVDA screen reader with default settings, using FireFox >= 88.0.1, Chrome >= 90.0.4430.212, and Microsoft Edge >= 90.0.818.66 on Windows 10**. Please keep this in mind, as other screen readers may announce things differently, and different settings or browsers may also affect what is announced. This repo is only meant to give non-screen reader users a general idea of how their HTML may be announced by a screen reader.

For more in depth information regarding web accessibility in general, please visit the [Web Accessibility Initiative](https://www.w3.org/WAI/). There you can find plenty of best practices, tutorials, tools to evaluate accessibility, and more.

If you have suggestions for an example you think should be included in this repo, feel free to submit a pull request with a `.md` file that includes a code example. If you have run it through NVDA or another screen reader yourself, feel free to include any necessary information (the screen reader and/or browsers used, what the output was when the page loaded or when manually navigating the page, any notes for the example, etc.). Otherwise I can run it through NVDA and add the outputs.

<br>

## Quick notes

Screen readers may have other keyboard shortcuts for navigating through a page. For example, with the NVDA screen reader, pressing the `k` key will navigate the user to the next link on the page (this is a reason why giving links meaningful names is important; navigating through a page's links and hearing "click here, link" is not helpful to users of assistive technologies).

When the screen reader announces an element, it may also announce what the element's role or type is. For example, an `<a>` tag may be announced with "link" in addition to the text contents of the element, and a `<button>` tag may be announced similarly (except with "button" being announced).
