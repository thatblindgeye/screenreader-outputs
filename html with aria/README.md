# HTML with ARIA

## Table of Contents

[Roles, State, and Properties](https://github.com/thatblindgeye/screenreader-outputs/blob/main/html%20with%20aria/roles-state-properties.md)
<br>
[ARIA Labels](https://github.com/thatblindgeye/screenreader-outputs/blob/main/html%20with%20aria/aria-labels.md)
<br>
[ARIA Live Regions](https://github.com/thatblindgeye/screenreader-outputs/blob/main/html%20with%20aria/aria-live-regions.md)
<br>
[Previous Examples with ARIA](https://github.com/thatblindgeye/screenreader-outputs/blob/main/html%20with%20aria/previous-examples-with-aria.md)

<br>

This section covers elements that have ARIA attributes added to them. ARIA attributes can help a screen reader announce the correct information to a user, or even prevent something from being announced. This can range from `<span>` or `<div>` tags being used to create a custom checkbox and giving it the `aria-role="checkbox"` attribute, or making sure a `<button>` whose text content is "+ Book" (the plus icon and the word "book") is announced as "Add book".

To understand some basic rules about using ARIA, checkout [ARIA in HTML - Examples of incorrect usage](https://www.w3.org/TR/html-aria/#examples-of-incorrect-usage), [WAI-ARIA Authoring Practices - Read me first](https://www.w3.org/TR/wai-aria-practices/#read_me_first), and [Notes on ARIA Use in HTML](https://www.w3.org/TR/using-aria/#notes2).

For a deeper dive, checkout [ARIA Authoring Practices 1.1](https://www.w3.org/TR/wai-aria-practices-1.1/). There's a lot of information on this page, but it's worth going through at your own pace. You'll learn just how powerful ARIA can be, as well as showing examples of how to create accessible widgets.

A great playlist to watch for accessibility in general are the [A11ycasts with Rob Dodson on Youtube](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g). In terms of ARIA and screen reader accessibility, the following videos are worth a watch:

[Screen Reader Basics: VoiceOver](https://www.youtube.com/watch?v=5R-6WvAihms&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g&index=8)
<br>
[Screen Reader Basics: NVDA](https://www.youtube.com/watch?v=Jao3s_CwdRU&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g&index=10)
<br>
[Alerts!](https://www.youtube.com/watch?v=5lzAj1ahRSI&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g&index=11)
<br>
[Intro to ARIA](https://www.youtube.com/watch?v=g9Qff0b-lHk&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g&index=14&t=222s)
<br>
[States and Properties in ARIA](https://www.youtube.com/watch?v=88tfx3jLV_M&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g&index=15)
<br>
[How to Build a Toggle Button](https://www.youtube.com/watch?v=16gvkPfPIx4&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g&index=26)
