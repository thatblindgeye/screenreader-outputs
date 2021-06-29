# Roles, States, and Properties

## `role`

    <div>I'm just a div</div>

**Screen reader:** "I'm just a d i v."

<br><br>

    <div role="button">I'm almost a button!</div>

**Screen reader:** "Button, I'm almost a button."

<br>

**Example notes:** Adding a `role` attribute doesn't add the functionality of the role being added. In this case, the `<div>` is not focusable and doesn't have any keyboard event handling (pressing the space or Enter key to "click" the button).

<br><br>

    <div id="checkbox-label">Check this checkbox:</div>
    <div id="custom-checkbox" aria-labelledby="checkbox-label" role="checkbox" tabindex="0"></div>

**Screen reader (on page load or using the `tab` key to navigate the page and give the checkbox focus:** "Check this checkbox, checkbox not checked."

<br>

**Example notes:** Clicking on the checkbox won't cause the checkbox to become checked, as this functionality would need to be added in JavaScript. Similar to the custom button example above, the custom checkbox also isn't focusable and doesn't have keyboard event hanndling.

<br>
<hr>
<br>

## Adding State and Properties

Using the checkbox example above, there is currently nothing that will change the checked state. What the custom checkbox needs is the `aria-checked` attribute, and a little JavaScript.

<br><br>

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

<br>

When clicking the custom checkbox now, the screen reader announced the new checked state each time, e.g. "checked" or "not checked".
