# Previous Examples with ARIA

<br><br>

## Buttons with icons

    <button type="button">
        <span class="material-icons" aria-hidden="true">add</span>
        Add to List
    </button>
    
**Screen reader:** "Button add to list."

**Examples notes:** In a [previous example of buttons with icons](https://github.com/thatblindgeye/screenreader-outputs/blob/main/nested%20html%20tags/buttons-with-icons.md), the screen reader announced duplicate text due to the text content of the `span` tag and the text content of the `button` tag. Using the `aria-hidden` attribute, the text content of the `span` tag should be hidden from the accessibility tree, but allow the icon to visually remain.

<br>

    <button type="button" aria-label="Add New">
        <span class="material-icons">add</span>
    </button>
    
**Screen reader:** "Button add new."

<br><br>

## `audio` and `video`

    <audio src="./assets/sound_sample.wav" aria-label="sound sample" controls></audio>
    
    <span id="media-label" aria-hidden="true">Sound Sample</span>
    <audio src="./assets/sound_sample.wav" aria-labelledby="media-label" controls></audio>
    
**Screen reader (Firefox - on page load):** "Sound sample grouping button play. Loading 100 percent. Position slider midnight slash three-fourteen. Button mute. Volume slider 100 out of grouping."

**Screen reader (Firefox - using the `tab` key to navigate the page and give the media controls focus):** "Sound sample grouping play button. Loading 100 percent. Midnight slash three-fourteen position slider. Mute button. 100."

**Screen reader (Chrome and Edge - on page load):** "Sound sample grouping button play. Midnight slash three-thirteen. Audio time scrubber midnight slash three-thirteen slider elapsed time. Midnight. Button mute. Button show more media controls."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page and give the media controls focus):** "Sound sample grouping play button. Midnight slash three-fourteen elapsed time. Midnight audio time scrubber midnight slash three-fourteen slider mute button show more media controls."

<br>

    <video src="./assets/video_sample.mp4" aria-label="video sample" controls></video>

    <span id="media-label" aria-hidden="true">Video Sample</span>
    <video src="./assets/video_sample.mp4" aria-labelledby="media-label" controls></video>
    
**Screen reader (Firefox - on page load):** "Video sample grouping button. Button play. Loading 100 percent. Position slider midnight slash zero twenty-three. Button mute. Volume slider 100. Button full screen."

**Screen reader (Firefox - using the `tab` key to navigate the page and give the media controls focus):** "Video sample grouping button play button. Loading 100 percent. Midnight slash zero twenty-three position slider mute button 100 volume slider full screen."

**Screen reader (Chrome and Edge - on page load):** "Video sample grouping buffering. Button play. Midnight slash zero twenty-two. Button mute. Button enter full screen. Button show more media controls. Video time scrubber midnight slash zero twenty-two slider elapsed time. Midnight."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page and give the media controls focus):** "Video sample grouping play button midnight slash zero twenty-two mute button enter full screen button show more media controls button more options elapsed time, midnight video time scrubber midnight slash zero twenty-two slider."

<hr>

**Notes:** In a [previous example of the `video` tag](https://github.com/thatblindgeye/screenreader-outputs/blob/main/basic%20html%20tags/video_tags.md) and a [previous example of the `audio` tag](https://github.com/thatblindgeye/screenreader-outputs/blob/main/basic%20html%20tags/audio_tags.md), the screen reader did not give any indication of what the media being played was. Using the `aria-labelledby` attribute may aid in context to the media that is tied to the media player.

Adding the `aria-hidden="true"` attribute prevented the screen reader from duplicating output of the text and from announcing the text when navigating the page using the arrow keys.

Wrapping the media tag inside of a `label` tag did not provide exactly the same output as above. When using the `tab` key to navigate the page and give the media controls focus, the screen reader did not announce the label text as it did in the example above.

Slightly less related to screen reader accessibility, but the MDN page on [Accessible multimedia](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/Multimedia) shows how you can create a custom media player as well as how to implement audio transcripts and video text tracks (another great way to offer accessibility).
