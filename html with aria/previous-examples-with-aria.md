# Previous Examples with ARIA

<br><br>

## Buttons with icons

    <button type="button">
        <span class="material-icons" aria-hidden="true">add</span>
        Add to List
    </button>
    
**Screen reader:** "Button add to list."

**Examples notes:** In a [previous example of buttons with icons](https://github.com/thatblindgeye/screenreader-outputs/blob/main/nested%20html%20tags/buttons-with-icons.md), the screen reader announced duplicate text due to the text content of the `span` tag and the text content of the `button` tag. Using the `aria-hidden` attribute, the text content of the `span` tag should be hidden from the accessibility tree, but allow the icon to visually remain.
