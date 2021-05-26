# Image Links

    <a href="https://www.google.com/">
      <img src="//unsplash.it/100" />
    </a>
    
**Screen reader (Firefox):** "Link graphic w w w dot google dot com." or "Visited link graphic w w w dot google dot com."

**Screen reader (Chrome and Edge - on page load):** "Link graphic 100." or "Visited link graphic 100."

**Screen reader (Chrome - using the `tab` key or keyboard shortcut for links to navigate the page):** "100 unlabelled graphic link." or "100 unlabelled graphic visited link."

**Screen reader (Edge - using the `tab` key or keyboard shortcut for links to navigate the page):** "100 graphic link." or "100 graphic visited link."

<br>

    <a href="https://www.google.com/">
        <svg width="100" height="100">
            <circle cx="50" cy="50" r="40" fill="red" />
        </svg>
    </a>

**Screen reader (Firefox):** "Link w w w dot google dot com." or "Visited link w w w dot google dot com."

**Screen reader (Chrome and Edge - on page load):** "Link w w w dot google dot com graphic." or "Visited link w w w dot google dot com graphic."

**Screen reader (Chrome and Edge - using the `tab` key or keyboard shortcut for links to navigate the page):** "Link w w w dot google dot com." or "Visited link w w w dot google dot com."

<br><br>

    <a href="https://www.google.com/">
      <img src="//unsplash.it/100" />
      Go to Google
    </a>
    
**Screen reader (on page load):** "Link go to google." or "Visited link go to google."

**Screen reader (Firefox - using the `tab` key or keyboard shortcut for links to navigate the page):** "w w w dot google dot com graphic go to google link." or "w w w dot google dot com graphic go to google visited link."

**Screen reader (Chrome and Edge - using the `tab` key or keyboard shortcut for links to navigate the page):** "Go to google link." or "Go to google visited link."

<br>

    <a href="https://www.google.com/">
        <svg width="100" height="100">
            <circle cx="50" cy="50" r="40" fill="red" />
        </svg>
        Go to Google
    </a>
    
**Screen reader:** "Link go to google." or "Visited link go to google."

<br><br>

    <a href="https://www.google.com/">
      <img src="//unsplash.it/100" alt="" />
    </a>
    
**Screen reader:** "Link w w w dot google dot com." or "Visited link w w w dot google dot com."

<br><br>

    <a href="https://www.google.com/">
      <img src="//unsplash.it/100" alt="Google" />
    </a>
    
**Screen reader:** "Link graphic Google." or "Visited link graphic Google."

<br><br>

    <a title="Google it" href="https://www.google.com/">
        <img src="//unsplash.it/100" />
    </a>
    
    <a title="Google it" href="https://www.google.com/">
        <svg width="100" height="100">
            <circle cx="50" cy="50" r="40" fill="red" />
        </svg>
     </a>
    
**Screen reader:** "Link google it." or "Visited link google it."

<br><br>

    <a href="https://www.google.com/">
      <img title="Google it" src="//unsplash.it/100" />
    </a>
    
**Screen reader:** "Link graphic google it." or "Visited link graphic google it."

<br>

    <a href="https://www.google.com/">
        <svg width="100" height="100">
            <title>Google it</title>
            <circle cx="50" cy="50" r="40" fill="red" />
        </svg>
    </a>
    
**Screen reader (Firefox):** "Link w w w dot google dot com." or "Visited link w w w dot google dot com."

**Screen reader (Chrome and Edge):** "Link graphic google it." or "Visited link graphic google it."

<br><br>

    <a title="Google now" href="https://www.google.com/">
      <img title="Google it" src="//unsplash.it/100" />
    </a>
    
**Screen reader (on page load):** "Link graphic google it." or "Visited link graphic google it."

**Screen reader (using the `tab` key or keyboard shortcut for links to navigate the page):** "Google it graphic link google now." or "Google it graphic visited link google now."

<br>

    <a title="Google now" href="https://www.google.com/">
        <svg width="100" height="100">
            <title>Google it</title>
            <circle cx="50" cy="50" r="40" fill="red" />
        </svg>
    </a>
    
**Screen reader (Firefox - on page load):** "Link google now." or "Visited link google now."

**Screen reader (Chrome and Edge - on page load):** "Link graphic google it." or "Visited link graphic google it."

**Screen reader (Chrome and Edge - using the `tab` key or keyboard shortcut for links to navigate the page):** "Google it graphic link google now." or "Google it graphic visited link google now."


<br><br>

    <a title="Google now" href="https://www.google.com/">
      <img title="Google it" src="//unsplash.it/100" alt="A google hyperlink" />
    </a>
    
**Screen reader (on page load):** "Link graphic a google hyperlink." or "Visited link graphic a google hyperlink."

**Screen reader (using the `tab` key or keyboard shortcut for links to navigate the page):** "A google hyperlink graphic google it link google now." or "A google hyperlink graphic google it visited link google now."

<hr>

**Notes:** When the `alt` attribute is an empty string or is omitted and the image fails to load, there may be no visual indication that there is a link rendered on the page, but it may still be accessible via `tab` key navigation.

The [W3 page on functional images](https://www.w3.org/WAI/tutorials/images/functional/) includes similar examples, including one that uses an icon to signify a link opens in a new window.
