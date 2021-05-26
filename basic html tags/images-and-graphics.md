# Images and Graphics

This section covers different types of image and graphic elements, including the `<canvas>`, `<image>`, `<picture>`, and `<svg>` tags.

<br>

## `<canvas>`

    <canvas width="300" height="300">
        An alternative text describing what your canvas displays.
    </canvas>
    
**Screen reader (on page load):** "An alternative text describing what your canvas displays."

<br>

    <canvas width="300" height="300" tabindex="0">
        An alternative text describing what your canvas displays.
    </canvas>

**Screen reader (using the `tab` key to navigate the page and give the canvas focus):** "An alternative text describing what your canvas displays."

**Notes:** Per MDN, there are [accessibility concerns with the `<canvas>` tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas#accessibility_concerns).

<hr>

## `<img>`

    <img src="//unsplash.it/500" alt="A random image from Unsplash">

**Screen reader:** "A random image from Unsplash, graphic."

<br>

    <img src="//unsplash.it/500" alt="">

**Example Notes:** The screen reader did not announce the presence of the image.

<br>

    <img src="//unsplash.it/500">
    
**Screen reader (Chrome):** "To get missing image descriptions open the context menu, unlabeled graphic."

<br>

    <img src="//unsplash.it/500" alt="" tabindex="0">

**Screen reader (using the `tab` key to navigate the page and give the image focus):** "Blank."

<br>

    <img src="//unsplash.it/500" tabindex="0">

**Screen reader (Firefox and Edge):** "500, graphic."

**Screen reader (Chrome):** "500, unlabeled graphic."

<br>

**Notes:** When using images as decoration, the `alt` attribute should be used with an empty string rather than omitted. If simply omitted, some screen readers or browsers may announce the image in some way when it shouldn't/doesn't need to (see [Decorative Images](https://www.w3.org/WAI/tutorials/images/decorative/) for more information).

<hr>

## `<picture>`

    <picture>
        <source media="(min-width:650px)" srcset="//unsplash.it/800">
        <source media="(min-width:465px)" srcset="//unsplash.it/500">
        <img src="//unsplash.it/200" alt="unsplash sample">
    </picture>
    
**Screen reader:** "Graphic, unsplash sample."

**Notes:** Each image was announced with the same output regardless of which image was being used.

The outputs from the `<img>` section above should remain the same when used inside a `<picture>` element, e.g. leaving the `alt` attribute as an empty string should cause the screen reader to ignore the presence of the image.

<hr>

## `<svg>`

    <svg width="100" height="100">
        <circle cx="50" cy="50" r="40" fill="red" />
    </svg>

**Example Notes:** The screen reader did not announce the presence of the `<svg>` element.

<br>

    <svg width="100" height="100" tabindex="-1">
        <circle cx="50" cy="50" r="40" fill="red" />
    </svg>

**Screen reader (Chrome and Edge - on page load or using the shortcut key for graphics):** "Graphic."

<br>

    <svg width="100" height="100" tabindex="-1">
        I'm a circle
        <circle cx="50" cy="50" r="40" fill="red" />
    </svg>

**Screen reader (Chrome and Edge - on page load or using the shortcut key for graphics):** "Graphic."

<br>

    <svg width="100" height="100" tabindex="-1">
        <title>I'm a circle.</title>
        <desc>A red circle.</desc>
        <circle cx="50" cy="50" r="40" fill="red" />
    </svg>

**Screen reader (Firefox - on mouse hover):** "I'm a circle. A red circle."

**Screen reader (Chrome and Edge - on page load):** "Graphic, I'm a circle."

**Screen reader (Chrome and Edge - using the shortcut key for graphics):** "I'm a circle, graphic."

**Notes:** If an `<svg>` is only decorative,it may be best to follow the rules for `<img>` tags (see [Decorative Images](https://www.w3.org/WAI/tutorials/images/decorative/) for more information).

The screen reader did not seem to recognize an `<svg>` element in Firefox except when hovering over it with the mouse. A possible fix is with ARIA attributes.

The text content of the `<title>` and `<desc>` tags were not rendered on the page, but the text contents of the `<title>` tag did appear as a tool tip when hovering over the `<svg>`.
