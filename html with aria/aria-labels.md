# ARIA Labels

## `aria-label`

### `<div>` Element with Text Content

    <div>This is a div container.</div>

    <div aria-label="Label for the div container">This is a div container.</div>

**Screen reader:** "This is a d i v container."

<br>

**Example notes:** Notice how the screen reader did not announce the `aria-label`, but the native text content.

<br><br>

### `<div>` Element with Text Content and the `role` Attribute

    <div role="button" aria-label="Label for the button" tabindex="0">A div acting as a button</div>

**Screen reader:** "Button label for the button."

<br>

**Example notes:** Unlike the example above, the screen reader now announced the `aria-label`, due to the `role` attribute being added.

<br><br>

### Landmark Element with Text Content

    <main aria-label="Label for the main container">This is a main container.</main>

**Screen reader:** "Label for the main container, main landmark, this is a main container."

<br><br>

### `<a>` Element with Text Content

    <a href="https://www.google.com/" aria-label="Google (opens in a new window)">Go To Google</a>

**Screen reader:** "Link, google. Opens in a new window." or "Visited link, google. Opens in a new window."

<br><br>

### `<button>` Element with Text Content

    <button type="button" aria-label="Close">X</button>

**Screen reader:** "Button close."

<br><br>

### Input with a Native `<label>` Element

    <label>
      Name:
      <input type="text" aria-label="Enter a name" />
    </label>

**Screen reader (Firefox - on page load):** "Clickable name edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Enter a name edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Name, enter a name edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Enter a name edit blank."

<br><br>

### Unordered List

    <ul aria-label="shopping list">
        <li>Butter</li>
        <li>Milk</li>
        <li>Eggs</li>
    </ul>

**Screen reader:** "Shopping list, list with three items, bullet butter, bullet milk, bullet eggs."

<br>

**Examples notes:** The text "list" was repeated because the screen reader read first the `aria-label`, followed by the role of the `<ul>` element.

Though the screen reader did announce the `aria-label`, it may be worth following the recommendation at the top of the page for when to use the `aria-label` attribute.

The screen reader announced "bullet" before each list item due to the CSS for the testing page not having a rule to remove the list-style-type. When the list-style-type is set to none, the screen reader did not announce "bullet". This applies to the below example as well.

<br><br>

### Landmark Element with an Unordered List

    <nav aria-label="main navigation">
        <ul>
            <li>Home</li>
            <li>About</li>
            <li>Contact</li>
        </ul>
    </nav>

**Screen reader:** "Main navigation, navigation landmark, list with three items, bullet home, bullet about, bullet contact."

<br>

**Examples notes:** The text "navigation" was repeated because the screen reader read first the `aria-label`, followed by stating the type of landmark.

<br>
<hr>
<br>

## `aria-labelledby`

<br><br>

### Single Label on Multiple Inputs

    <div id="myBillingId">Billing</div>
    <div>
      <div id="myNameId">Name</div>
      <input type="text" aria-labelledby="myBillingId myNameId"/>
    </div>
    <div>
      <div id="myAddressId">Address</div>
      <input type="text" aria-labelledby="myBillingId myAddressId"/>
    </div>

**Screen reader (Firefox - `tab` key to give focus to the inputs):** "Billing name edit has auto-complete blank." and "Billing address edit has auto-complete blank."

**Screen reader (Chrome and Edge - `tab` key to give focus to the inputs):** "Billing name edit blank." and "Billing address edit blank."

<br>

**Example notes:** This example was taken from the MDN page on [Using the aria-labelledby attribute](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-labelledby_attribute).

<br><br>

### Single Label on a Single Input

    <p>Please select the <span id="mysldr-lbl">number of days for your trip</span></p>
    <input type="range" id="mysldr" aria-labelledby="mysldr-lbl"></div>

**Screen reader (`tab` key to give focus to the input):** "Number of days for your trip slider 50."

<br>

**Example notes:** This example was taken from the W3 page on [Using aria-labelledby to provide a name for user interface controls](https://www.w3.org/WAI/WCAG21/Techniques/aria/ARIA16).

<br><br>

### Multiple Labels on a Single Input

    <label id="l1" for="f3">Notify me</label>
    <select name="amt" id="f3" aria-labelledby="l1 f3 l2">
      <option value="1">1</option>
      <option value="2">2</option>
    </select>
    <span id="l2" tabindex="-1">days in advance</span>

**Screen reader (Firefox - on page load):** "Clickable notify me combo box collapsed one days in advance."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Notify me one days in advance combo box one collapsed."

**Screen reader (Chrome and Edge - on page load):** "Notify me combo box collapsed one days in advance."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Notify me days in advance combo box one collapsed."

<br>

**Example notes:** This example was taken from the W3 page on [Using aria-labelledby to provide a name for user interface controls](https://www.w3.org/WAI/WCAG21/Techniques/aria/ARIA16).

<br><br>

### Removing the Label from the Accessibility Tree

    <span id="button-label" aria-hidden="true">Labelled by label</span>
    <button type="button" aria-labelledby="button-label">Native label</button>

**Screen reader:** "Button labelled by label."

<br>

**Example notes:** The text content of the `<span>` element is only announced due to the `aria-labelledby` attribute on the `<button>` element. The `aria-hidden` attribute removes the `<span>` element from the accessibility tree, which means it won't be announced by screen readers on its own.

<br>
<hr>
<br>

## `aria-describedby`

<br><br>

    <label>
        Password:
        <input type="password" aria-describedby="password-reqs" />
    </label>
    <span id="password-reqs">Your password must contain:
      <ul>
        <li>At least one capital letter</li>
        <li>At least one number</li>
        <li>At least one special character</li>
      </ul>
    </span>

**Screen reader (Firefox - on page load):** "Clickable password. Edit protected your password must contain, list with three items bullet, at least one capital letter, bullet at least one number, bullet at least one special character."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Password. Edit protected your password must contain, bullet at least one capital letter, bullet at least one number, bullet at least one special character, blank."

**Screen reader (Chrome and Edge - on page load):** "Password. Edit protected your password must contain, list with three items bullet, at least one capital letter, bullet at least one number, bullet at least one special character."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Password. Edit protected your password must contain, at least one capital letter, at least one number, at least one special character, blank."

<br>
<hr>
<br>

## `aria-label` vs `aria-labelledby` vs `aria-describedby`

### Without `aria-hidden` Attribute

    <span id="labelled">ARIA labelled by label</span>
    <button type="button" aria-label="An ARIA label" aria-labelledby="labelled" aria-describedby="described">Native label</button>
    <span id="described">ARIA described by description</span>

**Screen reader (on page load):** "ARIA labelled by label, button, ARIA labelled by label ARIA described by description."

**Screen reader (`tab` key to focus to the button):** "ARIA labelled by label, button, ARIA described by description."

<br><br>

### With `aria-hidden` Attribute

    <span id="labelled" aria-hidden="true">ARIA labelled by label</span>
    <button type="button" aria-label="An ARIA label" aria-labelledby="labelled" aria-describedby="described">Native label</button>
    <span id="described" aria-hidden="true">ARIA described by description</span>

**Screen reader (on page load):** "Button ARIA labelled by label."

**Screen reader (`tab` key to focus to the button):** "ARIA labelled by label button ARIA described by description."

<br><br>

## `aria-label` vs `aria-labelledby` vs `aria-describedby` vs `<label>`

    <span id="labelled">ARIA labelled by label</span>
    <label for='input'>Native label:</label>
    <input type="text" id="input" aria-label="An ARIA label" aria-labelledby="labelled" aria-describedby="described">
    <span id="described">ARIA described by description</span>

**Screen reader (Firefox- on page load):** "ARIA labelled by label clickable native label. Edit has auto-complete ARIA described by description."

**Screen reader (Firefox- `tab` key to focus to the input):** "ARIA labelled by label edit has auto-complete ARIA described by description blank."

**Screen reader (Chrome and Edge- on page load):** "ARIA labelled by label native label. Edit ARIA described by description."

**Screen reader (Chrome and Edge- `tab` key to focus to the input):** "ARIA labelled by label edit ARIA described by description blank."
