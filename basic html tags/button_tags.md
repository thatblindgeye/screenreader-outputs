# `<button>`

    <button type="button" value="Add"></button>

**Screen reader:** "button"

<br><br>

    <button type="button">Confirm</button>

**Screen reader:** "confirm button"

<br><br>

    <button type="button" value="fruit">Apple</button>

**Screen reader:** "apple button"

<br><br>

    <button type="button" disabled>Disabled</button>

**Screen reader (using the dedicated shortcut key to navigate all buttons on the page):** "disabled button unavailable"

**Example Notes:** When the page first loaded and the screen reader announced the contents of the page, the above output was also announced.

When tabbing to navigate the page, the screen reader did not announce the presence of the disabled button. This should be kept in mind in case a screen reader does not have a shortcut key to navigate all buttons on the page.

<br><br>

    <button type="button" autofocus>Autofocused</button>

**Screen reader:** "Autofocused button"

**Example Notes:** The screen reader announced this button when the page finished loading, and may or may not then announce the contents of the entire page afterwards.

<br><br>

    <button type="submit">Submit Form</button>

**Screen reader:** "submit form button"

<br><br>

    <button type="reset">Reset Form</button>

**Screen reader:** "reset form button"

<hr>

**Notes:** The type of button was not announced by the screen reader, only the text contents of the button itself.
