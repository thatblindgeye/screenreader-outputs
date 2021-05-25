# Multi-Input Form

    <form>
        <fieldset>
            <legend>First Section</legend>
            <label>
                Name:
                <input type="text">
            </label>
            <label>
                City:
                <input type="text">
            </label>
        </fieldset>
        <fieldset>
            <legend>Second Section</legend>
            <label>
                Would you like to check this checkbox?
                <input type="checkbox">
            </label>
            <p>Select your favorite color:</p>
            <input type="radio" id="red" name="color" value="red">
            <label for="red">Red</label><br>
            <input type="radio" id="blue" name="color" value="blue">
            <label for="blue">Blue</label><br>
            <input type="radio" id="other" name="color" value="other">
            <label for="other">Other</label> 
        </fieldset>
    </form>

**Screen reader (Firefox - on page load):** "Grouping first section. Clickable name, edit has auto-complete, clickable city, edit has auto-complete. Out of grouping." and "Grouping second section. Clickable would you like to check this checkbox, checkbox not checked. Select your favorite color, radio button not checked red, radio button not checked blue, radio button not checked other clickable."

**Screen reader (Edge and Chrome - on page load):** "Grouping first section. Name edit, city edit. Out of grouping." and "Grouping second section. Checkbox not checked would you like to check this checkbox. Select your favorite color, radio button not checked red, radio button not checked blue, radio button not checked other."

**Example notes:** When tabbing between input fields, the screen reader annoucned the name of each fieldset upone entering it, e.g. "Second section grouping".
