# `<audio>`

    // no controls
    <audio src="./assets/sound_sample.wav"></audio>

**Screen reader announces:** ""

    // no controls and autplay
    <audio src="./assets/sound_sample.wav" autoplay></audio>

**Screen reader announces:** ""

    // controls and autplay
    <audio src="./assets/sound_sample.wav" controls autoplay></audio>

**Screen reader announces:** ""

    // controls
    <audio src="./assets/sound_sample.wav" controls></audio>

**Screen reader announces:** ""

    // sources
    <audio controls>
      <source src="./assets/sound_sample.wav" type="audio/wav">
      Your browser does not support the audio tag.
    </audio>

**Screen reader announces:** ""

    // unsupported
    <audio controls>
      Your browser does not support the audio tag.
    </audio>

**Screen reader announces:** ""

**Note:** If the audio tag does not have the `controls` attribute, a screen reader may not announce the element (note to self: confirm in testing). Also, be mindful of using audio that auto plays without any warning or without any means to control the volume.
