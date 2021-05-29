# Image Maps

    <img src="//unsplash.it/600" alt="unsplash map" usemap="#unsplashmap">

    <map name="unsplashmap">
      <area shape="rect" coords="0,0,600,200" alt="top third" href="#">
      <area shape="poly" coords="0,225,600,225,600,325,300,325,300,275,0,275,0,225" alt="middle third" href="#">
      <area shape="circle" coords="300,450,100" alt="bottom third" href="#">
    </map>

**Screen reader (Firefox - on page load):** "Graphic, unsplash map."

**Screen reader (Firefox - `tab` key to give focus to a map area):** "Top third link, rect, unsplash map, graphic.", "Middle third link, poly, unsplash map, graphic.", and "Bottom third link, circle, unsplash map, graphic."

**Screen reader (Chrome and Edge - on page load):** "Link, top third, link, middle third, link, bottom third."

**Screen reader (Chrome and Edge - `tab` key to give focus to a map area):** "Top third link.", "Middle third link.", and "Bottom third link."

<br>

**Notes:** In Firefox, the screen reader announced the `alt` attribute of the area, the shape of the area, the `alt` attribute of the image, and finally the word "graphic".
