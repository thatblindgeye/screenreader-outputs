# `<label>`

    <label>Name:</label>

**Screen reader:** "Name."

<br>

    <label>
      Name:
      <input type="text">
    </label>

    <label for="name">Name:</label>
    <input type="text" id="name">

**Screen reader (Firefox - on page load):** "Clickable Name edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Name edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Name edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Name edit blank."

**Example Notes:** There was no discernible difference between either example when using the same browser. Wrapping an input inside the label tag from the first example gave the same output as using the `for` attribute from the second example. 
