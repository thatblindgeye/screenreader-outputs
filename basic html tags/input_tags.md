# `<input>`

## `button`

    <input type="button" value="">

**Screen reader:** "Button."

<br>

    <input type="button" value="Add">

**Screen reader:** "Add button"

<br><br>

## `checkbox`

    <label for="enroll">Enroll?</label>
    <input type="checkbox" name="enroll" id="enroll">

**Screen reader:** "Enroll? Checkbox not checked." or "Enroll? Checkbox checked."

<br>

    <input type="checkbox" name="enroll">

**Screen reader:** "Checkbox not checked." or "Checkbox checked."

<hr>

**Notes:** When clicking the checkbox with the `space` or `Enter` key, the screen reader announced the new status of the checkbox, e.g. "Checked" or "Not checked".
<br><br>

## `color`

    <label for="selected-color">Select color:</label>
    <input type="color" name="color" id="selected-color">
    
**Screen reader (Firefox):** "Select color button."

**Screen reader (Chrome and Edge):** "Select color clickable zero percent red, zero percent green, zero percent blue."

<br>

    <input type="color" name="color">
    
**Screen reader (Firefox):** "Button."

**Screen reader (Chrome):** "Clickable zero percent red, zero percent green, zero percent blue."

<hr>

**Notes:** For the color input type, the screen reader announced various settings inside the popup menu when clicking the input with the `space` or `Enter` key.

<br><br>

## `date`

    <label for="selected-date">Select date:</label>
    <input type="date" name="date" id="selected-date">

**Screen reader (Firefox - on page load):** "Select date clickable m m month spin button slash d d day spin button slash y y y y year spin button."

**Screen reader (Firefox - tabbing through each blank field):** "Select date, date edit. Month spin button fifty", "Day spin button fifty", and "Year spin button fifty."

**Screen reader (Chrome and Edge - on page load):** "Select date clickable spin button clickable m m slash spin button clickable d d slash spin button clickable y y y y menu button submenu show date picker."

**Screen reader (Chrome and Edge - tabbing through each blank field):** "Select date, date edit. Month select date, spin button zero", "Day select date, spin button zero", "Year select date, spin button zero", and "Show date picker menu button sub-menu."

<br>

    <input type="date" name="date">

**Screen reader (Firefox - on page load):** "Clickable month spin button m m slash day spin button d d slash year spin button y y y y."

**Screen reader (Firefox - tabbing through each blank field):** "Date edit. Month spin button fifty. Day spin button fifty. Year spin button fifty."

**Screen reader (Chrome and Edge - on page load):** "Clickable month spin button clickable m m slash day spin button clickable d d slash year spin button clickable y y y y menu button submenu show date picker."

**Screen reader (Chrome and Edge - tabbing through each blank field):** "Date edit. Month spin button zero", "Day spin button zero", "Year spin button zero", and "Show date picker menu button sub-menu."

<hr>

**Notes:** When the date field is filled in with an actual date, the screen reader announced the numbers for each spin button field, e.g. May 1st 2021 was announced with "zero five", "zero one", and "twenty-twenty".

Additionally, when a date is filled out in Firefox, the screen reader may announce a "clear button" button when pressing the `tab` key while the year field is the active field.

<br><br>

## `email`

    <label for="user-email">Email:</label>
    <input type="email" name="email" id="user-email">

**Screen reader (Firefox - on page load):** "Clickable email, edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Email, edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Email, edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Email, edit blank."

<br>

    <input type="email" name="email">
    
**Screen reader (Firefox - on page load):** "Edit, has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Edit, has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Edit blank."

<br><br>

## `file`

    <label for="selected-file">Choose a file:</label>
    <input type="file" name="file" id="selected-file">

**Screen reader (Firefox):** "Clickable choose a file, grouping button browse. No file selected. Out of grouping."

**Screen reader (Chrome and Edge):** "Choose a file, button choose a file."

**Example Notes:** When a file is selected and the input is navigated to with the `tab` key in Firefox only, the screen reader announced the name of the file instead of "No file selected".

For Chrome and Edge, the contents of the label element overrides the actual "Choose a file" text inside the button from the `file` input. 

<br>

    <input type="file" name="file">

**Screen reader (Firefox):** "Button browse. No file selected.

**Screen reader (Chrome and Edge):** "Button, no file chosen. Choose file."

**Example Notes:** When a file is selected and the input is navigated to with the `tab` key in all three browsers, the screen reader announced the name of the file instead of "No file chosen" or "No file selected".

<br>

    <input type="file" name="files" multiple>
    
**Screen reader (Firefox):** "Button browse. No files selected."

**Screen reader (Chrome and Edge):** "Button no file chosen, choose files."

**Example Note:** When at least one file is selected and the input is navigated to with the `tab` key in all three browsers, the screen reader announced the name of the file (only one file chosen) or the number of files ("2 files chosen") instead of "No file chosen" or "No file selected".

<br><br>

## `image`

    <label for="image-input">Submit</label>
    
    <input type="image" id="image-input" src="//unsplash.it/50" alt="submit image">
    
**Screen reader (Firefox - on page load):** "Button submit."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Clickable submit button submit." 

**Screen reader (Chrome and Edge - on page load):** "Submit button submit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Submit button."

<br>

    <input type="image" src="//unsplash.it/50" alt="submit">

**Screen reader:** "Submit button."

<br><br>

## `month`

    <label for="selected-month">Choose a month:</label>
    <input type="month" name="month" id="selected-month">

**Screen reader (Chrome and Edge - on page load):** "Choose a month clickable spin button clickable spin button clickable menu button submenu show month picker"

**Screen Reader (Chrome and Edge - tabbing through each blank field):** "Choose a month, date edit. Month choose a month, spin button zero", "Year choose a month, spin button zero", and "Show month picker menu button submenu."

<br>

    <input type="month" name="month">

**Screen reader (Chrome and Edge - on page load):** "Clickable month spin button clickable year spin button clickable menu button submenu show month picker"

**Screen Reader (Chrome and Edge - tabbing through each blank field):** "Date edit. Month spin button zero", "Year spin button zero", and "Show month picker menu button submenu."

<hr>

**Notes:** When the month fields are filled in with an actual month, the screen reader announced the input for each spin button field, e.g. May 2021 was announced with "Month spin button May" and "Year spin button twenty twenty-one".

The month input is not available in Firefox, and will default to a normal `text` input.

<br><br>

## `number`

    <label for="chosen-number">Choose a number:</label>
    <input type="number" name="number" id="chosen-number">

**Screen reader (Firefox - on page load):** "Clickable choose a number. Spin button has auto-complete editable."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Choose a number. Spin button has auto-complete editable blank."

**Screen reader (Chrome and Edge - on page load):** "Choose a number. Spin button editable."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Choose a number. Spin button editable blank."

<br>

    <input type="number" name="number">

**Screen reader (Firefox - on page load):** "Spin button has auto-complete editable."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Spin button has auto-complete editable blank."

**Screen reader (Chrome and Edge - on page load):** "Spin button editable."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Spin button editable blank."

<br>

    <input type="number" name="number" min="5">

**Example Notes:** The screen reader had the same outputs as the example above, and did not indicate that the field had a minimum number.

<br><br>

## `password`

    <label for="password">Password:</label>
    <input type="password" name="password" id="password">

**Screen reader (Firefox - on page load):** "Clickable password. edit protected."

**Screen reader (Chrome and Edge - on page load):** "Password. Edit protected."

**Screen reader (using the `tab` key to navigate the page):** "Password. Edit protected blank."

<br>

    <input type="password" name="password">

**Screen reader (on page load):** "Edit protected."

**Screen reader (using the `tab` key to navigate the page):** "Edit protected blank."

<hr>

**Notes:** With the option to announce typed characters enabled, the screen reader announced "star" in all three browsers instead of the actual character. When deleting characters from the field, instead of announcing the actual character, the screen reader announced "bullet" in Chrome and Edge, and "circle" in Firefox.

<br><br>

## `radio`

    <label for="radio-one">One</label>
    <input type="radio" name="number" value="one" id="radio-one">

**Screen reader (Firefox - on page load):** "Clickable one radio button not checked."

**Screen reader (Chrome and Edge - on page load):** "Radio button not checked one."

**Screen reader (using the `tab` key to navigate the page):** "One radio button not checked one of one."

<br>


    <label for="radio-one">One</label>
    <input type="radio" name="number" value="one" id="radio-one">
    <label for="radio-two">Two</label>
    <input type="radio" name="number" value="two" id="radio-two">

**Screen reader (Firefox - on page load):** "Clickable one radio button not checked, clickable two radio button not checked."

**Screen reader (Firefox - using the `tab` key to navigate the page with no inputs checked):** "One radio button not checked one of two, two radio button not checked two of two."

**Screen reader (Chrome and Edge - on page load):** "Radio button not checked one, radio button not checked two."

**Screen reader (using any arrow key to navigate the radio buttons):** "One radio button checked, one of two", or "Two radio button checked two of two."

<br>

    <input type="radio" name="number" value="two">

**Screen reader:** "Radio button not checked." or "Radio button checked."

<hr>

**Notes:** When no radio button in a grouping is checked and it is clicked with the `space` key, the screen reader announced "checked", similar to the `checkbox` input.

<br><br>

## `range`

    <label for="volume-range">Volume:</label>
    <input type="range" name="range" id="volume-range" min="0" max="100" value="50">

**Screen reader (Firefox):** "Clickable volume, slider 50."

**Screen reader (Chrome and Edge:** "Volume, slider 50."

<br>

    <input type="range" name="range" min="0" max="100" value="50">
    
**Screen reader (Chrome and Edge:** "Slider 50.

<hr>

**Notes:** When the slider was changed using the `left arrow`/`down arrow` or `up arrow`/`right arrow` keys, the screen reader announced the new value.

<br><br>

    <input type="reset" value="">

**Screen reader:** "Button."

<br>

    <input type="reset" value="Reset Form">

**Screen reader:** "Button reset form."

<br><br>

    <label for="search-field">Search:</label>
    <input type="search" name="search" id="search-field">
    
**Screen reader (Firefox - on page load):** "Clickable search, edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Search, edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Search, edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Search, edit blank."

<br>

    <input type="search" name="search">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Edit blank."

<br><br>

    <input type="submit" value="">

**Screen reader:** "Button."

<br>

    <input type="submit" value="Submit Form">

**Screen reader:** "Button submit form."

<br><br>

    <label for="phone-number">Phone:</label>
    <input type="tel" name="telephone" id="phone-number">

**Screen reader (Firefox - on page load):** "Clickable phone, edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Phone, edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Phone, edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Phone, edit blank."

<br>

    <input type="tel" name="telephone">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Edit blank."

<br><br>

    <input type="text">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Edit blank."

<br>

    <input type="text" maxlength="10">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Edit blank."

<br>

    <input type="text" name="first-name">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Edit blank."

<br>

    <input type="text" placeholder="Enter a name">

**Screen reader (Firefox - on page load):** "Enter a name edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Enter a name edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Enter a name edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Enter a name edit blank."

<br>

    <input type="text" required>

**Screen reader (Firefox - on page load):** "Edit required invalid entry has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Edit required invalid entry has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit required invalid entry."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Edit required invalid entry blank."

<br>

    <input type="text" disabled>

**Screen reader (on page load):** "Edit unavailable."

**Example Notes:** The screen reader did not announce anything when using the `tab` key to navigate the page.

<br>

    <input type="text" autocomplete="off">
    
**Screen reader (Firefox - on page load):** "Edit."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Edit blank."

**Exmaple Notes:** This attribute had not effect on the screen reader output in Chrome or Edge.

<br><br>

    <label for="selected-time">Time:</label>
    <input type="time" name="time" id="selected-time">

**Screen reader (Firefox - on page load):** "Clickable time. Grouping clickable hours spin button, minutes spin button, am slash pm edit has auto-complete out of grouping."

**Screen reader (Firefox - tabbing through each blank field):** "Time. Grouping. Hours spin button fifty", "Minutes spin button fifty", and "AM slash PM edit has auto-complete".

**Screen reader (Chrome and Edge - on page load):** "Time. Grouping clickable spin button clickable spin button clickable spin button clickable. Menu button submenu show time picker."

**Screen reader (Chrome and Edge - tabbing through each blank field):** "Time. Grouping. Hours time spin button zero", "Minutes time spin button zero", "AM slash PM time spin button zero", and "Show time picker menu button submenu."

<br>

    <input type="time" name="time">

**Screen reader (Firefox - on page load):** "Clickable hours spin button, minutes spin button, am slash pm edit has auto-complete."

**Screen reader (Firefox - tabbing through each blank field):** "Hours spin button fifty", "Minutes spin button fifty", and "AM slash PM edit has auto-complete".

**Screen reader (Chrome and Edge - on page load):** "Clickable hours spin button clickable minutes spin button clickable AM slash PM spin button clickable. Menu button submenu show time picker."

**Screen reader (Chrome and Edge - tabbing through each blank field):** "Hours spin button zero", "Minutes spin button zero", "AM slash PM spin button zero", and "Show time picker menu button submenu."

<br><br>

    <label for="entered-url">Enter a url:</label>
    <input type="url" name="url" id="entered-url">

**Screen reader (Firefox - on page load):** "Clickable Enter a URL edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Enter a URL edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Enter a URL, edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Enter a URL, edit blank."

<br>

    <input type="url" name="url">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - using the `tab` key to navigate the page):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - using the `tab` key to navigate the page):** "Edit blank."

<br><br>

    <label for="selected-week">Select a week:</label>
    <input type="week" name="week" id="selected-week">

**Screen reader (Chrome and Edge - on page load):** "Select a week, clickable week spin button clickable spin button clickable menu button submenu show week picker"

**Screen Reader (Chrome and Edge - tabbing through each blank field):** "Select a week. Date edit. Week select a week, spin button zero", "Year select a week, spin button zero", and "Show week picker menu button submenu."

<br>

    <input type="week" name="week">

**Screen reader (Chrome and Edge - on page load):** "Clickable week week spin button clickable year spin button clickable menu button submenu show week picker"

**Screen Reader (Chrome and Edge - tabbing through each blank field):** "Date edit. Week spin button zero", "Year spin button zero", and "Show week picker menu button submenu."

<hr>

**Notes:** When the month fields are filled in with an actual week, the screen reader announced the input for each spin button field, e.g. the 24th week of 2021 was announced with "Week spin button 24" and "Year spin button twenty twenty-one".

The month input is not available in Firefox, and will default to a normal `text` input.
