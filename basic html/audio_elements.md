# `<audio>`

Be mindful of using audio that plays without any warning or audio that the user cannot control the volume or playback of. What may make your page stand out can be incredibly startling or distracting.

The audio element does not indicate the name of the media that will be played. Using ARIA attributes or `<figure>` and `<figcaption>` elements may aid in offering context for the audio being played. See the [MDN page on the `<audio>` element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio) for an example using the `<figure>` element.

<br><br>

## Audio without Controls

    // no controls
    <audio src="./assets/sound_sample.wav"></audio>

    // no controls and autplay
    <audio src="./assets/sound_sample.wav" autoplay></audio>

**Screen reader:** The screen reader did not have any output for this example.

<br><br>

## Audio with Controls

### With `autoplay` Attribute

    <audio src="./assets/sound_sample.wav" controls autoplay></audio>

**Screen reader (Firefox - on page load):** "Play, loading 100 percent, position slider midnight slash three-fourteen, button mute, volume slider 100."

**Screen reader (Firefox - tabbing through each control button):** "Play button", "Position slider midnight slash three-fourteen", "Mute button", and "Volume slider 100".

**Screen reader (Chrome and Edge - on page load):** "Play, midnight slash three-thirteen audio time scrubber midnight slash three-thirteen slider elapsed time midnight, button mute, button show more media controls."

**Screen reader (Chrome and Edge - tabbing through each control button):** "Play button", "Audio time scrubber midnight slash midnight slider elapsed time. Midnight", "Volume slider one", "Mute button", and "Show more media controls button more options".

<br>

**Example notes:** When changing the timer position, the screen reader announced the new timer position. For Firefox it announced, "zero-fifteen slash three-fourteen," and for Chrome and Edge it announced, "Audio time scrubber zero-fifteen slash three-thirteen slider elapsed time zero-fifteen."

When changing the volume, the screen reader announced the new value of the volume. For Firefox, the values ranged from 0 to 100, and in Chrome and Edge the values ranged from 0.0 to 1.0.

When pressing the "Play" button, the screen reader announced "Pause" after the button updated, and vice versa announced "Play" when pressing the "Pause" button.

When pressing the "Mute" button, the screen reader announced "Unmute" as the button updated, and vice versa announced "Mute" when pressing the "Unmute" button.

<br><br>

### Without `autoplay` Attribute

    <audio src="./assets/sound_sample.wav" controls></audio>

**Screen reader:** This example had the same outputs as the `// controls and autoplay` example, except the audio doesn't automatically play when the page loads.

<br><br>

### With Valid `<source>` Element

    <audio controls>
      <source src="./assets/sound_sample.wav" type="audio/wav">
      Your browser does not support the audio tag.
    </audio>

**Screen reader:** This example had the same outputs as the `// controls and autoplay` example, except the audio doesn't automatically play when the page loads.

<br><br>

### With Invalid `<source>` Element

    <audio controls>
      Your browser does not support the audio tag.
    </audio>

**Screen reader (Firefox - on page load):** "Button play, loading, position slider zero, button mute, volume slider 100."

**Screen reader (Firefox - tabbing through each control button):** "Play button", "Position slider zero", "Mute button", and "Volume slider 100".

**Screen reader (Chrome and Edge - on page load):** "Grouping unavailable, button unavailable play, midnight slash midnight audio time scrubber midnight slash midnight slider unavailable elapsed time midnight, button unavailable mute."

**Screen reader (Chrome and Edge - `tab` key to give focus to the media control):** "Unable to play media, grouping play button unavailable, midnight slash midnight elapsed time midnight audio time scrubber midnight slash midnight slider unavailable, mute."
