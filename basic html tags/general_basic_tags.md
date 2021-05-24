# General Basic Tags

<br><br>

## `<b>`, `<em>`, `<i>`, `mark`, `<strong>`, and `<u>`

    <p>This is a sentence with <b>emphasized</b> text.</p>


    <p>This is a sentence with <strong>emphasized</strong> text.</p>


    <p>This is a sentence with <em>emphasized</em> text.</p>


    <p>This is a sentence with <u>emphasized</u> text.</p>


    <p>This is a sentence with <i>emphasized</i> text.</p>
    
**Screen reader:** "This is a sentence with emphasized text."

**Examples Notes:** There is no discernible emphasis in any of the above examples, but the appropriate tag should still be used when applicable.

<br>

    <p>This is a sentence with <mark>highlighted</mark> text.</p>

**Screen reader:** "This is a sentence with marked-content highlighted out of marked-content text."

<br><br>

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

**Examples Note:** The screen reader did not give any indication that the first example was using an `<address>` tag nor was there any discernible difference between either example, but the `<address>` tag should still be used when applicable.

<br><br>

## `<blockquote>`

    <blockquote cite="https://www.w3.org/Help/#activity">
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </blockquote>

**Screen reader:** "blockquote W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission out of blockquote".

**Example Notes:** the "blockquote" and "out of blockquote" text was only announced when the screen reader was reading the contents of the page, or when navigating the page using the `up arrow` and `down arrow` keys.

<br>

    <p>
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </p>

**Screen reader:** "W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission".

<br><br>

## `<cite>`

    <p><cite>The Starry Night</cite> by Vincent van Gogh</p>

    <p>The Starry Night by Vincent van Gogh</p>

**Screen reader:** "The Starry Night by Vincent Van Gogh"

**Examples Notes:** The screen reader did not give any indication that the first example was using a `<cite>` tag nor was there any discernible difference between either example, but the `<cite>` tag should still be used when applicable.

<br><br>

## `<code>`

    <p>The <code>code</code> HTML tag should be used to define text as computer code.</p>

    <p>The code HTML tag should be used to define text as computer code.</p>

**Screen reader:** "The code HTML tag should be used to define text as computer code."

**Examples Notes:** The screen reader did not give any indication of which part of the text was inside the `<code>` tag, but the tag should still be used when applicable.

<br><br>

## `<data>`

    <data value="12345">HP Laptop</data>

    <p>HP Laptop</p>

**Screen reader:** "HP laptop."

**Examples Notes:** The screen reader did not give any indication that the first example was using a `<data>` tag nor was there any discernible difference between either example, but the `<data>` tag should still be used when applicable.

<br><br>

## `<del>` and `<ins>`

    <p>My favorite color is <del>red</del> <ins>purple.</ins></p>

**Screen reader:** "My favorite color is deleted red inserted purple."

<br><br>

## `<dialog>`

    <dialog open>Thank you for checking out this repo!</dialog>

**Screen reader:** "Dialog."

**Example Notes:** The screen reader did not announce the text content of the dialog tag itself. 

<br>

    <dialog open tabindex='0'>Thank you for checking out this repo!</dialog>

**Screen reader (using the `tab` key to navigate the page):** "Dialog thank you for checking out this repo."

**Example Notes:** Check the browser/screen reader support for the `<dialog>` tag before using it.

<br><br>

## `<h1>` to `<h6>`

    <h1>An H1 tag</h1>

**Screen reader:** "An h one tag heading level one."

**Example Notes:** The screen reader announced the other remaining 5 heading tags similarly ("an h two tag heading level two", etc.).

<br><br>

## `<iframe>`

    <iframe src="https://www.w3.org/WAI/"></iframe>

**Screen reader:** "Frame..."

**Example Notes:** After the initial output above, the screen reader began to announce the content inside the iframe.

<br>

    <iframe src="https://www.w3.org/WAI/" title="Web Accessibility Initiative"></iframe>

**Screen reader:** "Web Accessibility Initiative frame..."

**Example Notes:** The title attribute should be included to give screen readers context of the embedded content.

<br><br>

## `<img>`

    <img src="//unsplash.it/500" alt="A random image from Unsplash">

**Screen reader:** "Graphic a random image from Unsplash."

<br>

    <img src="//unsplash.it/500" alt="">

**Example Notes:** The screen reader did not announce the presence of the image when navigating the page with the `up arrow` and `down arrow` keys, or when the page first loaded and the screen reader announced the contents of the page.

<br>

    <img src="//unsplash.it/500">
    
**Screen reader (Chrome - on page load):** "Unlabeled graphic. To get missing image descriptions, open the context menu."

<br>

    <img src="//unsplash.it/500" alt="" tabindex="0">

**Screen reader (using the `tab` key to navigate the page):** "Blank."

<br>

    <img src="//unsplash.it/500" tabindex="0">

**Screen reader (Firefox and Edge - using the `tab` key to navigate the page):** "600 graphic."

**Screen reader (Chrome - using the `tab` key to navigate the page):** "600 Unlabelled graphic."

<hr>

**Notes:** When using images as decoration, the `alt` attribute should be used with an empty string rather than omitted, some some screen readers or browsers may announce such an image in some way. Checkout the W3 [Decorative Images](https://www.w3.org/WAI/tutorials/images/decorative/) page for further information.

<br><br>

## `<kbd>`

    <p>My keyboard is broken, so I have to copy and paste the <kbd>t</kbd> key.</p>

    <p>My keyboard is broken, so I have to copy and paste the t key.</p>

**Screen reader:** "My keyboard is broken, so I have to copy and paste the t key"

**Example Notes:** The screen reader did not give any indication that the first example was using a `<kbd>` tag nor was there any discernible difference between either example, but the `<kbd>` tag should still be used when applicable.

<br><br>

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

**Examples Notes:** The screen reader did not give any indication that the first example was using a `<pre>` tag nor was there any discernible difference between either example, but the `<pre>` tag should still be used when applicable.

When using the `<pre>` tag to create an image with text characters, for example, you should provide an alternative caption for screen readers. Check out the [MDN page on the pre tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre#accessibility_concerns) for an example.

<br><br>

## `<q>`

    <p><q>This is a quoted section of text,</q> said the paragraph tag.</p>

    <p>"This is a quoted section of text," said the paragraph tag.</p>

**Screen reader:** "This is a quoted section of text said the paragraph tag."

**Examples Notes:** The screen reader did not give any indication that the first example was using a `<q>` tag nor was there any discernible difference between either example, but the `<q>` tag should still be used when applicable.

<br><br>

## `<s>`

    <p><s>There are 10 spots left.</s></p>
    <p>Only 2 spots left!</p>

    <p>There are 10 spots left</p>
    <p>Only 2 spots left!</p>

**Screen reader:** "There are ten spots left. Only two spots left."

**Examples Notes:** The screen reader did not give any indication that the first example was using an `<s>` tag nor was there any discernible difference between either example, but the `<s>` tag should still be used when applicable.

<br><br>

## `<samp>`

    <samp>An error message from a program</samp>

    <p>An error message from a program</p>

**Screen reader:** "An error message from a program."

**Examples Notes:** The screen reader did not give any indication that the first example was using a `<samp>` tag nor was there any discernible difference between either example, but the `<samp>` tag should still be used when applicable.

<br><br>

## `<small>`

    <small>Copyright 2021 Nobody, Inc.</small>

    <p>Copyright 2021 Nobody, Inc.</p>

**Screen reader:** "Copyright twenty twenty-one Nobody Incorporated."

**Examples Notes:** The screen reader did not give any indication that the first example was using a `<small>` tag nor was there any discernible difference between either example, but the `<small>` tag should still be used when applicable.

<br><br>

## `<sub>` and `<sup>`

    <p>This is an example of <sub>subscript text</sub> and <sup>superscripted text</sup>.</p>

    <p>This is an example of subscript text and superscripted text.</p>

**Screen reader:** "This is an example of subscript text and superscript text."

**Examples Notes:** The screen reader did not give any indication that the first example was using a `<sub>` or `<sup>` tag nor was there any discernible difference between either example, but the `<sub>` or `<sup>` tags should still be used when applicable.

<br><br>

## `textarea>`

    <textarea></textarea>

**Screen reader (Firefox - on page load):** "Edit multi-line out of Edit"

**Screen reader (Chrome and Edge - on page load):** "Edit multi-line"

**Screen reader (using the `tab` key to navigate the page):** "Edit multi-line blank"

**Example Notes:** If the text area has text entered into it when navigating to it with the `tab` key, the screen reader may announce the content of the text-area rather than "blank".

<br>

    <label>
      Leave a review:
      <textarea></textarea>
    </label>

**Screen reader (Firefox - on page load):** "Clickable leave a review, edit multi-line out of Edit."

**Screen reader (Chrome and Edge - on page load):** "Leave a review, edit multi-line."

**Screen reader (using the `tab` key to navigate the page):** "Leave a review, edit multiline blank. "

<br><br>

## `<var>`

    <p>I declared <var>number</var> as a variable.</p>
    
    <p>I declared number as a variable.</p>

**Screen reader:** "I declared number as a variable."

**Examples Note:** The screen reader did not give any indication that the first example was using a `<var>` tag nor was there any discernible difference between either example, but the `<var>` tag should still be used when applicable.

<br><br>
