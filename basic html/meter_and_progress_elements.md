# `<meter>` and `<progress>`

Although the screen reader announces both the `<meter>` and `<progress>` elements similarly, they both have their own semantic purpose and should be used as such.

<br><br>

## `<meter>`

### Without a Label - Currency for Text Content

    <meter value="1000" min="0" max="5000">$1000 out of $5000</meter>

**Screen reader (Firefox):** "Progress bar one thousand dollars out of five thousand dollars."

**Screen reader (Chrome and Edge):** "Progress bar one thousand."

<br><br>

### With a Label - Decimal Value

    <label>
      Donation Goal:
      <meter value="0.31">31%</meter>
    </label>

**Screen reader (Firefox):** "Donation goal, progress bar thirty-one percent."

**Screen reader (Chrome and Edge):** "Donation goal, progress bar zero point three one zero zero zero zero zero zero two three eight four one eight five eight."

<br><br>

### With a Label - Integer Value

    <label>
      Donation Goal:
      <meter value="31" min='0' max='100'>31%</meter>
    </label>

**Screen reader (Firefox):** "Donation goal, progress bar thirty-one percent."

**Screen reader (Chrome and Edge):** "Donation goal, progress bar thirty-one."

<br><br>

### With a Label - Currency for Text Content

    <label>
      Donation Goal:
      <meter value="1000" min="0" max="5000">$1000 out of $5000</meter>
    </label>

**Screen reader (Firefox):** "Donation goal, progress bar one thousand dollars out of five thousand dollars."

**Screen reader (Chrome and Edge):** "Donation goal, progress bar one thousand."

<br>
<hr>
<br>

## `<progress>`

### Without a Label

    <progress value="89" max="100">89%</progress>

**Screen reader (Firefox):** "Progress bar eighty-nine percent."

**Screen reader (Chrome and Edge):** "Progress bar eighty-nine."

<br><br>

### With a Label

    <label>
      Download:
      <progress value="89" max="100">89%</progress>
    </label>

**Screen reader (Firefox):** "Download, progress bar eighty-nine percent."

**Screen reader (Chrome and Edge):** "Download, progress bar eighty-nine."
