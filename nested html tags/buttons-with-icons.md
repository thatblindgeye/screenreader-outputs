# Buttons with icons

<br><br>

    <button type="button">
      <img src="//unsplash.it/50" />
    </button>
    
    <button type="button">
      <img src="//unsplash.it/50" alt="" />
    </button>
    
**Screen reader:** "Button."

<br><br>
    
    <button type="button">
      <img src="//unsplash.it/50" alt="Image button" />
    </button>
    
**Screen reader:** "Button graphic image button."

<br><br>

    <button type="button">
      <img src="//unsplash.it/50" />
      Google It
    </button>
    
    <button type="button">
      <img src="//unsplash.it/50" alt="" />
      Google It
    </button>
      
    <button title="Google It" type="button">
      <img  src="//unsplash.it/50" />
    </button>
    
**Screen reader:** "Button google it."

<br><br>
    
      <button type="button">
        <img src="//unsplash.it/50" alt="Image button" />
        Google It
      </button>
    
**Screen reader:** "Button graphic image button google it."

<br><br>

    <button type="button">
      <img title="Google It" src="//unsplash.it/50" />
    </button>
    
**Screen reader:** "Button graphic google it."

<br><br>

    <button title="Google It" type="button">
      <img title="Google Now"  src="//unsplash.it/50" />
    </button>

**Screen reader (on page load):** "Button graphic google now."

**Screen reader (using the `tab` key to navigate the page):** "Google now button graphic google it."

<br><br>

    <button title="Google It" type="button">
      <img title="Google Now"  src="//unsplash.it/50" alt="Google This" />
    </button>

**Screen reader (on page load):** "Button graphic google this."

**Screen reader (using the `tab` key to navigate the page):** "Google this graphic google now button google it."

<br><br>

    <button type="button">
        <span class="material-icons-outlined">add</span>
    </button>

**Screen reader:** "Button add."

<br><br>

    <button type="button">
        <span class="material-icons-outlined">add</span>
        Add to List
    </button>

**Screen reader:** "Button add add to list."

**Example notes:** The text inside the span that determines the icon to display was read by the screen reader, which can cause duplicate outputs when creating a button with both an icon and text. This can be resolved using ARIA attributes.

<br><br>

    <button title="Add this to a new list" type="button">
        <span class="material-icons-outlined">add</span>
        Add to List
    </button>

**Screen reader (on page load):** "Button add add to list."

**Screen reader (using the `tab` key to navigate the page):** "Add add to list button add this to a new list."

<br><br>
    
    // using svg tags for the add button from Google icons
    <button type="button">
        <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000">
            <path d="M0 0h24v24H0V0z" fill="none"/>
            <path d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"/>
        </svg>
        Add to List
    </button>

**Screen reader:** "Button add to list."

