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

**Screen reader:** "Enroll? Checkbox not checked."

<br>

    <input type="checkbox" name="enroll">

**Screen reader:** "Checkbox not checked."

<br><br>

## `color`

    <label for="selected-color">Select color:</label>
    <input type="color" name="color" id="selected-color">
    
**Screen reader (Firefox):** "Select color button."

**Screen reader (Chrome):** "Select color clickable zero percent red, zero percent green, zero percent blue."

<br>

    <input type="color" name="color">
    
**Screen reader (Firefox):** "Button."

**Screen reader (Chrome):** "Clickable zero percent red, zero percent green, zero percent blue."

**Examples Note:** For the color input type, the screen reader announces various settings inside the popup menu when clicking the input.

<br><br>

## `date`

    <label for="selected-date">Select date:</label>
    <input type="date" name="date" id="selected-date">

**Screen reader (Firefox):** "Select date clickable m m month spin button slash d d day spin button slash y y y y year spin button."

**Screen reader (Firefox, tabbing through blank input):** "Month spin button fifty. Day spin button fifty. Year spin button fifty."

**Screen reader (Chrome):** "Select date clickable m m month select date spin button clickable slash d d day select date spin button clickable slash y y y y year select date spin button clickable show date picker."

**Screen reader (Chrome, tabbing through blank input):** "Select date, date edit. Month select date spin button zero. Day select date spin button zero. Year select date spin button zero. Show date picker menu button sub-menu."

<br>

    <input type="date" name="date">

**Screen reader (Firefox):** "Clickable m m month spin button slash d d day spin button slash y y y y year spin button."

**Screen reader (Firefox, tabbing through blank input):** "Select date, date edit. Month spin button fifty. Day spin button fifty. Year spin button fifty."

**Screen reader (Chrome):** "Clickable m m month spin button clickable slash d d day spin button clickable slash y y y y year spin button clickable show date picker."

**Screen reader (Chrome, tabbing through blank input):** "Month spin button zero. Day spin button zero. Year spin button zero. Show date picker menu button sub-menu."

**Exmaples Note:** When the date field is filled in with an actual date, the screen reader announced the numbers for each spin button field, e.g. May 1st 2021 was announced with "zero five", "zero one", and "twenty-twenty".

Additionally, in Firefox the screen reader announced, "clear button" at the end when the date field was filled out.

<br><br>

## `email`

    <label for="user-email">Email:</label>
    <input type="email" name="email" id="user-email">

**Screen reader (Firefox):** "Email, edit has auto-complete."

**Screen reader (Firefox, tabbing to input field):** "Email, edit has auto-complete blank."

**Screen reader (Chrome):** "Email, edit."

**Screen reader (Chrome, tabbing to input field):** "Email, edit blank."

<br>

    <input type="email" name="email">
    
**Screen reader (Firefox):** "Edit, has auto-complete."

**Screen reader (Firefox, tabbing to input field):** "Edit, has auto-complete blank."

**Screen reader (Chrome):** "Edit."

**Screen reader (Chrome, tabbing to input field):** "Edit blank."

<br><br>

## `file`

    <label for="selected-file">Choose a file:</label>
    <input type="file" name="file" id="selected-file">

**Screen reader (Firefox):** "Choose a file, grouping browse, button. No file selected. Out of grouping."

**Screen reader (Chrome):** "Choose a file, button."

**Example Note:** In Firefox, when navigating with arrow keys, the file name was announced in place of the "no file selected" text when a file was selected.

<br>

    <input type="file" name="file">

**Screen reader (Firefox):** "Browse button."

**Screen reader (Chrome):** "No file chosen, choose file button."

**Example Note:** In Firefox, when navigating with arrow keys, the file name was announced in place of the "no file selected" text when a file was selected.

In Chrome, the file name was announced in place of the "no file selected" text when a file was selected.

<br>

    <input type="file" name="files" multiple>
    
**Screen reader (Firefox):** "Browse button."

**Screen reader (Chrome):** "No file chosen, choose files button."

**Example Note:** In Firefox, when navigating with arrow keys, the file name (one file selected) or the number of files (more than one selected) was announced in place of the "no file selected" text when at least one file was selected

In Chrome, the file name (one file selected) or the number of files (more than one selected) was announced in place of the "no file selected" text when at least one file was selected.

<br><br>

    <label for="image-input">Submit</label>
    
    <input type="image" id="image-input" src="//unsplash.it/50" alt="submit image">

**Screen reader announces:**

<br>

    <input type="image" src="//unsplash.it/50" alt="submit">

**Screen reader announces:**

<br><br>

    <label for="selected-month">Choose a month:</label>
    <input type="month" name="month" id="selected-month">

**Screen reader announces:**

<br>

    <input type="month" name="month">

**Screen reader announces:**

<br><br>

    <label for="chosen-number">Choose a number:</label>
    <input type="number" name="number" id="chosen-number">

**Screen reader announces:**

<br>

    <input type="number" name="number">

**Screen reader announces:**

<br>

    <input type="number" name="number" min="5">

**Screen reader announces:**

<br><br>

    <label for="password">Password:</label>
    <input type="password" name="password" id="password">

**Screen reader announces:**

<br>

    <input type="password" name="password">

**Screen reader announces:**

<br><br>

    <label for="radio-one">One</label>
    <input type="radio" name="number" value="one" id="radio-one">

**Screen reader announces:**

<br>

    <input type="radio" name="number" value="two">

**Screen reader announces:**

<br><br>

    <label for="volume-range">Volume:</label>
    <input type="range" name="range" id="volume-range" min="0" max="100" value="50">

**Screen reader announces:**

<br>

    <input type="range" name="range" min="0" max="100" value="50">

**Screen reader announces:**

<br><br>

    <input type="reset" value="">

**Screen reader announces:**

<br>

    <input type="reset" value="Reset Form">

**Screen reader announces:**

<br><br>

    <label for="search-field">Search:</label>
    <input type="search" name="search" id="search-field">

**Screen reader announces:**

<br>

    <input type="search" name="search">

**Screen reader announces:**

<br><br>

    <input type="submit" value="">

**Screen reader announces:**

<br>

    <input type="submit" value="Submit Form">

**Screen reader announces:**

<br><br>

    <label for="phone-number">Phone:</label>
    <input type="tel" name="telephone" id="phone-number">

**Screen reader announces:**

<br>

    <input type="tel" name="telephone">

**Screen reader announces:**

<br><br>

    <input type="text">

**Screen reader announces:**

<br>

    <input type="text" maxlength="10">

**Screen reader announces:**

<br>

    <input type="text" name="first-name">

**Screen reader announces:**

<br>

    <input type="text" placeholder="Enter a name">

**Screen reader announces:**

<br>

    <input type="text" required>

**Screen reader announces:**

<br><br>

    <label for="selected-time">Time:</label>
    <input type="time" name="time" id="selected-time">

**Screen reader announces:**

<br>

    <input type="time" name="time">

**Screen reader announces:**

<br><br>

    <label for="entered-url">Enter a url:</label>
    <input type="url" name="url" id="entered-url">

**Screen reader announces:**

<br>

    <input type="url" name="url">

**Screen reader announces:**

<br><br>

    <label for="selected-week">Select a week:</label>
    <input type="week" name="week" id="selected-week">

**Screen reader announces:**

<br>

    <input type="week" name="week">

**Screen reader announces:**
