# Accessibility Dev Tools

Whether you already know it or not, the dev tools in a browser can be incredibly helpful for various things. Whether you're trying to debug some JavaScript in the debugger, using the console to check or test Javascript, or tinkering with/checking out the HTML and CSS, dev tools are just downright handy.

They can even be great for inspecting accessibility, such as seeing the color contrast of text to its background, running an audit of a page with either aXe accessibility dev tools or Lighthouse, or getting an idea of what a screen reader might announce to a user (what we're interested in!).

In Firefox, there should be a dedicated "Accessibility" tab along the top of the dev tools (where the Inspector, Console. etc. tabs are located). If you don't see it, you may need to go into your dev tool settings and enable Accessibility under the "Default Developer Tools" section. If you right click a page, you should see an "Inspect Accessibility Properties" option, which will bring you to the Accessibility tab in the dev tools as well. [MDN's Accessibility Inspector](https://developer.mozilla.org/en-US/docs/Tools/Accessibility_inspector) page has a great general overview of this tab.

In Chrome and Edge, simply select the "Accessibility" tab on the right side of the Elements pane (where the Styles, Computed, etc. tabs are located). If you don't see the tab, you may need to enable experimental dev tools. Checkout [The Art of Labeling](https://youtu.be/8dCUzOiMRy4?t=106) at the 1:46 marker to see how to do so. [Chrome's Accessibility features reference](https://developer.chrome.com/docs/devtools/accessibility/reference/) page goes further into what you can do with their accessibility dev tools.

With Accessibility available in the dev tools, you can select an element you want to inspect from the HTML list in Chrome/Edge or the accessibility tree in Firefox (or using the element picker tool). Once you're inspecting the accessibility of an element, what we're interested in for the purposes of this repo are the Computed Properties (Chrome/Edge) or Properties (Firefox) section.

For Firefox's Properties section, the properties "name", "value", "description", and "relations" can be useful to look into. For some examples in this repo, what the screen reader announces may be the value of the "name", "value", or "description" properties, or sometimes more than one of them combined. The "relations" property has its own properties which may show where an element is getting its label from, whether it be from the `<label>` element or from an ARIA label (`aria-labelledby` or `aria-describedby`; an `aria-label` attribute would simply override the "name" property on an element). Don't worry about understanding ARIA attributes just yet, the HTML with ARIA section goes over these. For now just follow along.

**Note:** If the element providing a label for another element has a `display: none` CSS property, the "relations" section may not show the element providing the label. This doesn't necessarily mean the label has no affect within the screen reader, you just may not be able to track where an element is getting its label from through the dev tools.

For Chrome's/Edge's Computed Properties section, there should always be a "name" property, even if it's an empty string. The "name" property has its own properties, which show whether the element is being labelled by anything else (an `aria-label` or `aria-labelledby` attribute, a title attribute, or a `<label>` element, for example). Similar to Firefox Properties section, the `aria-label` attribute will override the "name" property. If an element has a description (usually from `aria-describedby` attribute or the `<desc>` element within an `<svg>` element), "description" and "Described by" properties will also appear here.

Now for a couple of examples.

![Screenshot from Chrome Accessibility dev tools](https://user-images.githubusercontent.com/70952936/119906667-a5685600-bf1c-11eb-93ec-8f43a6ac101c.png)

In the screenshot from Chrome dev tools above, we're using the following code:

    <a href="..."><img src="..." alt="Google"></a>
    // Notice there is no text contents for the <a> element

The screen reader announced this link as "Google, visited link" due to the `alt="Google"` attribute.

<br>

![Screenshot from Firefox Accessibility dev tools](https://user-images.githubusercontent.com/70952936/119907360-12c8b680-bf1e-11eb-9a18-7e843feddfd1.png)

In the screenshot from Firefox dev tools above, we're using the following code:

    <button type="button"></button>
    // Notice there is no text contents

The screen reader annoucned this button as "Confirm, button" due to it having an `arialabelledby` attribute that references another element whose text contents is "Confirm". Remember, if the element providing the "Confirm" label had `display: none` in CSS, the "relations" property would not show the "labelled by" property.

<br>

Keep in mind the Accessibility dev tools may not always show exactly what a screen reader announces. For example, in the screen shots above, the "name" property for the link is only "Google", but the screen reader announced "Google, visited link", which is the "name" property of the element and the type of element with the modifier "visited" to let the user know they've clicked the link before (if it were an unvisited link, it might simply be "link").

Similarly, a checkbox with a `<label>` of "Single" might be announced as, "Single, checkbox, not checked": the "name" property which is taken from the `<label>`, the type of element (a checkbox), and the state of the checkbox (not checked).

Not all elements are announced with their role or the type of element they are. `<p>Hello</p>` would only get announced as "Hello", not "Hello, paragraph".

Now that you have an understanding of how to access the accessibility dev tools, as you go through this repo it could be handy to copy and paste examples into your own HTML file in VS Code (or whichever code editor you prefer), open the HTML in a browser, and inspect the accessibility dev tools for the elements. If you do, you'll notice some examples have outputs that may not totally match what the dev tools show (the first example in the Image Links section is a good example for this).

The best way to test things is with an actual screen reader. [NVDA](https://www.nvaccess.org/download/) is available for Windows only, Narrator is also available for Windows, Chrome Vos is available on Chrome OS, and VoiceOver is available on macOS devices, and all of them are free. Whether you test any of those four out, or opt for a completely different one, it's important to know which OS's or browsers they're available for or work best with, know how reliable they might be, and to understand that each screen reader may (unfortunately) produce different results from one another.

If you can't download a screen reader or are unsure which to choose, despite it perhaps not being 100% accurate 100% of the time, using the accessibility dev tools can be a really good second choice for providing an idea of what might be announced by a screen reader.
