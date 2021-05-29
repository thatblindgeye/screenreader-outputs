# `<button>`

## Without Text Content

    <button type="button" value="Add"></button>

**Screen reader:** "Button"

<br><br>

## With Text Content

    <button type="button">Confirm</button>

    <button type="button" value="add">Confirm</button>

**Screen reader:** "Confirm button"

<br><br>

## With the `disabled` Attribute

    <button type="button" disabled>Submit</button>

**Screen reader (on page load or shortcut key to navigate between buttons):** "Submit, button, unavailable"

<br>

**Example Notes:** When tabbing to navigate the page, the screen reader did not announce the presence of the disabled button. This should be kept in mind in case a screen reader does not have a shortcut key to navigate all buttons on the page or when a user would naturally be tabbing between form inputs.

<br><br>

## With the `autofocus` Attribute

    <button type="button" autofocus>Click Here</button>

**Screen reader:** "Click here, button"

<br>

**Example Notes:** The screen reader announced this button when the page finished loading, and may or may not then announce the contents of the entire page afterwards.

<br><br>

## `<button type="submit">`

    <button type="submit">Submit Form</button>

**Screen reader:** "Submit form, button"

<br>

**Example notes:** The screen reader did not indicate that the button was specifically a submit button.

<br><br>

## `<button type="reset">`

    <button type="reset">Reset Form</button>

**Screen reader:** "Reset form, button"

<br>

**Example notes:** The screen reader did not indicate that the button was specifically a reset button.
