# Buttons with Icons

## Withou the `alt` Attribute

    <button type="button">
      <img src="//unsplash.it/50" />
    </button>

**Screen reader:** "Button."

<br><br>

## With an Empty String for the `alt` Attribute

    <button type="button">
      <img src="//unsplash.it/50" alt="" />
    </button>

**Screen reader:** "Button."

<br><br>

## With Text for the `alt` Attribute

    <button type="button">
      <img src="//unsplash.it/50" alt="Image button" />
    </button>

**Screen reader:** "Button graphic image button."

<br><br>

## With Text Content

    <button type="button">
      <img src="//unsplash.it/50" />
      Google It
    </button>

**Screen reader:** "Button google it."

<br><br>

## With Text Content and an `<svg>` Element

    <button type="button">
        <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000">
            <path d="M0 0h24v24H0V0z" fill="none"/>
            <path d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"/>
        </svg>
        Add to List
    </button>

**Screen reader:** "Button add to list."

<br><br>

## With Text Content and an Empty String for the `alt` Attribute

    <button type="button">
      <img src="//unsplash.it/50" alt="" />
      Google It
    </button>

**Screen reader:** "Button google it."

<br><br>

## With Text Content and Text for the `alt` Attribute

      <button type="button">
        <img src="//unsplash.it/50" alt="Image button" />
        Google It
      </button>

**Screen reader:** "Button graphic image button google it."

<br><br>

## With Text for the `title` Attribute on the `<button>` Element

    <button title="Google It" type="button">
      <img  src="//unsplash.it/50" />
    </button>

**Screen reader:** "Button google it."

<br><br>

## With Text for the `title` Attribute on the `<img>` Element

    <button type="button">
      <img title="Google It" src="//unsplash.it/50" />
    </button>

**Screen reader:** "Button graphic google it."

<br><br>

## With Text for the `title` Attribute on Both Elements

    <button title="Google It" type="button">
      <img title="Google Now"  src="//unsplash.it/50" />
    </button>

**Screen reader (on page load):** "Button graphic google now."

**Screen reader (`tab` key to give focus to the button):** "Google now button graphic google it."

<br><br>

## With Text for the `title` Attribute on Both Elements and Text for the `alt' Attribute

    <button title="Google It" type="button">
      <img title="Google Now"  src="//unsplash.it/50" alt="Google This" />
    </button>

**Screen reader (on page load):** "Button graphic google this."

**Screen reader (`tab` key to give focus to the button):** "Google this graphic google now button google it."

<br><br>

## With a Material Icon

    <button type="button">
        <span class="material-icons">add</span>
    </button>

**Screen reader:** "Button add."

<br><br>

## With a Material Icon and Text Content

    <button type="button">
        <span class="material-icons">add</span>
        Add to List
    </button>

**Screen reader:** "Button add add to list."

<br>

**Example notes:** The text inside the span that determines the icon to display was read by the screen reader, which can cause duplicate outputs when creating a button with both an icon and text. This can be resolved using ARIA attributes.

<br><br>

## With a Material Icon, Text Content, and Text for the `title` Attribute on the `<button>` Element

    <button title="Add this to a new list" type="button">
        <span class="material-icons">add</span>
        Add to List
    </button>

**Screen reader (on page load):** "Button add add to list."

**Screen reader (`tab` key to give focus to the button):** "Add add to list button add this to a new list."
