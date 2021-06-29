# ARIA Live Regions

## `aria-live="polite"`

<br><br>

    // HTML
    <p aria-live="polite">My favorite paragraph is <span id="dynamic-paragraph">red</span></p>
    <button type="button" id="timer-button">Click to Start Timer</button>

    <p>I am a static paragraph. I definitely will never, ever get interrupted by any dynamic updates.</p>

    // JavaScript
    const paragraph = document.getElementById("dynamic-paragraph");
    const startButton = document.getElementById("timer-button");

    let counter = 1;
    const colors = ["red", "white", "purple", "blue", "green", "yellow", "brown", "black"]

    function startTimer() {
        const timer = setInterval(() => {
            if (counter >= colors.length) {
                counter = 0
            }

            paragraph.textContent = `${colors[counter++]}`;
        }, 3000);
    }

    startButton.addEventListener("click", startTimer)

**Screen reader (pressing the button to start the timer, then pressing the `down arrow` key to have the screen reader announce the second paragraph):** "I am a static paragraph. I definitely will never, ever get interrupted by any dynamic updates. White. Purple. Blue."

<br>

**Example notes:** By the time the screen reader finished announcing the second paragraph, the dynamic paragraph had been updated three times, changing to "white", then "purple", and finally "blue". Afterwards, the screen reader announced the new contents of the `<span id="dynamic-paragraph">` element each time it was updated every 3 seconds ("green", "yellow", etc.).

<br><br>

## `aria-live="assertive"`

Using the same example in the `aria-live="polite"` section above, the HTML gets changed to:

<br>

    <p >My favorite paragraph is <span role="alert" id="dynamic-paragraph">red</span></p>
    <button type="button" id="update-button">Click to Start Timer</button>

    <p>I am a static paragraph. I definitely will never, ever get interrupted by any dynamic updates.</p>

**Screen reader (pressing the button to start the timer, then pressing the `down arrow` key to have the screen reader announce the second paragraph):** "I am a static paragraph. I def- alert white. I am a static paragraph. Alert purple. I am a static paragraph. Alert blue."

<br>

**Example notes:** The `role="alert"` attribute was used on the dynamic paragraph instead of the `aria-live="assertive"` attribute on the `<p>` element due to the issue with using "assertive" with the NVDA and JAWS screen readers.

If the `role="alert"` attribute was placed on the `<p>` element instead, the entire `<p>` element would get announced, e.g. "alert my favorite color is white."

<br>
<hr>
<br>

## `aria-atomic`

From the `aria-live="polite"` example above, only the contents of the dynamic paragraph was announced by the screen reader. With `aria-atomic="true"`:

<br><br>

    <p aria-live="polite" aria-atomic="true">My favorite paragraph is <span id="dynamic-paragraph">red</span></p>
    <button type="button" id="timer-button">Click to Start Timer</button>

    <p>I am a static paragraph. I definitely will never, ever get interrupted by any dynamic updates.</p>

**Screen reader (pressing the button to start the timer, then pressing the `down arrow` key to have the screen reader announce the second paragraph):** "I am a static paragraph. I definitely will never, ever get interrupted by any dynamic updates. My favorite color is white. My favorite color is purple. My favorite color is blue."

<br><br>

Here's an example using some simple nesting:

    // HTML
    <div aria-live="polite">
        Here is some placeholder text.
        <div>
            Just a little more placeholder.
            <div id="dynamic-content1"></div>
            <div id="dynamic-content2"></div>
        </div>
    </div>
    <button type="button" id="update-button">Click to Update</button>

    // JavaScript
    const content1 = document.getElementById("dynamic-content1");
    const content2 = document.getElementById("dynamic-content2");
    const updater = document.getElementById("update-button");

    function updateContainers() {
        content1.textContent = "And here's some dynamic content."
        content2.textContent = "Just for good measure."
    }

    updater.addEventListener("click", updateContainers)

**Screen reader (pressing the button):** "Just for good measure. And here's some dynamic content."

<br>

**Example notes:** Notice that the screen reader announced the second updated `<div>` first ("Just for good measure"). If the function in the JavaScript file had the `.textContent` lines reversed, the screen reader would announce the updates in the order that the HTML is laid out.

If the top level `<div>` element had the `aria-atomic="true"` attribute, the screen reader would have announced, "Here is some placeholder text. Just a little more placeholder. And here's some dynamic content. Just for good measure." twice, once for each update that occurred within the ARIA live region.

<br>
<hr>
<br>

## Updating Content vs Updating Display

    // HTML
    <div aria-live="polite">
        Here is some placeholder text.
        <div>
            Just a little more placeholder.
            <div id="dynamic-content1">I'm no longer hidden!</div>
        </div>
    </div>
    <button type="button" id="show-button">Click to Show</button>

    // CSS
    #dynamic-content1 {
      display: none;
    }

    // JavaScript
    const content1 = document.getElementById("dynamic-content1");
    const updater = document.getElementById("show-button");

    function updateContainers() {
        content1.style.display = "block";
    }

    updater.addEventListener("click", updateContainers)

**Screen reader (Firefox - pressing the button):** "I'm no longer hidden."

**Screen reader (Chrome and Edge - pressing the button):** "Here is some placeholder text dot. Just a little more placeholder dot. I'm no longer hidden."

<br>

**Example notes:** The result was the same in Firefox when using the `visibility: hidden` property in CSS and updating it to `visibility: visible` in JavaScript. Keep in mind that not every screen reader may announce updates that stem from updating the display or visibility of an element, though.

When the `visibility` property was updated in Chrome and Edge, the screen reader announced either just the updated `<div>` ("I'm no longer hidden"), or everything inside of the top level `<div>` ("Here is some placeholder text...", etc.), depending on whether the `aria-atomic="true"` attribute was added or not.
