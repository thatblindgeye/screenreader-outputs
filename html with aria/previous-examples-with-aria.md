# Previous Examples with ARIA

This section revisits various examples from other sections in this repo, adding ARIA attributes to show how the previous examples can be made more accessible or to simply change what a screen reader announces.

<br><br>

## `audio`

    // with the aria-label attribute
    <audio src="./assets/sound_sample.wav" aria-label="sound sample" controls></audio>

    // with a span that has the aria-hidden attribute
    <span id="media-label" aria-hidden="true">Sound Sample</span>
    <audio src="./assets/sound_sample.wav" aria-labelledby="media-label" controls></audio>

**Screen reader (Firefox - on page load):** "Sound sample grouping button play. Loading 100 percent. Position slider midnight slash three-fourteen. Button mute. Volume slider 100 out of grouping."

**Screen reader (Firefox - `tab` key to give focus to the media control):** "Sound sample grouping play button. Loading 100 percent. Midnight slash three-fourteen position slider. Mute button. 100."

**Screen reader (Chrome and Edge - on page load):** "Sound sample grouping button play. Midnight slash three-thirteen. Audio time scrubber midnight slash three-thirteen slider elapsed time. Midnight. Button mute. Button show more media controls."

**Screen reader (Chrome and Edge - `tab` key to give focus to the media control):** "Sound sample grouping play button. Midnight slash three-fourteen elapsed time. Midnight audio time scrubber midnight slash three-fourteen slider mute button show more media controls."

<br><br>

## `video`

    // with the aria-label attribute
    <video src="./assets/video_sample.mp4" aria-label="video sample" controls></video>

    // with a span that has the aria-hidden attribute
    <span id="media-label" aria-hidden="true">Video Sample</span>
    <video src="./assets/video_sample.mp4" aria-labelledby="media-label" controls></video>

**Screen reader (Firefox - on page load):** "Video sample grouping button. Button play. Loading 100 percent. Position slider midnight slash zero twenty-three. Button mute. Volume slider 100. Button full screen."

**Screen reader (Firefox - `tab` key give focus to the media control):** "Video sample grouping button play button. Loading 100 percent. Midnight slash zero twenty-three position slider mute button 100 volume slider full screen."

**Screen reader (Chrome and Edge - on page load):** "Video sample grouping buffering. Button play. Midnight slash zero twenty-two. Button mute. Button enter full screen. Button show more media controls. Video time scrubber midnight slash zero twenty-two slider elapsed time. Midnight."

**Screen reader (Chrome and Edge - `tab` key to give focus to the media control):** "Video sample grouping play button midnight slash zero twenty-two mute button enter full screen button show more media controls button more options elapsed time, midnight video time scrubber midnight slash zero twenty-two slider."

<br>

**Notes:** In a [previous example of the `video` tag](https://github.com/thatblindgeye/screenreader-outputs/blob/main/basic%20html%20tags/video_tags.md) and a [previous example of the `audio` tag](https://github.com/thatblindgeye/screenreader-outputs/blob/main/basic%20html%20tags/audio_tags.md), the screen reader did not give any indication of what the media being played was. Using the `aria-labelledby` attribute may aid in context to the media that is tied to the media player.

Adding the `aria-hidden="true"` attribute prevented the screen reader from duplicating output of the text and from announcing the text when navigating the page using the arrow keys.

Wrapping the media tag inside of a `label` tag did not provide exactly the same output as above. When using the `tab` key to navigate the page and give the media controls focus, the screen reader did not announce the label text as it did in the example above.

Slightly less related to screen reader accessibility, but the MDN page on [Accessible multimedia](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/Multimedia) shows how you can create a custom media player as well as how to implement audio transcripts and video text tracks (another great way to offer accessibility).

<br>
<hr>
<br>

## `<buttone>`

### With the `aria-disabled` Attribute

    <button type="button" aria-disabled="true">ARIA</button>

**Screen reader:** "ARIA, button, unvailable."

<br>

**Example notes:** In a [previous example of the `button` tag](https://github.com/thatblindgeye/screenreader-outputs/blob/main/basic%20html%20tags/button_tags.md), when a button had the `disabled` attribute, the screen reader recognized the button when using the dedicated key for navigating between buttons on the page, when using the `up arrow` or `down arrow` keys, and when the page initially loaded, but ignored the button when using the `tab` key to navigate the page. Keep in mind these results are only with the NVDA screen reader; other screen readers may behave differently.

Using the `aria-disabled` attribute still makes the button focusable and recognized by the screen reader when tabbing in addition to the ways a button with the `disabled` attribute is focusable/recognized.

Using an example from the [a11y-101 page on aria-disabled](https://a11y-101.com/development/aria-disabled) (specifically the "Combining aria-disabled and aria-live" section), a case for using `aria-disabled` could be when you have a button that is disabled until a user checks some sort of "agree to terms of service" checkbox. Keep in mind that using `aria-disabled` would require extra JavaScript to properly disable the button.

<br>
<hr>
<br>

## `<button>`

### With a Material Icon and the `aria-hidden` attribute

    <button type="button">
        <span class="material-icons" aria-hidden="true">add</span>
        Add to List
    </button>

**Screen reader:** "Button add to list."

<br>

**Examples notes:** In a [previous example of buttons with icons](https://github.com/thatblindgeye/screenreader-outputs/blob/main/nested%20html%20tags/buttons-with-icons.md), the screen reader announced duplicate text due to the text content of the `span` tag and the text content of the `button` tag. Using the `aria-hidden` attribute, the text content of the `span` tag should be hidden from the accessibility tree, but allow the icon to visually remain.

<br><br>

### With the `aria-label` Attribute

    <button type="button" aria-label="Add New">
        <span class="material-icons">add</span>
    </button>

**Screen reader:** "Button add new."

<br>
<hr>
<br>

## Input with the `aria-required` Attribute

    <form>
        <label>
            Name:
            <input type="text" aria-required="true" />
        </label>
        <input type="submit" />
    </form>

**Screen reader (Firefox - `tab` key to give focus to the input):** "Name, edit required has auto-complete, blank."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Name, edit required, blank."

<br>

**Example notes:** In a [previous example of the `<input>` tag](https://github.com/thatblindgeye/screenreader-outputs/blob/main/basic%20html%20tags/input_tags.md), the screen reader also announced "invalid entry" for text inputs that had the `required` attribute.

Another difference is when the form is submitted. Using the `required` attribute, when attempting to submit the form with the input blank, the browser may have a default popup appear stating, "please fill out this field" (or something similar), and the form is prevented from being submitted. Using `aria-required`, there is no such pop-up and the form is not prevented from being submitted (this can also be achieved by giving the form tag the `novalidate` attribute when using the native `required` attribute on inputs).

If you are doing your own form validation rather than relying on browser validation then this may not be an issue, and using `aria-required` (or giving a form the `novalidate` attribute) may be beneficial to making your form more uniform across different browsers.

<br>
<hr>
<br>

## Multi-Input Form with the `aria-labelledby` Attribute

    <form aria-label="A sample form">
        <fieldset>
            <legend id="section-one">First Section</legend>
            <label id="name-label">
                Name:
                <input type="text" aria-labelledby="section-one name-label">
            </label>
            <label id="city-label">
                City:
                <input type="text" aria-labelledby="section-one city-label">
            </label>
        </fieldset>
        <fieldset>
            <legend id="section-two">Second Section</legend>
            <label id="checkbox-label">
                Would you like to check this checkbox?
                <input type="checkbox" aria-labelledby="section-two checkbox-label">
            </label>
            <p id="color-label">Select your favorite color:</p>
            <input type="radio" id="red" name="color" value="red" aria-labelledby="section-two color-label red-label">
            <label for="red" id="red-label">Red</label><br>
            <input type="radio" id="blue" name="color" value="blue" aria-labelledby="section-two color-label blue-label">
            <label for="blue" id="blue-label">Blue</label><br>
            <input type="radio" id="other" name="color" value="other" aria-labelledby="section-two color-label other-label">
            <label for="other" id="other-label">Other</label>
        </fieldset>
    </form>

**Screen reader (Firefox - `tab` key to give focus to the inputs):** "A sample form form landmark. First section grouping. First section name, edit has auto-complete blank.", "First section city, edit has auto-complete blank.", "Second section grouping. Clickable second section would you like to check this checkbox. Checkbox not checked.", "Second section select your favorite color, red, radio button not checked one of three.", "Second section select your favorite color, blue, radio button not checked two of three.", and "Second section select your favorite color, other, radio button not checked three of three.".

**Screen reader (Edge and Chrome - `tab` key to give focus to the inputs):** "A sample form form. First section grouping. First section name, edit blank.", "First section city, edit blank.", "Second section grouping. Second section would you like to check this checkbox. Checkbox not checked.", "Second section select your favorite color, red, radio button not checked one of three.", "Second section select your favorite color, blue, radio button not checked two of three.", and "Second section select your favorite color, other, radio button not checked three of three.".

<br>

**Example notes:** You may not need so many `aria-labelledby` labels on radio inputs, but this example was meant to show what can be done with ARIA labels.

<br>
<hr>
<br>

## `<svg>`

### With the `role` Attribute

    <svg width="100" height="100" role="img">
        <title>I'm a circle.</title>
        <desc>A red circle.</desc>
        <circle cx="50" cy="50" r="40" fill="red" />
    </svg>

**Screen reader (on page load):** "Graphic, I'm a circle."

**Screen reader (Firefox - shortcut key to navigate between graphics):** "I'm a circle, graphic, a red circle."

**Screen reader (Chrome and Edge - shortcut key to navigate between graphics):** "I'm a circle, graphic."

<br><br>

### With the `aria-labelledby` Attribute

    <svg width="100" height="100" aria-labelledby="svg-title svg-desc">
        <title id="svg-title">I'm another circle.</title>
        <desc id="svg-desc">Another red circle.</desc>
        <circle cx="50" cy="50" r="40" fill="red" />
    </svg>

**Screen reader (Chrome and Edge - on page load or shortcut key to navigate between graphics):** "Graphic, I'm another circle, another red circle."

**Notes:** "The screen reader did not announce the presence of the `<svg>` in Firefox."

<br><br>

### With the `role` and `aria-labelledby` Attributes

    <svg width="100" height="100" role="img" aria-labelledby="svg-title2 svg-desc2">
        <title id="svg-title2">I'm yet another circle.</title>
        <desc id="svg-desc2">Yet another red circle.</desc>
        <circle cx="50" cy="50" r="40" fill="red" />
    </svg>

**Screen reader (on page load):** "Graphic, I'm yet another circle, yet another red circle."

**Screen reader (Firefox - shortcut key to navigate between graphics):** "I'm yet another circle, yet another red circle, graphic, yet another red circle."

**Screen reader (Chrome and Edge - shortcut key to navigate between graphics):** "I'm yet another circle, yet another red circle, graphic."
