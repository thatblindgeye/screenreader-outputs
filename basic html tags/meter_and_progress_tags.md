# `<meter>` and `<progress>`

    <meter value="1000" min="0" max="5000">$1000 out of $5000</meter>

**Screen reader (Firefox):** "Progress bar one thousand dollars out of five thousand dollars."

**Screen reader (Chrome):** "Progress bar one thousand."

<br>

    <label>
      Donation Goal:
      <meter value="0.31">31%</meter>
    </label>

**Screen reader (Firefox):** "Donation goal, progress bar thirty-one percent."

**Screen reader (Chrome):** "Donation goal, progress bar zero point three one zero zero zero zero zero zero two three eight four one eight five eight."

<br>

    <label>
      Donation Goal:
      <meter value="31" min='0' max='100'>31%</meter>
    </label>

**Screen reader (Firefox):** "Donation goal, progress bar thirty-one percent."

**Screen reader (Chrome):** "Donation goal, progress bar thirty-one."

<br>

    <label>
      Donation Goal:
      <meter value="1000" min="0" max="5000">$1000 out of $5000</meter>
    </label>


**Screen reader (Firefox):** "Donation goal, progress bar one thousand dollars out of five thousand dollars."

**Screen reader (Chrome):** "Donation goal, progress bar one thousand."

<br>

    <progress value="89" max="100">89%</progress>

**Screen reader (Firefox):** "Progress bar eighty-nine percent."

**Screen reader (Chrome):** "Progress bar eighty-nine."

<br>

    <label>
      Download:
      <progress value="89" max="100">89%</progress>
    </label>

**Screen reader (Firefox):** "Download, progress bar eighty-nine percent."

**Screen reader (Chrome):** "Download, progress bar eighty-nine."

<br><br>

**Note:** Although the screen reader announced both `<meter>` and `<progress>` tags similarly, they both have their own semantic purpose and should be used as such.
