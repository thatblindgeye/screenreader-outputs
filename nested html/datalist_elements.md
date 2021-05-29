# Datalists

    <form>
        <label>
            Enter your favorite dice:
            <input list="dice-list" name="dice" id="dice">
        </label>
        <datalist id="dice-list">
          <option value="four sided dice">
          <option value="six sided dice">
          <option value="eight sided dice">
          <option value="ten sided dice">
          <option value="twelve sided dice">
          <option value="twenty sided dice">
        </datalist>
    </form>

**Screen reader (Firefox - on page load):** "Clickable enter your favorite dice, combo-box has auto-complete editable."

**Screen reader (Firefox - `up arrow` and `down arrow` to open the datalist when input is blank):** "Blank."

**Screen reader (Chrome and Edge - on page load):** "Enter your favorite dice, combo-box has auto-complete editable."

**Screen reader (`tab` key to give focus to the input):** "Enter your favorite dice, combo-box has auto-complete editable blank."

**Screen reader (`up arrow` and `down arrow` to cycle through the datalist):** The screen reader announced the current selection value followed by its position in the list, e.g. "four sided dice, one of six". In Edge, it announced the position as "dot one of six".

<br>

**Example notes:** In Chrome and Edge, the list was automatically expanded upon entering the input field, whereas in Firefox only pressing the `up arrow` or `down arrow` keys or entering text that was found in one of the list options expanded the list.

When first entering the expanded list in Chrome and Edge, the screen reader announced "Autofill list expanded" followed by the current selection value and its position in the list. In Firefox, the screen reader only announced "list" followed by the current selection value and its position in the list.

When the input was filled in with a selection from the datalist, the screen reader announced the text "selected" along with the selection, e.g. "Enter your favorite dice, combo-box has auto-complete editable selected four sided dice".

When pressing the `Escape` key to collapse the datalist, the screen reader did not announce the datalist had collapsed, but instead had the same output as though the input had been given focus again.
