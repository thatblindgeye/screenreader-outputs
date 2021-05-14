# `<video>`

    // no controls
    <video src="./assets/video_sample.mp4"></video>

**Screen reader announces:** ""

    // no controls and autoplay
    <video src="./assets/video_sample.mp4" autoplay></video>

**Screen reader announces:** ""

    // controls and autoplay
    <video src="./assets/video_sample.mp4" autoplay></video>

**Screen reader announces:** ""

    // controls
    <video src="./assets/video_sample.mp4" controls></video>

**Screen reader announces:** ""

    // muted
    <video src="./assets/video_sample.mp4" muted></video>

**Screen reader announces:** ""

    // sources
    <video controls>
      <source src="./assets/video_sample.mp4" type="audio/mpeg">
      Your browser does not support the audio tag.
    </video>

**Screen reader announces:** ""

    // unsupported
    <video controls>
      Your browser does not support the audio tag.
    </video>

**Screen reader announces:** ""
