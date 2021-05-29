# `<input>`

## `<input type="button">`

### With an Empty String for the `value` Attribute

    <input type="button" value="">

**Screen reader:** "Button."

<br><br>

### With Text for the `value` Attribute

    <input type="button" value="Add">

**Screen reader:** "Add, button"

<br>
<hr>
<br>

## `<input type="checkbox">`

### Without a Label

    <input type="checkbox" name="enroll">

**Screen reader:** "Checkbox, not checked." or "Checkbox, checked."

<br><br>

### With a Label

    <label for="enroll">Enroll?</label>
    <input type="checkbox" name="enroll" id="enroll">

**Screen reader:** "Enroll, checkbox, not checked." or "Enroll, checkbox, checked."

<br>

**Notes:** When clicking the checkbox with the `space` or `Enter` key, the screen reader announced the new status of the checkbox, e.g. "checked" or "not checked".

<br>
<hr>
<br>

## `<input type="color">`

### Without a Label

    <input type="color" name="color">

**Screen reader (Firefox):** "Button."

**Screen reader (Chrome):** "Clickable, zero percent red, zero percent green, zero percent blue."

<br><br>

### With a Label

    <label for="selected-color">Select color:</label>
    <input type="color" name="color" id="selected-color">

**Screen reader (Firefox):** "Select color, button."

**Screen reader (Chrome and Edge):** "Select color, clickable, zero percent red, zero percent green, zero percent blue."

<br>

**Notes:** For the color input type, the screen reader announced various settings inside the popup menu when clicking the input with the `space` or `Enter` key.

<br>
<hr>
<br>

## `<input type="date">`

### Without a Label

    <input type="date" name="date">

**Screen reader (Firefox - on page load):** "Clickable, month spin button m m slash day spin button d d slash year spin button y y y y."

**Screen reader (Firefox - tabbing through each blank field):** "Date edit. Month spin button fifty. Day spin button fifty. Year spin button fifty."

**Screen reader (Chrome and Edge - on page load):** "Clickable month spin button clickable m m slash day spin button clickable d d slash year spin button clickable y y y y menu button submenu show date picker."

**Screen reader (Chrome and Edge - tabbing through each blank field):** "Date edit. Month spin button zero", "Day spin button zero", "Year spin button zero", and "Show date picker menu button sub-menu."

<br><br>

### With a Label

    <label for="selected-date">Select date:</label>
    <input type="date" name="date" id="selected-date">

**Screen reader (Firefox - on page load):** "Select date, clickable, m m month spin button slash d d day spin button slash y y y y year spin button."

**Screen reader (Firefox - tabbing through each blank field):** "Select date, date edit. Month spin button fifty", "Day spin button fifty", and "Year spin button fifty."

**Screen reader (Chrome and Edge - on page load):** "Select date, clickable spin button clickable m m slash spin button clickable d d slash spin button clickable y y y y menu button submenu show date picker."

**Screen reader (Chrome and Edge - tabbing through each blank field):** "Select date, date edit. Month select date, spin button zero", "Day select date, spin button zero", "Year select date, spin button zero", and "Show date picker menu button sub-menu."

<br>

**Notes:** When the date field is filled in with an actual date, the screen reader announced the numbers for each spin button field, e.g. May 1st 2021 was announced with "zero five", "zero one", and "twenty-twenty".

Additionally, when a date is filled out in Firefox, the screen reader may announce a "clear button" button when pressing the `tab` key while the year field is the active field.

<br>
<hr>
<br>

## `<input type="email">`

### Without a Label

    <input type="email" name="email">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Edit blank."

<br><br>

### With a Label

    <label for="user-email">Email:</label>
    <input type="email" name="email" id="user-email">

**Screen reader (Firefox - on page load):** "Clickable email edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Email edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Email edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Email edit blank."

<br>
<hr>
<br>

## `<input type="file">`

### Without a Label

    <input type="file" name="file">

**Screen reader (Firefox):** "Button browse. No file selected.

**Screen reader (Chrome and Edge):** "Button, no file chosen. Choose file."

<br>

**Example Notes:** When a file is selected and the input is navigated to with the `tab` key in all three browsers, the screen reader announced the name of the file instead of "No file chosen" or "No file selected".

<br><br>

### Without a Label and With the `multiple` Attribute

    <input type="file" name="files" multiple>

**Screen reader (Firefox):** "Button browse. No files selected."

**Screen reader (Chrome and Edge):** "Button no file chosen, choose files."

<br>

**Example Notes:** When at least one file is selected and the input is navigated to with the `tab` key in all three browsers, the screen reader announced the name of the file (only one file chosen) or the number of files ("2 files chosen") instead of "No file chosen" or "No file selected".

<br><br>

### With a Label

    <label for="selected-file">Choose a file:</label>
    <input type="file" name="file" id="selected-file">

**Screen reader (Firefox):** "Clickable choose a file, grouping button browse. No file selected. Out of grouping."

**Screen reader (Chrome and Edge):** "Choose a file, button, choose a file."

<br>

**Example Notes:** When a file is selected and the input is navigated to with the `tab` key in Firefox only, the screen reader announced the name of the file instead of "No file selected".

For Chrome and Edge, the contents of the label element overrides the actual "Choose a file" text inside the button from the `file` input.

<br>
<hr>
<br>

## `<input type="image">`

### Without a Label

    <input type="image" src="//unsplash.it/50" alt="submit">

**Screen reader:** "Submit button."

<br><br>

### With a Label

    <label for="image-input">Submit</label>
    <input type="image" id="image-input" src="//unsplash.it/50" alt="submit image">

**Screen reader (Firefox - on page load):** "Button, submit."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Clickable submit button submit."

**Screen reader (Chrome and Edge - on page load):** "Submit button submit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Submit button."

<br>
<hr>
<br>

## `<input type="month">`

### Without a Label

    <input type="month" name="month">

**Screen reader (Chrome and Edge - on page load):** "Clickable month spin button clickable year spin button clickable menu button submenu show month picker"

**Screen Reader (Chrome and Edge - tabbing through each blank field):** "Date edit. Month spin button zero", "Year spin button zero", and "Show month picker menu button submenu."

<br><br>

### With a Label

    <label for="selected-month">Choose a month:</label>
    <input type="month" name="month" id="selected-month">

**Screen reader (Chrome and Edge - on page load):** "Choose a month clickable spin button clickable spin button clickable menu button submenu show month picker"

**Screen Reader (Chrome and Edge - tabbing through each blank field):** "Choose a month, date edit. Month choose a month, spin button zero", "Year choose a month, spin button zero", and "Show month picker menu button submenu."

<br>

**Notes:** When the month fields are filled in with an actual month, the screen reader announced the input for each spin button field, e.g. May 2021 was announced with "Month spin button May" and "Year spin button twenty twenty-one".

The month input is not available in Firefox, and will default to a text input.

<br>
<hr>
<br>

## `<input type="number">`

### Without a Label

    <input type="number" name="number">

**Screen reader (Firefox - on page load):** "Spin button has auto-complete editable."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Spin button has auto-complete editable blank."

**Screen reader (Chrome and Edge - on page load):** "Spin button editable."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Spin button editable blank."

<br><br>

### Without a Label and With the `min` Attribute

    <input type="number" name="number" min="5">

**Example Notes:** The screen reader had the same outputs as the example above, and did not indicate that the field had the `minimum` attribute.

<br><br>

### With a Label

    <label for="chosen-number">Choose a number:</label>
    <input type="number" name="number" id="chosen-number">

**Screen reader (Firefox - on page load):** "Clickable choose a number. Spin button has auto-complete editable."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Choose a number. Spin button has auto-complete editable blank."

**Screen reader (Chrome and Edge - on page load):** "Choose a number. Spin button editable."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Choose a number. Spin button editable blank."

<br>
<hr>
<br>

## `<input type="password">`

### Without a Label

    <input type="password" name="password">

**Screen reader (on page load):** "Edit protected."

**Screen reader (`tab` key to give focus to the input):** "Edit protected blank."

<br><br>

### With a Label

    <label for="password">Password:</label>
    <input type="password" name="password" id="password">

**Screen reader (Firefox - on page load):** "Clickable password. edit protected."

**Screen reader (Chrome and Edge - on page load):** "Password. Edit protected."

**Screen reader (`tab` key to give focus to the input):** "Password. Edit protected blank."

<br>

**Notes:** With the option to announce typed characters enabled, the screen reader announced "star" in all three browsers instead of the actual character. When deleting characters from the field, instead of announcing the actual character, the screen reader announced "bullet" in Chrome and Edge, and "circle" in Firefox.

<br>
<hr>
<br>

## `<input type="radio">`

### Without a Label - Single Input

    <input type="radio" name="number" value="two">

**Screen reader:** "Radio button not checked." or "Radio button checked."

<br><br>

### With a Label - Single Input

    <label for="radio-one">One</label>
    <input type="radio" name="number" value="one" id="radio-one">

**Screen reader (Firefox - on page load):** "Clickable one radio button not checked."

**Screen reader (Chrome and Edge - on page load):** "Radio button not checked one."

**Screen reader (`tab` key to give focus to the input):** "One radio button not checked one of one."

<br><br>

### With a Label - Multiple Inputs

    <label for="radio-one">One</label>
    <input type="radio" name="number" value="one" id="radio-one">
    <label for="radio-two">Two</label>
    <input type="radio" name="number" value="two" id="radio-two">

**Screen reader (Firefox - on page load):** "Clickable one radio button not checked, clickable two radio button not checked."

**Screen reader (Firefox - `tab` key to give focus to the input with no input checked):** "One radio button not checked one of two, two radio button not checked two of two."

**Screen reader (Chrome and Edge - on page load):** "Radio button not checked one, radio button not checked two."

**Screen reader (using any arrow key to navigate a group of radio buttons):** "One radio button checked, one of two", or "Two radio button checked two of two."

<br>

**Notes:** When no radio button in a grouping is checked and it is clicked with the `space` key, the screen reader announced "checked", similar to the `checkbox` input.

<br>
<hr>
<br>

## `<input type="range">`

### Without a Label

    <input type="range" name="range" min="0" max="100" value="50">

**Screen reader (Chrome and Edge:** "Slider 50.

<br><br>

### With a Label

    <label for="volume-range">Volume:</label>
    <input type="range" name="range" id="volume-range" min="0" max="100" value="50">

**Screen reader (Firefox):** "Clickable volume, slider 50."

**Screen reader (Chrome and Edge:** "Volume, slider 50."

<br>

**Notes:** When the slider was changed using the `left arrow`/`down arrow` or `up arrow`/`right arrow` keys, the screen reader announced the new value.

<br>
<hr>
<br>

## `<input type="reset">`

### With an Empty String for the `value` Attribute

    <input type="reset" value="">

**Screen reader:** "Button."

<br><br>

### With Text for the `value` Attribute

    <input type="reset" value="Reset Form">

**Screen reader:** "Button reset form."

<br>
<hr>
<br>

## `<input type="search">`

### Without a Label

    <input type="search" name="search">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Edit blank."

<br><br>

### With a Label

    <label for="search-field">Search:</label>
    <input type="search" name="search" id="search-field">

**Screen reader (Firefox - on page load):** "Clickable search, edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Search, edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Search, edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Search, edit blank."

<br>
<hr>
<br>

## `<input type="submit">`

### With an Empty String for the `value` Attribute

    <input type="submit" value="">

**Screen reader:** "Button."

<br><br>

### With Text for the `value` Attribute

    <input type="submit" value="Submit Form">

**Screen reader:** "Button submit form."

<br>
<hr>
<br>

## `<input type="tel">`

### Without a Label

    <input type="tel" name="telephone">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Edit blank."

<br><br>

### With a Label

    <label for="phone-number">Phone:</label>
    <input type="tel" name="telephone" id="phone-number">

**Screen reader (Firefox - on page load):** "Clickable phone, edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Phone, edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Phone, edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Phone, edit blank."

<br>
<hr>
<br>

## `<input type="text">`

### Without a Label

    <input type="text">

    <input type="text" maxlength="10">

    <input type="text" name="first-name">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Edit blank."

<br><br>

### Without a Label and With a Placeholder

    <input type="text" placeholder="Enter a name">

**Screen reader (Firefox - on page load):** "Enter a name edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Enter a name edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Enter a name edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Enter a name edit blank."

<br><br>

### Without a Label and With the `required` Attribute

    <input type="text" required>

**Screen reader (Firefox - on page load):** "Edit required invalid entry has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Edit required invalid entry has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit required invalid entry."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Edit required invalid entry blank."

<br><br>

### Without a Label and With the `disabled` Attribute

    <input type="text" disabled>

**Screen reader (on page load):** "Edit unavailable."

<br>

**Example Notes:** The screen reader did not announce the presence of the input when using the `tab` key to navigate the page.

<br><br>

### Without a Label and With the `auto-complete="off"` Attribute

    <input type="text" autocomplete="off">

**Screen reader (Firefox - on page load):** "Edit."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Edit blank."

<br>

**Exmaple Notes:** This attribute had no effect on the screen reader output in Chrome or Edge as these were the default outputs for the browsers.

<br>
<hr>
<br>

## `<input type="time">`

### Without a Label

    <input type="time" name="time">

**Screen reader (Firefox - on page load):** "Clickable hours spin button, minutes spin button, am slash pm edit has auto-complete."

**Screen reader (Firefox - tabbing through each blank field):** "Hours spin button fifty", "Minutes spin button fifty", and "AM slash PM edit has auto-complete".

**Screen reader (Chrome and Edge - on page load):** "Clickable hours spin button clickable minutes spin button clickable AM slash PM spin button clickable. Menu button submenu show time picker."

**Screen reader (Chrome and Edge - tabbing through each blank field):** "Hours spin button zero", "Minutes spin button zero", "AM slash PM spin button zero", and "Show time picker menu button submenu."

<br><br>

### With a Label

    <label for="selected-time">Time:</label>
    <input type="time" name="time" id="selected-time">

**Screen reader (Firefox - on page load):** "Clickable time. Grouping clickable hours spin button, minutes spin button, am slash pm edit has auto-complete out of grouping."

**Screen reader (Firefox - tabbing through each blank field):** "Time. Grouping. Hours spin button fifty", "Minutes spin button fifty", and "AM slash PM edit has auto-complete".

**Screen reader (Chrome and Edge - on page load):** "Time. Grouping clickable spin button clickable spin button clickable spin button clickable. Menu button submenu show time picker."

**Screen reader (Chrome and Edge - tabbing through each blank field):** "Time. Grouping. Hours time spin button zero", "Minutes time spin button zero", "AM slash PM time spin button zero", and "Show time picker menu button submenu."

<br>
<hr>
<br>

## `<input type="url">`

### Without a Label

    <input type="url" name="url">

**Screen reader (Firefox - on page load):** "Edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Edit blank."

<br><br>

### With a Label

    <label for="entered-url">Enter a url:</label>
    <input type="url" name="url" id="entered-url">

**Screen reader (Firefox - on page load):** "Clickable Enter a URL edit has auto-complete."

**Screen reader (Firefox - `tab` key to give focus to the input):** "Enter a URL edit has auto-complete blank."

**Screen reader (Chrome and Edge - on page load):** "Enter a URL, edit."

**Screen reader (Chrome and Edge - `tab` key to give focus to the input):** "Enter a URL, edit blank."

<br>
<hr>
<br>

## `<input type="week">`

### Without a Label

    <input type="week" name="week">

**Screen reader (Chrome and Edge - on page load):** "Clickable week week spin button clickable year spin button clickable menu button submenu show week picker"

**Screen Reader (Chrome and Edge - tabbing through each blank field):** "Date edit. Week spin button zero", "Year spin button zero", and "Show week picker menu button submenu."

<br><br>

### With a Label

    <label for="selected-week">Select a week:</label>
    <input type="week" name="week" id="selected-week">

**Screen reader (Chrome and Edge - on page load):** "Select a week, clickable week spin button clickable spin button clickable menu button submenu show week picker"

**Screen Reader (Chrome and Edge - tabbing through each blank field):** "Select a week. Date edit. Week select a week, spin button zero", "Year select a week, spin button zero", and "Show week picker menu button submenu."

<br>

**Notes:** When the month fields are filled in with an actual week, the screen reader announced the input for each spin button field, e.g. the 24th week of 2021 was announced with "Week spin button 24" and "Year spin button twenty twenty-one".

The month input is not available in Firefox, and will default to a text input.
