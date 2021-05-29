# Accessibility Tree and `aria-hidden`

<blockquote cite="https://www.w3.org/TR/core-aam/#intro_treetypes">"The accessibility tree and the DOM tree are parallel structures. Roughly speaking the accessibility tree is a subset of the DOM tree."</blockquote>

[W3.org on Tree Types](https://www.w3.org/TR/core-aam/#intro_treetypes)

<br>

Any element that exposes something (an accessibility event or a property, relationship, or feature) becomes a part of the accessibility tree. Elements like `<div>` and `<span>` don't expose anything on their own, but the use of the `role` attribute can expose something to make that element part of the accessibility tree. Other elements naturally expose something, such as an `<input>`.

Both [The Accessibility Tree - Google](https://developers.google.com/web/fundamentals/accessibility/semantics-builtin/the-accessibility-tree) and [Accessibility Tree - MDN](https://developer.mozilla.org/en-US/docs/Glossary/Accessibility_tree) have good general overviews of the topic

<br>

What is part of the accessibility tree, though, can be hidden from assistive technologies like screen readers. Three ways you can hide text and prevent it from being announced by a screen reader will also visually hide the element. In HTML, the `hidden` attribute. In CSS, either `display: none` or `visibility: hidden`.

But what if you need to hide something to prevent a screen reader from announcing it, but keep it visually visible? That's where the `aria-hidden` attribute comes in.

When you add `aria-hidden="true"` to an element, it removes that element and all of its children from the accessibility tree. Keep in mind that adding `aria-hidden="false"` to an element will not re-expose that element to the accessibility tree if one of its parents has `aria-hidden="true"`.

According to [Using the aria-hidden attribute](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-hidden_attribute), `aria-hidden` can be useful for:

1. decorative content, such as images and icons
2. duplicated content, such as repeated text
3. offscreen content, such as menus

Using the `aria-hidden` attribute must be done with caution, however, and we must follow the [fourth rule of ARIA](https://www.w3.org/TR/using-aria/#fourth): **do not use `aria-hidden` on a focusable element.** If you do, then you risk a user tabbing to that element, but not hearing any announcement from the screen reader, which can be confusing at best.

<br>

The Previous Examples with ARIA section has some examples using `aria-hidden`, such as a button with an icon inside of it, with the icon having the `aria-hidden` attribute. This doesn't break the fourth rule of ARIA, because the button itself isn't hidden, so it will still be recognized by assistive technologies.

For offscreen content, think of any time you may have placed a menu or a modal off screen. It's off screen, it's fine! Until a user tries navigating with their keyboard and no matter how many times they press the `tab` key, nothing on the page is showing it has any focus. Or a screen reader is announcing the contents of a modal that should only appear after a specific action is taken by the user.

Using `aria-hidden="true"` as well as `tabindex="-1"`can fix those issues (as can the CSS properties `display: none` and `visibility: hidden`).
