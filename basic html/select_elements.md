# `<select>`

## Simple `<select>` Element

    <label>Choose a color:
      <select name="color">
          <option value="">--Select an option--</option>
          <option value="red">Red</option>
          <option value="green">Green</option>
          <option value="blue">Blue</option>
      </select>
    </label

**Screen reader (Firefox - on page load):** "Clickable choose a color, combo box collapsed select an option."

**Screen reader (Firefox - `space` key to open the select box):** "Combo box expanded, select an option list."

**Screen reader (Chrome and Edge - on page load):** "Choose a color, combo box collapsed select an option."

**Screen reader (Chrome and Edge - `space` key to open the select box):** "Expanded list, select an option one of four."

<br>

**Example notes:** When navigating between the different options, the screen reader announced the name of the option followed by its number in the list, e.g. "red two of four".

When an option has the `disabled` attribute added to it, the screen reader still counted it in the total number of options even though it could not be selected or tabbed to.

<br><br>

## With `<optgroup>` Elements

    <label>Choose your favorite dessert:
        <select>
            <optgroup label="Ice Cream">
                <option>Chocolate</option>
                <option>Vanilla</option>
                <option>Strawberry</option>
            </optgroup>
            <optgroup label="Pie">
                <option>Pumpkin</option>
                <option>Apple</option>
            </optgroup>
        </select>
    </label>

**Screen reader (Firefox - on page load):** "Clickable choose your favorite dessert, combo box collapsed chocolate."

**Screen reader (Firefox - `space` key to open the select box):** "Combo box expanded, chocolate list, ice cream grouping, chocolate one of three level two."

**Screen reader (Chrome and Edge - on page load):** "Choose your favorite dessert, combo box collapsed chocolate."

**Screen reader (Chrome and Edge - `space` key to open the select box):** "Expanded list, chocolate one of five."

<br>

**Example notes:** Only in Firefox did the screen reader indicate when tabbing between the different `<optgroup` elements of the input.

<br><br>

## With the `multiple` Attribute

    <label>Choose your favorite pet:
        <select multiple>
            <option>Dog</option>
            <option>Cat</option>
            <option>Hamster</option>
            <option>Bird</option>
        </select>
    </label>

**Screen reader (Firefox - on page load):** "Clickable choose your favorite pet, list clickable dog."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Choose your favorite pet, list, dog one of four."

**Screen reader (Chrome and Edge - on page load):** "Choose your favorite pet, list clickable dog."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Choose your favorite pet, list."

<br>

**Example notes:** The screen reader did not indicate that multiple items were selected when tabbing back into the input.
