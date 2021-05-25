# `<video>`

    // no controls
    <video src="./assets/video_sample.mp4"></video>

**Screen reader:** The screen reader did not have any output for this example.

<hr>

    // no controls and autoplay
    <video src="./assets/video_sample.mp4" autoplay></video>

**Screen reader:** The screen reader did not have any output for this example.

**Example notes:** The audio automatically began playing when the page loaded.

<hr>

    // controls and autoplay
    <video src="./assets/video_sample.mp4" autoplay></video>

**Screen reader (Firefox - on page load):** "Button. Button play. Loading 100 percent. Position slider midnight slash zero twenty-three. Button mute. Volume slider 100. Button full screen"

**Screen reader (Firefox - tabbing through each controls button):** "Button", "Play button", "Position slider midnight slash zero twenty-three", "Mute button", "Volume slider 100", and "Full screen button".

**Screen reader (Chrome and Edge - on page load):** "Buffering. Button play. Midnight. Button unavailable mute. Button unavailable enter full screen. Button show more media controls. Video time scrubber midnight slash zero twenty-two slider unavailable elapsed time."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page and give the media controls focus):** "Play button midnight slash zero twenty-two mute button enter full screen show more media controls button more options elapsed time, midnight video time scrubber midnight slash zero twenty-two slider.

**Screen reader (Chrome and Edge - tabbing through each controls button):** "Play button", "Volume slider 1", "Mute button", "Enter full screen button", "Show more media controls button more options", and "Video time scrubber midnight slash zero twenty-two slider elapsed time. Midnight."

**Example notes:** The video automatically began playing when the page loaded.

When changing the timer position, the screen reader announced the new timer position. For Firefox it announced, "zero-oh-eight slash zero twenty-three," and for Chrome and Edge it announced, "Video time scrubber zero-oh-eight slash zero twenty-two slider elapsed time. zero-oh-eight."

When changing the volume, the screen reader announced the new value of the volume. For Firefox, the values ranged from 0 to 100, and in Chrome and Edge the values ranged from 0.0 to 1.0.

When pressing the "Play" button, the screen reader announced "Pause" as the button changed, and vice versa announced "Play" when pressing the "Pause" button.

When pressing the "Mute" button, the screen reader announced "Unmute" as the button changed, and vice versa announced "Mute" when pressing the "Unmute" button.

When pressing the "Full screen" button, the screen reader announced "Exit full screen" after entering full screen mode, and indicated how to exit full screen by pressing the `tab` key while in full screen ("Exit full screen. E S C button").

<hr>

    // controls
    <video src="./assets/video_sample.mp4" controls></video>

**Screen reader:** This example had the same outputs as the `// controls and autoplay` example, except the audio doesn't automatically play when the page loads.

<hr>

    // muted
    <video src="./assets/video_sample.mp4" muted></video>

**Screen reader:** This example had the same outputs as the `// controls and autoplay` example, except the audio doesn't automatically play when the page loads and any announcement of a mute button was replaced with "unmute".

<hr>

    // sources
    <video controls>
      <source src="./assets/video_sample.mp4" type="audio/mpeg">
      Your browser does not support the audio tag.
    </video>

**Screen reader:** This example had the same outputs as the `// controls and autoplay` example, except the audio doesn't automatically play when the page loads.

<hr>

    // unsupported
    <video controls>
      Your browser does not support the audio tag.
    </video>

**Screen reader (Firefox - on page load):** "Button. Button play. Loading. Position slider zero. Button mute. Volume slider 100. Button full screen."

**Screen reader (Firefox - tabbing through each controls button):** "Play button", "Position slider zero", "Mute button", "Volume slider 100", and "Full screen button."
    
**Screen reader (Chrome and Edge - on page load):** "Grouping unavailable button unavailable play. Midnight. Button unavailable mute. Button unavailable enter full screen. Button unavailable show more media controls. Video time scrubber midnight slash midnight unavailable slider elapsed time. Midnight."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page and give the media controls focus):** "Unable to play media. Grouping play button unavailable midnight mute button unavailable enter full screen button unavailable show more media controls button unavailable more options elapsed time. Midnight."

<hr>

**Notes:** Be mindful of using video that auto plays without any warning or video that has no way to control the volume.

The video element does not indicate what the video that will be played is named. Using ARIA attributes may aid in offering context for the video being played.
