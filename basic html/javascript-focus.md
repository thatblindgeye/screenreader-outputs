# JavaScript's `focus()` Method

If you aren't already familiar with it, the `focus()` method in JavaScript allows you to set focus on a specified element. Maybe clicking a button will set focus on an input field, for example. But how would that translate to the screen reader output?

    // HTML
    <label>
        Enter your name:
        <input id="input" type="text">
    </label>

    <button id="button" type="button">Click to give the input focus</button>
    
    // JavaScript
    const input = document.getElementById("input");
    const button = document.getElementById("button");

    function focusInput() {
        input.focus()
    }

    button.addEventListener("click", focusInput)
    
**Screen reader (Firefox - `space` or `Enter` key to click the button):** "Enter your name, edit, has auto-complete blank."

**Screen reader (Chrome and Edge - `space` or `Enter` key to click the button):** "Enter your name, edit blank."

<br>

It translates pretty well, at least with the NVDA screen reader. What about an input that is visually hidden, but becomes visible after some sort of user interaction? We'll use the same code from above, but with the following changes:

    // CSS
    #input {
      display: none;
    }
    
    // JavaScript
    function focusInput() {
        input.style.display = "inline";
        input.focus()
    }

**Screen reader (Firefox - `space` or `Enter` key to click the button):** "Enter your name, edit, has auto-complete blank."

**Screen reader (Chrome and Edge - `space` or `Enter` key to click the button):** "Enter your name, edit blank."

<br>

Same result! Well, what about an input that is created and appended dynamically with JavaScript instead?

    // HTML
    <div id="container"></div>
    <button id="button" type="button">Click to give the input focus</button>
    
    // JavaScript
    const button = document.getElementById("button");
    const container = document.getElementById("container")

    function createInput() {
        const label = document.createElement("label");
        label.textContent = "Enter your name:";

        const input = document.createElement("input");
        input.setAttribute("type", "text");
        input.setAttribute("id", "input");

        label.appendChild(input)
        container.append(label);
    }

    button.addEventListener("click", () => {
        createInput();
        document.getElementById("input").focus();
    })

**Screen reader (Firefox - `space` or `Enter` key to click the button):** "Enter your name, edit, has auto-complete blank."

**Screen reader (Chrome and Edge - `space` or `Enter` key to click the button):** "Enter your name, edit blank."

<br>

The same result once again. And it's not just input elements. If an `<a>` element were to have the focus set on it from JavaScript, it would be announced by the screen reader as well, as should any element that can receive focus. To test this out a little further:

    // HTML
    <div id="container">Just some text</div>
    <button id="button" type="button">Click to give the div focus</button>

    // JavaScript
    const button = document.getElementById("button");
    const container = document.getElementById("container")

    function setFocus() {
        container.focus()
    }

    button.addEventListener("click", setFocus);
    
**Example notes:** The screen reader did not announce anything upon clicking the button, because the `<div>` element cannot receive focus... yet.

<br>

    // HTML
    <div tabindex="0" id="container">Just some text</div>
    <button id="button" type="button">Click to give the div focus</button>
    
**Screen reader (`space` or `Enter` key to click the button):** "Just some text."

<br>

Now that the `<div>` element has the `tabindex="0"` attribute, it can receive focus and the screen reader announces the text contents.



