# `<output>`

    <form oninput="x.value=parseInt(a.value)+parseInt(b.value)">
        <input type="number" id="a" value="20">
        + <input type="number" id="b" value="25">
        = <output name="x" for="a b"></output>
    </form>

**Screen reader (Firefox - on page load):** "Spin button has auto-complete editable twenty, plus, spin button has auto-complete editable twenty-five, equals."

**Screen reader (Firefox - arrow keys to change the value of an input):** The screen reader announced the new value of the current input followed by the new value of the `<output>` element, albeit with a quirk. For example, if the `<output>` element changed from 48 to 49 it was announced as "nine", if it changed from 49 to 50 it was announced as "fifty", if it changed from 109 to 110 it was announced as "ten", and if it was changed from 199 to 200 it was announced as "two hundred".

**Screen reader (Chrome and Edge - on page load):** "Spin button editable twenty, plus, spin button editable twenty-five, equals."

**Screen reader (Chrome and Edge - arrow keys to change the value of an input):** The screen reader announced the new value of the current input followed by the new value of the `<output>` element, e.g. increasing the first input by one resulted in "twenty-one, forty-six" being announced.

**Screen reader (manually entering new numbers in an input):** The screen reader announced the new value of the `<output>` element, e.g. changing the first input to 25 resulted in "fifty" being announced.

**Screen reader (completely deleting the contents of an input):** "N a n".
