## `aria-label`

The `aria-label` attribute simply labels an element with the specified string when there is no visible label on the page. This can override any native labeling on the element.

Per [Using the aria-label attribute](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute), the `aria-label` attribute should only be used on interactive elements (buttons, checkboxes, etc.), landmark elements (main, nav, etc.), elements with an explicit widget role, and `iframe` or `img` elements.

According to [https://dequeuniversity.com/assets/html/jquery-summit/html5/slides/landmarks.html](https://dequeuniversity.com/assets/html/jquery-summit/html5/slides/landmarks.html), the `<article>` and `<region>` elements are not considered ARIA landmarks and will be unaffected by the `aria-label` attribute.

<br><br>

    <div>This is a div container.</div>
    
    <div aria-label="Label for the div container">This is a div container.</div>

**Screen reader:** "This is a d i v container."

<br>

    <div role="button" aria-label="Label for the button" tabindex="0">A div acting as a button</div>

**Screen reader:** "Button label for the button."

<br>

    <main aria-label="Label for the main container">This is a main container.</main>

**Screen reader:** "Label for the main container main landmark this is a main container."

<br>

    <a href="https://www.google.com/" aria-label="Google (opens in a new window)">Google</a>

**Screen reader:** "Link google. Opens in a new window." or "Visited link google. Opens in a new window."

<br>

    <button type="button" aria-label="Close">X</button>

**Screen reader:** "Button close."

<br>

    <label>
      Name:
      <input type="text" aria-label="Enter a name" />
    </label>

**Screen reader (Firefox - on page load):** "Clickable name edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page and give inputs focus):** "Enter a name edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Name, enter a name edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page and give inputs focus):** "Enter a name edit blank."


<br><br>

## `aria-labelledby`

The `aria-labelledby` attribute is similar to the `aria-label` attribute, except it requires creating a relationship between elements by using ID's. Think of `aria-labelledby` as though it were the `<label>` tag linking itself with a form input with the `for` attribute.

This attribute should be used to convey essential information to the user. It also overrides all other labels for an element, including `aria-label` and the native `<label>` tag.
    
    <div id="myBillingId">Billing</div>
    <div>
      <div id="myNameId">Name</div>
      <input type="text" aria-labelledby="myBillingId myNameId"/>
    </div>
    <div>
      <div id="myAddressId">Address</div>
      <input type="text" aria-labelledby="myBillingId myAddressId"/>
    </div>

**Screen reader (Firefox - using the `tab` key to navigate the page and give inputs focus):** "Billing name edit has auto-complete blank." and "Billing address edit has auto-complete blank."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page and give inputs focus):** "Billing name edit blank." and "Billing address edit blank."

**Example notes:** This example was taken from the MDN page on [Using the aria-labelledby attribute](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-labelledby_attribute).

<br>

    <p>Please select the <span id="mysldr-lbl">number of days for your trip</span></p>
    <input type="range" id="mysldr" aria-labelledby="mysldr-lbl"></div>

**Screen reader (using the `tab` key to navigate the page and give inputs focus):** "Number of days for your trip slider 50."

**Example notes:** This example was taken from the W3 page on [Using aria-labelledby to provide a name for user interface controls](https://www.w3.org/WAI/WCAG21/Techniques/aria/ARIA16).

<br>

    <label id="l1" for="f3">Notify me</label>
    <select name="amt" id="f3" aria-labelledby="l1 f3 l2">
      <option value="1">1</option>
      <option value="2">2</option>
    </select>
    <span id="l2" tabindex="-1">days in advance</span>
    
**Screen reader (Firefox - on page load):** "Clickable notify me combo box collapsed one days in advance."

**Screen reader (Firefox - using the `tab` key to navigate the page and give inputs focus):** "Notify me one days in advance combo box one collapsed."

**Screen reader (Chrome and Edge - on page load):** "Notify me combo box collapsed one days in advance."
    
**Screen reader (Chrome and Edge - using the `tab` key to navigate the page and give inputs focus):** "Notify me days in advance combo box one collapsed."

**Example notes:** This example was taken from the W3 page on [Using aria-labelledby to provide a name for user interface controls](https://www.w3.org/WAI/WCAG21/Techniques/aria/ARIA16).

<br><br>

## `aria-describedby`

The `aria-describedby` attribute works similarly to the `aria-labelledby` attribute by creating a relationship between elements using ID's. Unlike `aria-labelledby`, hwoever, `aria-describedby` conveys additional information that might help a user.

    <span id="password-reqs">Your password must contain:
      <ul>
        <li>At least one capital letter</li>
        <li>At least one number</li>
        <li>At least one special character</li>
      </ul>
    </span>

**Screen reader (Firefox - on page load):** "Clickable password. Edit has auto-complete your password must contain, list with three items bullet, at least one capital letter, bullet at least one number, bullet at least one special character."

**Screen reader (Firefox - using the `tab` key to navigate the page and give inputs focus):** "Password. Edit has auto-complete your password must contain, bullet at least one capital letter, bullet at least one number, bullet at least one special character, blank."

**Screen reader (Chrome and Edge - on page load):** "Password. Edit your password must contain, list with three items bullet, at least one capital letter, bullet at least one number, bullet at least one special character."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page and give inputs focus):** "Password. Edit your password must contain, at least one capital letter, at least one number, at least one special character, blank."

<br><br>

## `aria-label` vs `aria-labelledby` vs `aria-describedby` vs `<label>`

    <span id="labelled">ARIA labelled by label</span>
    <button type="button" aria-label="An ARIA label" aria-labelledby="labelled" aria-describedby="described">Native label</button>
    <span id="described">ARIA described by description</span>

**Screen reader (on page load):** "ARIA labelled by label button ARIA labelled by label ARIA described by description."

**Screen reader (using the `tab` key to navigate the page and give button focus):** "ARIA labelled by label button ARIA described by description."

<br>

    <span id="labelled" aria-hidden="true">ARIA labelled by label</span>
    <button type="button" aria-label="An ARIA label" aria-labelledby="labelled" aria-describedby="described">Native label</button>
    <span id="described" aria-hidden="true">ARIA described by description</span>

**Screen reader (on page load):** "Button ARIA labelled by label."

**Screen reader (using the `tab` key to navigate the page and give button focus):** "ARIA labelled by label button ARIA described by description."

<br>

    <span id="labelled">ARIA labelled by label</span>
    <label for='input'>Native label:</label>
    <input type="text" id="input" aria-label="An ARIA label" aria-labelledby="labelled" aria-describedby="described">
    <span id="described">ARIA described by description</span>

**Screen reader (Firefox- on page load):** "ARIA labelled by label clickable native label. Edit has auto-complete ARIA described by description."

**Screen reader (Firefox- using the `tab` key to navigate the page and give input focus):** "ARIA labelled by label edit has auto-complete ARIA described by description blank."

**Screen reader (Chrome and Edge- on page load):** "ARIA labelled by label native label. Edit ARIA described by description."

**Screen reader (Chrome and Edge- using the `tab` key to navigate the page and give input focus):** "ARIA labelled by label edit ARIA described by description blank."


