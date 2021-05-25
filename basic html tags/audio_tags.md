# `<audio>`

    // no controls
    <audio src="./assets/sound_sample.wav"></audio>

**Screen reader:** The screen reader did not have any output for this example.

<hr>

    // no controls and autplay
    <audio src="./assets/sound_sample.wav" autoplay></audio>

**Screen reader:** The screen reader did not have any output for this example.

**Example notes:** The audio automatically began playing when the page loaded.

<hr>

    // controls and autoplay
    <audio src="./assets/sound_sample.wav" controls autoplay></audio>
    
**Screen reader (Firefox - on page load):** "Play. Loading 100 percent. Position slider midnight slash three-fourteen. Button mute. Volume slider 100."

**Screen reader (Firefox - tabbing through each controls button):** "Play button", "Position slider midnight slash three-fourteen", "Mute button", and "Volume slider 100".

**Screen reader (Chrome and Edge - on page load):** "Play. Midnight slash three-thirteen. Audio time scrubber midnight slash three-thirteen slider elapsed time. Midnight. Button mute. Button show more media controls."

**Screen reader (Chrome and Edge - tabbing through each controls button):** "Play button", "Audio time scrubber midnight slash midnight slider elapsed time. Midnight", "Volume slider one", "Mute button", and "Show more media controls button more options".

**Example notes:** The audio automatically began playing when the page loaded.

When changing the timer position, the screen reader announced the new timer position. For Firefox it announced, "zero-fifteen slash three-fourteen," and for Chrome and Edge it announced, "Audio time scrubber zero-fifteen slash three-thirteen slider elapsed time. Zero-fifteen."

When changing the volume, the screen reader announced the new value of the volume. For Firefox, the values ranged from 0 to 100, and in Chrome and Edge the values ranged from 0.0 to 1.0.

When pressing the "Play" button, the screen reader announced "Pause" as the button changed, and vice versa announced "Play" when pressing the "Pause" button.

When pressing the "Mute" button, the screen reader announced "Unmute" as the button changed, and vice versa announced "Mute" when pressing the "Unmute" button.

<hr>

    // controls
    <audio src="./assets/sound_sample.wav" controls></audio>

**Screen reader:** This example had the same outputs as the `// controls and autoplay` example, except the audio doesn't automatically play when the page loads.

<hr>

    // sources
    <audio controls>
      <source src="./assets/sound_sample.wav" type="audio/wav">
      Your browser does not support the audio tag.
    </audio>

**Screen reader:** This example had the same outputs as the `// controls and autoplay` example, except the audio doesn't automatically play when the page loads.

<hr>

    // unsupported
    <audio controls>
      Your browser does not support the audio tag.
    </audio>
    
**Screen reader (Firefox - on page load):** "Button play. Loading. Position slider zero. Button mute. Volume slider 100."

**Screen reader (Firefox - tabbing through each controls button):** "Play button", "Position slider zero", "Mute button", and "Volume slider 100".
    
**Screen reader (Chrome and Edge - on page load):** "Grouping unavailable button unavailable play. Midnight slash midnight. Audio time scrubber midnight slash midnight slider unavailable elapsed time. Midnight. Button unavailable mute."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page and give the media controls focus):** "Unable to play media. Grouping play button unavailable. Midnight slash midnight elapsed time. Midnight audio time scrubber midnight slash midnight slider unavailable. Mute."

<hr>

**Notes:** Be mindful of using audio that auto plays without any warning or audio that has no way to control the volume.

The audio element does not indicate what the sound that will be played is named. Using ARIA attributes or a `<figure>` and `<figcaption>` tag may aid in offering context for the audio being played. See the [MDN page on the `<audio>` tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio) for an example using the `<figure>` tag.


