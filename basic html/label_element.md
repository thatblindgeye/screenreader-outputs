# `<label>`

## Just a Label

    <label>Name:</label>

**Screen reader:** "Name."

<br><br>

## A Label and an Input

    <label>
      Name:
      <input type="text">
    </label>

    <label for="name">Name:</label>
    <input type="text" id="name">

**Screen reader (Firefox - on page load):** "Clickable Name edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Name edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Name edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Name edit blank."

<br>

**Example Notes:** Wrapping an input inside the `<label>` element in the first example gave the same output as using the `for` attribute in the second example.
