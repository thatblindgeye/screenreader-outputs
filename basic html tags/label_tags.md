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

**Screen reader (Firefox):** "Name edit has auto-complete blank."

**Screen reader (Chrome):** "Name edit blank."

**Examples Note:** There was no discernible difference between either example when using the same browser. Wrapping an input inside the label tag from the first example gave the same output as using the `for` attribute from the second example. 
