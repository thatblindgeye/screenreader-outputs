# Roles, State, and Properties

This section covers ARIA attributes that more relate to the `role` attribute. Other attributes, such as `aria-label` or `aria-live` will have their own section.

Adding a role or an ARIA state or property can help define or change semantic meaning on an element. A `role` attribute can turn a simple `<div>` into a button, an attribute such as `aria-pressed` can notify a screen reader user whether an element is currently toggled or not, and an attribute such as `aria-required` can notify whether an input is required.

Checkout [ARIA roles, state, and properties](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques) and the [list of ARIA roles references](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles) on MDN for lists of the different roles, state, and properties available.

<br>

## Adding a `role`


The `role` attribute can give semantic meaning to an element or change an element's semantics (such as a `<div>` or `<span>`).

Before using the `role` attribute or adding other ARIA attributes, a couple of things should be kept in mind from the [rules of ARIA use](https://www.w3.org/TR/using-aria/#rule1). First, when there is a native HTML element or attribute available, favor using it over giving an element a `role` or using an ARIA attribute. The aforementioned link to ARIA rules goes over some cases when using ARIA is more beneficial over native HTML.

Secondly, caution should be used when adding the `role` attribute to an element. There are [examples of incorrect usage](https://www.w3.org/TR/html-aria/#examples-of-incorrect-usage) when it comes to using the `role` attribute, one being that you should not override an element's default role and semantics. `<button role="checkbox">` would be an incorrect way of using the `role` attribute.

<br>

    <div>I'm just a div</div>
    
**Screen reader:** "I'm just a d i v."

<br>
    
    <div role="button">I'm almost a button!</div>
    
**Screen reader:** "Button, I'm almost a button."

<br>

Like the [WAI-ARIA authoring practices](https://www.w3.org/TR/wai-aria-practices/#read_me_first) mentions, a role is a promise.

Simply adding a `role` to an element won't automatically give it the same functionality of the element that the role promises. Using the example above, clicking the second `<div>` won't cause anything to happen, and a user can't tab to the div. Even adding a `tabindex="0"` wouldn't be enough, as keyboard support would have to be added in via JavaScript (pressing the `space` or `Enter` key to activate the button).

Turning a `<div>` into a button and adding the correct functionality via JavaScript may not be the most difficult thing, but turning a `<div>` into a custom checkbox using ARIA can require a few more extra steps.

    <div id="checkbox-label">Check this checkbox:</div>
    <div id="custom-checkbox" aria-labelledby="checkbox-label" role="checkbox" tabindex="0"></div>
    
**Screen reader (on page load or using the `tab` key to navigate the page and give the checkbox focus:** "Check this checkbox, checkbox not checked."

<br>

## Adding State and Properties

Using the above checkbox example, there is currently nothing that will change the checked state. What the custom checkbox needs is the `aria-checked` attribute, and a little JavaScript.

    // HTML
    <div id="checkbox-label">Check this checkbox:</div>
    <div id="custom-checkbox" aria-labelledby="checkbox-label" role="checkbox" tabindex="0" aria-checked="false"></div>

    // JavaScript
    const checkbox = document.getElementById("custom-checkbox");

    function toggleCheckbox(e) {
      const checked = checkbox.getAttribute("aria-checked") === "false" ? "true" : "false";

      if (e.type === "click" || e.key === " " || e.key === "Enter") {
        checkbox.setAttribute("aria-checked", checked)
      }
    }

    checkbox.addEventListener("click", toggleCheckbox)
    checkbox.addEventListener("keydown", toggleCheckbox)

When clicking the custom checkbox now, the screen reader announced the new checked state each time, e.g. "checked" or "not checked".

Keep in mind that the `<div id="checkbox-label">` element doesn't truly act like a label and would require a bit more JavaScript to add in that functionality (clicking the label counts as clicking the checkbox itself). 

Another thing to keep in mind is that a custom checkbox that uses a `role` and ARIA attributes may not be beneficial inside of a form that gets submitted to a server, as the custom checkbox information may not be submitted like a native checkbox's information would be.

There is also a slightly easier/better way to create a [custom checkbox from W3Schools](https://www.w3schools.com/howto/howto_css_custom_checkbox.asp), which would also solve the above issue when submitting a form to a server, but this example was more meant to show how extra steps need to be taken when using the `role` and other ARIA attributes.


