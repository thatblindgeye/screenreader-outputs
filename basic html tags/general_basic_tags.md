# General Basic Tags

<br><br>

## `<b>`, `<em>`, `<i>`, `mark`, `<strong>`, and `<u>`

    <p>This is a sentence with <b>emphasized</b> text.</p>


    <p>This is a sentence with <strong>emphasized</strong> text.</p>


    <p>This is a sentence with <em>emphasized</em> text.</p>


    <p>This is a sentence with <u>emphasized</u> text.</p>


    <p>This is a sentence with <i>emphasized</i> text.</p>
    
**Screen reader:** "This is a sentence with emphasized text."

**Example Notes:** There was no discernible emphasis in any of the above examples, but the appropriate tag should still be used when applicable (see [`<b>`: The Bring Attention To element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b), [`<strong>`: The Strong Importance element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong), [`<em>`: The Emphasis element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em), [`<u>`: The Unarticulated Annotation (Underline) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/u), and [`<i>`: The Idiomatic Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i) for more information).

<br>

    <p>This is a sentence with <mark>highlighted</mark> text.</p>

**Screen reader:** "This is a sentence with marked-content highlighted out of marked-content text."

<hr>

## `<address>`

    <address>
      John Smith</br>
      123 Fake St</br>
      Fakesville, OH 12345
    </address>

    <p>
      John Smith</br>
      123 Fake St</br>
      Fakesville, OH 12345
    </p>

**Screen reader:** "John Smith, one two three Fake Street, Fakesville Ohio, one two three four five."

**Example Note:** The screen reader did not give any indication that the first example was using an `<address>` tag nor was there any discernible difference between either example, but the `<address>` tag should still be used when applicable (see [`<address>`: The Contact Address element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address) for more information).

<hr>

## `<blockquote>`

    <blockquote cite="https://www.w3.org/Help/#activity">
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </blockquote>

**Screen reader:** "blockquote W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission out of blockquote".

<br>

    <p>
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </p>

**Screen reader:** "W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission".

<hr>

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

## `<cite>`

    <p><cite>The Starry Night</cite> by Vincent van Gogh</p>

    <p>The Starry Night by Vincent van Gogh</p>

**Screen reader:** "The Starry Night by Vincent Van Gogh"

**Example Notes:** The screen reader did not give any indication that the first example was using a `<cite>` tag nor was there any discernible difference between either example, but the `<cite>` tag should still be used when applicable (see [`<cite>`: The Citation element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite) for more information).

<hr>

## `<code>`

    <p>The <code>code</code> HTML tag should be used to define text as computer code.</p>

    <p>The code HTML tag should be used to define text as computer code.</p>

**Screen reader:** "The code HTML tag should be used to define text as computer code."

**Examples Notes:** The screen reader did not give any indication that the first example was using a `<code>` tag nor was there any discernible difference between either example, but the `<code>` tag should still be used when applicable (see [`<code>`: The Inline Code element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code) for more information).

<hr>

## `<data>`

    <data value="12345">HP Laptop</data>

    <p>HP Laptop</p>

**Screen reader:** "HP laptop."

**Example Notes:** The screen reader did not give any indication that the first example was using a `<data>` tag nor was there any discernible difference between either example, but the `<data>` tag should still be used when applicable (see [MDN's page on the `<data>` tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/data) for more information).

<hr>

## `<del>` and `<ins>`

    <p>My favorite color is <del>red</del> <ins>purple.</ins></p>

**Screen reader:** "My favorite color is deleted red inserted purple."

<hr>

## `<dialog>`

    <dialog open>Thank you for checking out this repo!</dialog>

**Screen reader:** "Dialog."

**Example Notes:** The screen reader did not announce the text content of the dialog tag itself. 

<br>

    <dialog open tabindex='0'>Thank you for checking out this repo!</dialog>

**Screen reader (using the `tab` key to navigate the page and give the dialog focus):** "Dialog thank you for checking out this repo."

**Example Notes:** Check the browser/screen reader support at [`<dialog>`: The Dialog element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog) before using this tag.

<hr>

## `<h1>` to `<h6>`

    <h1>An H1 tag</h1>

**Screen reader:** "An h one tag heading level one."

**Example Notes:** The screen reader announced the other remaining 5 heading tags similarly ("an h two tag heading level two", etc.).

<hr>

## `<iframe>`

    <iframe src="https://www.w3.org/WAI/"></iframe>

**Screen reader:** "Frame..."

**Example Notes:** After the initial output above, the screen reader began to announce the content inside the iframe.

<br>

    <iframe src="https://www.w3.org/WAI/" title="Web Accessibility Initiative"></iframe>

**Screen reader:** "Web Accessibility Initiative frame..."

**Example Notes:** The title attribute should be included to give screen readers context of the embedded content.

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

## `<kbd>`

    <p>My keyboard is broken, so I have to copy and paste the <kbd>t</kbd> key.</p>

    <p>My keyboard is broken, so I have to copy and paste the t key.</p>

**Screen reader:** "My keyboard is broken, so I have to copy and paste the t key"

**Example Notes:** The screen reader did not give any indication that the first example was using a `<kbd>` tag nor was there any discernible difference between either example, but the `<kbd>` tag should still be used when applicable (see [`<kbd>`: The Keyboard Input element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd) for more information).

<hr>

## `<pre>`

    <pre>
      An example of     what
      preformatted  text can
      look             like.
    </pre>

    <p>
      An example of     what
      preformatted  text can
      look             like.
    </p>

**Screen reader:** "An example of what preformatted text can look like."

**Example Notes:** The screen reader did not give any indication that the first example was using a `<pre>` tag nor was there any discernible difference between either example, but the `<pre>` tag should still be used when applicable (see [`<pre>`: The Preformatted Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre) for more information).

When using the `<pre>` tag to create an image with text characters, for example, you should provide an alternative caption for screen readers. See the link for the `pre` tag above for an example.

<hr>

## `<q>`

    <p><q>This is a quoted section of text,</q> said the paragraph tag.</p>

    <p>"This is a quoted section of text," said the paragraph tag.</p>

**Screen reader:** "This is a quoted section of text said the paragraph tag."

**Example Notes:** The screen reader did not give any indication that the first example was using a `<q>` tag nor was there any discernible difference between either example, but the `<q>` tag should still be used when applicable (see [`<q>`: The Inline Quotation element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q) for more information).

<hr>

## `<s>`

    <p><s>There are 10 spots left.</s></p>
    <p>Only 2 spots left!</p>

    <p>There are 10 spots left</p>
    <p>Only 2 spots left!</p>

**Screen reader:** "There are ten spots left. Only two spots left."

**Example Notes:** The screen reader did not give any indication that the first example was using an `<s>` tag nor was there any discernible difference between either example, but the `<s>` tag should still be used when applicable (see [MDN's page on the `<s>` tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/s) for more information).

<hr>

## `<samp>`

    <samp>An error message from a program</samp>

    <p>An error message from a program</p>

**Screen reader:** "An error message from a program."

**Example Notes:** The screen reader did not give any indication that the first example was using a `<samp>` tag nor was there any discernible difference between either example, but the `<samp>` tag should still be used when applicable (see [`<samp>`: The Sample Output element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/samp) for more information).

<hr>

## `<small>`

    <small>Copyright 2021 Nobody, Inc.</small>

    <p>Copyright 2021 Nobody, Inc.</p>

**Screen reader:** "Copyright twenty twenty-one Nobody Incorporated."

**Example Notes:** The screen reader did not give any indication that the first example was using a `<small>` tag nor was there any discernible difference between either example, but the `<small>` tag should still be used when applicable (see [`<small>`: the side comment element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/small) for more information).

<hr>

## `<sub>` and `<sup>`

    <p>This is an example of <sub>subscript text</sub> and <sup>superscripted text</sup>.</p>

    <p>This is an example of subscript text and superscripted text.</p>

**Screen reader:** "This is an example of subscript text and superscript text."

**Example Notes:** The screen reader did not give any indication that the first example was using a `<sub>` or `<sup>` tag nor was there any discernible difference between either example, but the `<sub>` or `<sup>` tags should still be used when applicable (see [`<sub>`: The Subscript element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sub) and [`<sup>`: The Superscript element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sup) for more information).

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

<hr>

## `textarea>`

    <textarea></textarea>

**Screen reader (Firefox - on page load):** "Edit multi-line out of edit"

**Screen reader (Chrome and Edge - on page load):** "Edit multi-line"

**Screen reader (using the `tab` key to navigate the page):** "Edit multi-line blank"

<br>

    <label>
      Leave a review:
      <textarea></textarea>
    </label>

**Screen reader (Firefox - on page load):** "Clickable leave a review, edit multi-line out of edit."

**Screen reader (Chrome and Edge - on page load):** "Leave a review, edit multi-line."

**Screen reader (using the `tab` key to navigate the page):** "Leave a review, edit multiline blank."

<br>

**Notes:** If the text area has text entered into it when navigating to it with the `tab` key, the screen reader may announce the content of the text-area rather than "blank".

<hr>

## `<var>`

    <p>I declared <var>number</var> as a variable.</p>
    
    <p>I declared number as a variable.</p>

**Screen reader:** "I declared number as a variable."

**Example Note:** The screen reader did not give any indication that the first example was using a `<var>` tag nor was there any discernible difference between either example, but the `<var>` tag should still be used when applicable (see [`<var>`: The Variable element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/var) for more information).

