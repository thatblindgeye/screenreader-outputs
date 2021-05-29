# General Basic Elements

This section covers elements that may not require their own section, either due to the outputs being straight forward enough or there not being enough examples or notes for the example to warrant its own section.

<br><br>

## `<b>`, `<em>`, `<i>`, `mark`, and `<strong>`

    <p>This is a sentence with <b>emphasized</b> text.</p>


    <p>This is a sentence with <strong>emphasized</strong> text.</p>


    <p>This is a sentence with <em>emphasized</em> text.</p>


    <p>This is a sentence with <u>emphasized</u> text.</p>


    <p>This is a sentence with <i>emphasized</i> text.</p>

**Screen reader:** "This is a sentence with emphasized text."

**Example Notes:** There was no discernible emphasis in any of the above examples, but the appropriate element should still be used when applicable (see [`<b>`: The Bring Attention To element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/b), [`<strong>`: The Strong Importance element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong), [`<em>`: The Emphasis element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em), [`<u>`: The Unarticulated Annotation (Underline) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/u), and [`<i>`: The Idiomatic Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i) for more information).

<br><br>

## `<u>`

    <p>This is a sentence with <mark>highlighted</mark> text.</p>

**Screen reader:** "This is a sentence with marked-content highlighted out of marked-content text."

<br>
<hr>
<br>

## `<abbr>` and `<dfn>`

    <p><abbr title="Cascading Style Sheets">CSS</abbr> is a language that describes the style of an HTML document.</p>

    <p><dfn><abbr title="Cascading Style Sheets">CSS</abbr></dfn> is a language that describes the style of an HTML document.</p>

    <p><dfn>CSS</dfn> is a language that describes the style of an HTML document.</p>

    <p>CSS is a language that describes the style of an HTML document.</p>

**Screen reader:** "CSS is a language that describes the style of an HTML document."

<br>

**Notes:** The screen reader did not give any indication that the first example was using an `<abbr>` or `<dfn>` element nor was there any discernible difference between the examples, but the `<abbr>` and `<dfn>` elements should still be used when applicable (see [`<abbr>`: The Abbreviation element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr) and [`<dfn>`: The Definition element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dfn) for more information).

The title attribute on the `<abbr>` element may be capabale of being announced via the JAWS screen reader by adjusting the settings, but otherwise may not get announced.

<br>
<hr>
<br>

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

<br>

**Example Note:** The screen reader did not give any indication that the first example was using an `<address>` element nor was there any discernible difference between either example, but the `<address>` element should still be used when applicable (see [`<address>`: The Contact Address element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address) for more information).

<br>
<hr>
<br>

## `<blockquote>`

    <blockquote cite="https://www.w3.org/Help/#activity">
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </blockquote>

**Screen reader:** "Blockquote. W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission. Out of blockquote".

<br>

    <p>
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </p>

**Screen reader:** "W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission".

<br>
<hr>
<br>

## `<cite>`

    <p><cite>The Starry Night</cite> by Vincent van Gogh</p>

    <p>The Starry Night by Vincent van Gogh</p>

**Screen reader:** "The Starry Night by Vincent Van Gogh"

<br>

**Example Notes:** The screen reader did not give any indication that the first example was using a `<cite>` element nor was there any discernible difference between either example, but the `<cite>` element should still be used when applicable (see [`<cite>`: The Citation element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite) for more information).

<br>
<hr>
<br>

## `<code>`

    <p>The <code>code</code> HTML element should be used to define text as computer code.</p>

    <p>The code HTML element should be used to define text as computer code.</p>

**Screen reader:** "The code HTML element should be used to define text as computer code."

<br>

**Examples Notes:** The screen reader did not give any indication that the first example was using a `<code>` element nor was there any discernible difference between either example, but the `<code>` element should still be used when applicable (see [`<code>`: The Inline Code element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code) for more information).

<br>
<hr>
<br>

## `<data>`

    <data value="12345">HP Laptop</data>

    <p>HP Laptop</p>

**Screen reader:** "HP laptop."

<br>

**Example Notes:** The screen reader did not give any indication that the first example was using a `<data>` element nor was there any discernible difference between either example, but the `<data>` element should still be used when applicable (see [MDN's page on the `<data>` element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/data) for more information).

<br>
<hr>
<br>

## `<del>` and `<ins>`

    <p>My favorite color is <del>red</del> <ins>purple.</ins></p>

**Screen reader:** "My favorite color is deleted red inserted purple."

<br>
<hr>
<br>

## `<details>` and `<summary>`

    <details>
        <summary>Avatar: The Last Airbender</summary>
        <p>Avatar: The Last Airbender is an American animated television series produced by Nickelodeon Animation Studios.</p>
    </details>

**Screen reader:** "Button, collapsed, Avatar The Last Airbender."

<br>

**Notes:** When pressing the `space` or `Enter` keys when the `<summary>` element had focus, the screen reader announced the new state of the element, e.g. "collapsed" or "expanded".

When the `<summary>` element is expanded, the screen reader announced the text within the `<details>` element only after pressing the `down arrow` key and did not automatically start announcing the text content of the `<details>` element.

<br>
<hr>
<br>

## `<dialog>`

    <dialog open>Thank you for checking out this repo!</dialog>

**Screen reader:** "Dialog."

<br>

**Example Notes:** The screen reader did not announce the text content of the dialog element itself.

<br><br>

    <dialog open tabindex='0'>Thank you for checking out this repo!</dialog>

**Screen reader (`tab` key to give focus to the dialog):** "Dialog, thank you for checking out this repo."

<br>

**Example Notes:** Check the browser/screen reader support at [`<dialog>`: The Dialog element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog) before using this element.

<br>
<hr>
<br>

## `<figure>` and `<figcaption>`

    <figure>
        <img src="//unsplash.it/250" alt="Unsplash sample">
        <figcaption>Fig.1 - A random Unsplash picture.</figcaption>
    </figure>

**Screen reader (on page load):** "Figure, graphic, Unsplash sample." and "Caption, fig dot one a random Unsplash picture."

<br>

**Notes:** When using the `up arrow` or `down arrow` keys to navigate the page, the `<figure>` and `<figcaption>` elements were announced individually, but with the same outputs as above.

<br>
<hr>
<br>

## `<h1>` to `<h6>`

    <h1>An H1 element</h1>

**Screen reader:** "An h one element, heading level one."

<br>

**Example Notes:** The screen reader announced the other remaining 5 heading elements similarly ("an h two element, heading level two", etc.).

<br>
<hr>
<br>

## `<iframe>`

    <iframe src="https://www.w3.org/WAI/"></iframe>

**Screen reader:** "Frame..."

<br><br>

    <iframe src="https://www.w3.org/WAI/" title="Web Accessibility Initiative"></iframe>

**Screen reader:** "Web Accessibility Initiative frame..."

<br>

**Notes:** The title attribute should be included to give screen readers context of the embedded content.

After the initial output of the examples above, the screen reader began to announce the content inside the iframe.

<br>
<hr>
<br>

## `<kbd>`

    <p>My keyboard is broken, so I have to copy and paste the <kbd>t</kbd> key.</p>

    <p>My keyboard is broken, so I have to copy and paste the t key.</p>

**Screen reader:** "My keyboard is broken, so I have to copy and paste the t key"

<br>

**Example Notes:** The screen reader did not give any indication that the first example was using a `<kbd>` element nor was there any discernible difference between either example, but the `<kbd>` element should still be used when applicable (see [`<kbd>`: The Keyboard Input element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd) for more information).

<br>
<hr>
<br>

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

<br>

**Example Notes:** The screen reader did not give any indication that the first example was using a `<pre>` element nor was there any discernible difference between either example, but the `<pre>` element should still be used when applicable (see [`<pre>`: The Preformatted Text element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre) for more information).

When using the `<pre>` element to create an image with text characters, for example, you should provide an alternative caption for screen readers. See the link for the `pre` element above for an example.

<br>
<hr>
<br>

## `<q>`

    <p><q>This is a quoted section of text,</q> said the paragraph element.</p>

    <p>"This is a quoted section of text," said the paragraph element.</p>

**Screen reader:** "This is a quoted section of text said the paragraph element."

<br>

**Example Notes:** The screen reader did not give any indication that the first example was using a `<q>` element nor was there any discernible difference between either example, but the `<q>` element should still be used when applicable (see [`<q>`: The Inline Quotation element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q) for more information).

<br>
<hr>
<br>

## `<s>`

    <p><s>There are 10 spots left.</s></p>
    <p>Only 2 spots left!</p>

    <p>There are 10 spots left</p>
    <p>Only 2 spots left!</p>

**Screen reader:** "There are ten spots left. Only two spots left."

<br>

**Example Notes:** The screen reader did not give any indication that the first example was using an `<s>` element nor was there any discernible difference between either example, but the `<s>` element should still be used when applicable (see [MDN's page on the `<s>` element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/s) for more information).

<br>
<hr>
<br>

## `<samp>`

    <samp>An error message from a program</samp>

    <p>An error message from a program</p>

**Screen reader:** "An error message from a program."

<br>

**Example Notes:** The screen reader did not give any indication that the first example was using a `<samp>` element nor was there any discernible difference between either example, but the `<samp>` element should still be used when applicable (see [`<samp>`: The Sample Output element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/samp) for more information).

<br>
<hr>
<br>

## `<small>`

    <small>Copyright 2021 Nobody, Inc.</small>

    <p>Copyright 2021 Nobody, Inc.</p>

**Screen reader:** "Copyright twenty twenty-one Nobody Incorporated."

<br>

**Example Notes:** The screen reader did not give any indication that the first example was using a `<small>` element nor was there any discernible difference between either example, but the `<small>` element should still be used when applicable (see [`<small>`: the side comment element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/small) for more information).

<br>
<hr>
<br>

## `<sub>` and `<sup>`

    <p>This is an example of <sub>subscript text</sub> and <sup>superscripted text</sup>.</p>

    <p>This is an example of subscript text and superscripted text.</p>

**Screen reader:** "This is an example of subscript text and superscript text."

<br>

**Example Notes:** The screen reader did not give any indication that the first example was using a `<sub>` or `<sup>` element nor was there any discernible difference between either example, but the `<sub>` or `<sup>` elements should still be used when applicable (see [`<sub>`: The Subscript element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sub) and [`<sup>`: The Superscript element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sup) for more information).

<br>
<hr>
<br>

## `textarea>`

    <textarea></textarea>

**Screen reader (Firefox - on page load):** "Edit, multi-line, out of edit"

**Screen reader (Chrome and Edge - on page load):** "Edit, multi-line"

**Screen reader (`tab` key to give focus to the textarea):** "Edit, multi-line blank"

<br><br>

    <label>
      Leave a review:
      <textarea></textarea>
    </label>

**Screen reader (Firefox - on page load):** "Clickable, leave a review, edit, multi-line, out of edit."

**Screen reader (Chrome and Edge - on page load):** "Leave a review, edit, multi-line."

**Screen reader (`tab` key to give focus to the textarea):** "Leave a review, edit, multiline blank."

<br>

**Notes:** If the text area has text entered into it when navigating to it with the `tab` key, the screen reader may announce the content of the text-area rather than "blank".

<br>
<hr>
<br>

## `<var>`

    <p>I declared <var>number</var> as a variable.</p>

    <p>I declared number as a variable.</p>

**Screen reader:** "I declared number as a variable."

<br>

**Example Note:** The screen reader did not give any indication that the first example was using a `<var>` element nor was there any discernible difference between either example, but the `<var>` element should still be used when applicable (see [`<var>`: The Variable element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/var) for more information).
