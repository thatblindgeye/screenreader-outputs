#General Basic Tags

## Some quick notes

Tags such as `<b>`, `<em>`, `<i>`, `mark`, `<strong>`, and `<u>` may not be announced by a screen reader with any emphassis.

ARIA Landmark tags are: `<article>`, `<aside>`, `<footer>`, `<form>`, `<header>`, `<main>`, `<nav>`, and `<section>`. These semantic tags can help screen reader users navigate through a web page.

The `<div>` and `<span>` tags do not have any special announcement from a screen reader on their own.
<br><br>

## `<b>`, `<em>`, `<i>`, `mark`, `<strong>`, and `<u>`

    <p>This is a sentence with <b>emphasized</b> text.</p>

**Screen reader announces:** ""

    <p>This is a sentence with <strong>emphasized</strong> text.</p>

**Screen reader announces:** ""

    <p>This is a sentence with <em>emphasized</em> text.</p>

**Screen reader announces:** ""

    <p>This is a sentence with <u>emphasized</u> text.</p>

**Screen reader announces:** ""

    <p>This is a sentence with <i>emphasized</i> text.</p>

**Screen reader announces:** ""

    <p>This is a sentence with <mark>highlighted</mark> text.</p>

**Screen reader announces:** ""

    <p>This is a sentence with no emphasized text.</p>

**Screen reader announces:** ""

<br><br>

## `<address>`

    <address>
      John Smith</br>
      123 Fake St</br>
      Fakesville, OH 12345
    </address>

**Screen reader announces:** ""

    <p>
      John Smith</br>
      123 Fake St</br>
      Fakesville, OH 12345
    </p>

**Screen reader announces:** ""
<br><br>

## `<blockquote>`

    <blockquote cite="https://www.w3.org/Help/#activity">
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </blockquote>

**Screen reader announces:** ""

    <p>
        W3C's primary activity is to develop protocols and guidelines that ensure long-term growth for the Web. W3C's standards define key parts of what makes the World Wide Web work. Learn more about W3C's mission.
    </p>

**Screen reader announces:** ""
<br><br>

## `<cite>`

    <p><cite>The Starry Night</cite> by Vincent van Gogh</p>

**Screen reader announces:** ""

    <p>The Starry Night by Vincent van Gogh</p>

**Screen reader announces:** ""
<br><br>

## `<code>`

    <p>The <code>code</code> HTML tag should be used to define text as computer code.</p>

**Screen reader announces:** ""

    <p>The code HTML tag should be used to define text as computer code.</p>

**Screen reader announces:** ""
<br><br>

## `<data>`

    <data value="12345">HP Laptop</data>

**Screen reader announces:** ""

    <p>HP Laptop</p>

**Screen reader announces:** ""
<br><br>

## `<del>` and `<ins>`

    <p>My favorite color is <del>red</del> <ins>purple</ins>.</p>

**Screen reader announces:** ""

## `<dialog>`

    <dialog open>Thank you for checking out this repo!</dialog>

**Screen reader announces:** ""
**Note:** Check the browser support for this tag before using it.
<br><br>

## `<h1>` to `<h6>`

    <h1>An H1 tag</h1>
    <h2>An H2 tag</h2>
    <h6>An H6 tag</h6>

**Screen reader announces:** A screen reader will announce the heading level of the tag followed by the text contents of the tag, e.g. "heading level one 'an h1 tag'".

<br><br>

## `<iframe>`

    <iframe src="https://www.w3.org/WAI/"></iframe>

**Screen reader announces:** ""

    <iframe src="https://www.w3.org/WAI/" title="Web Accessibility Initiative"></iframe>

**Screen reader announces:** ""

**Note:** The title attribute should be included to give screen readers context of the embedded content.

<br><br>

## `<img>`

    <img src="//unsplash.it/500" alt="A random image from Unsplash">

**Screen reader announces:** ""

    <img src="//unsplash.it/500" alt="">

**Screen reader announces:** ""

**Note:** Per <a href="https://www.w3.org/WAI/tutorials/images/">WAI tutorials</a>, images that are only meant to add a visual decoration to a page (rather than convey any important value) should have a null text alternative, `alt=""`, rather than omitting the `alt` attribute.

<br><br>

## `<kbd>`

    <p>My keyboard is broken, so I have to copy and paste the <kbd>t</kbd> key.</p>

**Screen reader announces:**

    <p>My keyboard is broken, so I have to copy and paste the t key.</p>

**Screen reader announces:**

<br><br>

## `<p>`

    <p>Just a normal paragraph tag.</p>

**Screen reader announces:**

    <div>Text within a normal div tag</div>

**Screen reader announces:**

<br><br>

## `<pre>`

    <pre>
      An example of     what
      preformatted  text can
      look             like.
    </pre>

**Screen reader announces:**

    <p>
      Not an example of  what
      preformatted  text can
      look             like.
    </p>

**Screen reader announces:**

<br><br>

## `<q>`

    <p><q>This is a quoted section of text,</q> said the paragraph tag.</p>

**Screen reader announces:**

    <p>"This is a quoted section of text," said the paragraph tag.</p>

**Screen reader announces:**

<br><br>

## `<s>`

    <p><s>There are 10 spots left.</s></p>
    <p>Only 2 spots left!</p>

**Screen reader announces:**

<br><br>

## `<samp>`

    <samp>An error message from a program</samp>

**Screen reader announces:**

    <p>An error message from a program</p>

**Screen reader announces:**

<br><br>

## `<small>`

    <small>Copyright 2021 Nobody, Inc.</small>

**Screen reader announces:**

    <p>Copyright 2021 Nobody, Inc.</p>

**Screen reader announces:**

<br><br>

## `<sub>` and `<sup>`

    <p>This is an example of <sub>subscript text</sub> and <sup>superscripted text</sup>.</p>

**Screen reader announces:**

<br><br>

## `textarea>`

    <textarea></textarea>

**Screen reader announces:**

    <label>
      Leave a review:
      <textarea></textarea>
    </label>

**Screen reader announces:**

<br><br>

## `<var>`

    <p>I declared <var>number</var> as a variable.</p>

**Screen reader announces:**

    <p>I declared number as a variable.</p>

**Screen reader announces:**

<br><br>
