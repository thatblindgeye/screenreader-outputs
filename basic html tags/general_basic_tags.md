# General Basic Tags

<br><br>

## `<b>`, `<em>`, `<i>`, `mark`, `<strong>`, and `<u>`

    <p>This is a sentence with <b>emphasized</b> text.</p>


    <p>This is a sentence with <strong>emphasized</strong> text.</p>


    <p>This is a sentence with <em>emphasized</em> text.</p>


    <p>This is a sentence with <u>emphasized</u> text.</p>


    <p>This is a sentence with <i>emphasized</i> text.</p>
    
**Screen reader:** "This is a sentence with emphasized text."

**Examples Note:** There is no discernible emphasis in any of the above examples, but the appropriate tag should still be used when applicable.

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

**Examples Note:** The screen reader did not give any indication that the first example was using an `<address>` tag nor was there any discernible difference between either example, but the `<address>` tag should still be used for semantics.

<br><br>

## `<blockquote>`

    <blockquote cite="https://www.w3.org/Help/#activity">
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </blockquote>

**Screen reader announces:** "blockquote W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission out of blockquote".

<br>

    <p>
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </p>

**Example Note:** The screen reader only announced the text as though it were a normal string of text, without any indication that it was a blockquote.

<br><br>

## `<cite>`

    <p><cite>The Starry Night</cite> by Vincent van Gogh</p>

    <p>The Starry Night by Vincent van Gogh</p>

**Screen reader:** "The Starry Night by Vincent Van Gogh"

**Examples Note:** The screen reader did not give any indication that the first example was using a `<cite>` tag nor was there any discernible difference between either example, but the `<cite>` tag should still be used when applicable.

<br><br>

## `<code>`

    <p>The <code>code</code> HTML tag should be used to define text as computer code.</p>

    <p>The code HTML tag should be used to define text as computer code.</p>

**Screen reader:** "The code HTML tag should be used to define text as computer code."

**Examples Note:** The screen reader did not give any indication of which part of the text was inside the `<code>` tag, but the tag should still be used when applicable.

<br><br>

## `<data>`

    <data value="12345">HP Laptop</data>

    <p>HP Laptop</p>

**Screen reader:** "HP laptop."

**Examples Note:** The screen reader did not give any indication that the first example was using a `<data>` tag nor was there any discernible difference between either example, but the `<data>` tag should still be used when applicable.

<br><br>

## `<del>` and `<ins>`

    <p>My favorite color is <del>red</del> <ins>purple.</ins></p>

**Screen reader:** "My favorite color is red deleted purple inserted."

<br><br>

## `<dialog>`

    <dialog open>Thank you for checking out this repo!</dialog>

**Screen reader:** "Dialog."

**Example Note:** The screen reader did not announce the text content of the dialog tag itself. 

<br>

    <dialog open tabindex='0'>Thank you for checking out this repo!</dialog>

**Screen reader:** "Dialog thank you for checking out this repo."

**Example Note:** The screen reader only announced the text content of the dialog when using the tab key to navigate the page.

**Note:** Check the browser/screen reader support for the `<dialog>` tag before using it.

<br><br>

## `<h1>` to `<h6>`

    <h1>An H1 tag</h1>

**Screen reader:** "An h one tag heading level one."

**Note:** The screen reader announced the other remaining 5 h tags similarly.

<br><br>

## `<iframe>`

    <iframe src="https://www.w3.org/WAI/"></iframe>

**Screen reader:** "Frame..."

**Example Note:** After the initial output above, the screen reader begins to announce the content inside the iframe.

<br>

    <iframe src="https://www.w3.org/WAI/" title="Web Accessibility Initiative"></iframe>

**Screen reader:** "Web Accessibility Initiative frame..."

**Note:** The title attribute should be included to give screen readers context of the embedded content.

<br><br>

## `<img>`

    <img src="//unsplash.it/500" alt="A random image from Unsplash">

**Screen reader:** "Graphic a random image from Unsplash."

<br>

    <img src="//unsplash.it/500" alt="">

**Screen reader (Firefox):** "Blank."

**Example Note:** Chrome did not announce anything when navigating through the page unless a tabindex of 0 was added to the image tag, and only when using the tab key to navigate the page.

**Note:** Per <a href="https://www.w3.org/WAI/tutorials/images/">WAI tutorials</a>, images that are only meant to add a visual decoration to a page (rather than convey any important value) should have a null text alternative, `alt=""`, rather than omitting the `alt` attribute.

<br><br>

## `<kbd>`

    <p>My keyboard is broken, so I have to copy and paste the <kbd>t</kbd> key.</p>

    <p>My keyboard is broken, so I have to copy and paste the t key.</p>

**Screen reader:** "My keyboard is broken, so I have to copy and paste the t key"

**Example Note:** The screen reader did not give any indication that the first example was using a `<kbd>` tag nor was there any discernible difference between either example, but the `<kbd>` tag should still be used when applicable.

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

**Examples Note:** The screen reader did not give any indication that the first example was using a `<pre>` tag nor was there any discernible difference between either example, but the `<pre>` tag should still be used when applicable.

**Note:** When using the `<pre>` tag to create an image with text characters, for example, one should provide an alternative caption for screen readers. Check out the [MDN page on the pre tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre#accessibility_concerns) for an example.

<br><br>

## `<q>`

    <p><q>This is a quoted section of text,</q> said the paragraph tag.</p>

    <p>"This is a quoted section of text," said the paragraph tag.</p>

**Screen reader:** "This is a quoted section of text said the paragraph tag."

**Examples Note:** The screen reader did not give any indication that the first example was using a `<q>` tag nor was there any discernible difference between either example, but the `<q>` tag should still be used when applicable.

<br><br>

## `<s>`

    <p><s>There are 10 spots left.</s></p>
    <p>Only 2 spots left!</p>

**Screen reader:** "There are ten spots left. Only two spots left."

<br><br>

## `<samp>`

    <samp>An error message from a program</samp>

    <p>An error message from a program</p>

**Screen reader:** "An error message from a program."

**Examples Note:** The screen reader did not give any indication that the first example was using a `<samp>` tag nor was there any discernible difference between either example, but the `<samp>` tag should still be used when applicable.

<br><br>

## `<small>`

    <small>Copyright 2021 Nobody, Inc.</small>

    <p>Copyright 2021 Nobody, Inc.</p>

**Screen reader:** "Copyright twenty twenty-one Nobody Incorporated."

**Examples Note:** The screen reader did not give any indication that the first example was using a `<small>` tag nor was there any discernible difference between either example, but the `<small>` tag should still be used when applicable.

<br><br>

## `<sub>` and `<sup>`

    <p>This is an example of <sub>subscript text</sub> and <sup>superscripted text</sup>.</p>

**Screen reader:** "This is an example of subscript text and superscript text."

**Examples Note:** The screen reader did not give any indication of the text being inside the `<sub>` or `<sup>` tags, but the tags should still be used when applicable.

<br><br>

## `textarea>`

    <textarea></textarea>

**Screen reader:** "Edit multi-line blank"

**Example Note:** If the text area has text entered into it when navigating to it, the screen reader may announce "Edit multi-line" followed by the content of the text-area.

<br>

    <label>
      Leave a review:
      <textarea></textarea>
    </label>

**Screen reader:** "Leave a review, edit multi-line blank."

<br><br>

## `<var>`

    <p>I declared <var>number</var> as a variable.</p>
    
    <p>I declared number as a variable.</p>

**Screen reader:** "I declared number as a variable."

**Examples Note:** The screen reader did not give any indication that the first example was using a `<var>` tag nor was there any discernible difference between either example, but the `<var>` tag should still be used when applicable.

<br><br>
