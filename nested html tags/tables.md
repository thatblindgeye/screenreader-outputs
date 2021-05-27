# Tables

Screen reader users may be able to navigate tables with keyboard shortcuts specifically meant for navigating tables. This allows them to manually go to the next or previous cell in a row or column, and the screen reader will announce "edge of table" when a user reaches the last row or column in the table.

The use (or lack of use) of the `<colgroup>` tag did not seem to affect what the NVDA screen reader announced. It seems that using the tag may be more helpful for visual styling, so it has been omitted from these examples. See [MDN's page on the `<colgroup>` tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/colgroup) to see and edit their example (try moving the `class="batman"` attribute from the `<colgroup>` tag and placing it on one of the `<th>` or `<td>` tags).

W3.org has a great page regarding [table concepts](https://www.w3.org/WAI/tutorials/tables/), which goes into how to properly make an accessible table using various table formats.

## A Bad Table

    <table>
        <th>Day</th>
        <th>Hours</th>
        <td>Monday</td>
        <td>9:00 AM to 8:00 PM</td>
        <td>Wednesday</td>
        <td>8:00 AM to 10:00 PM</td>
        <td>Friday</td>
        <td>Closed</td>
    </table>
    
**Screen reader (Firefox - on page load):** "Table with one rows and eight columns. Row one column one day. Column two hours. Column three Monday. Column four nine AM to eight PM. Column five Wednesday. Column six eight AM to ten PM. Column seven Friday. Column eight closed. Out of table."

**Screen reader (Firefox - on page load):** "Table with one rows and eight columns. Days hours. Row one column one day. Column two hours. Column three Monday. Column four nine AM to eight PM. Column five Wednesday. Column six eight AM to ten PM. Column seven Friday. Column eight closed. Out of table."

**Example notes:** When manually navigating the table, the screen reader announced the column number followed by the contents of the new cell, e.g. "column two hours".

Keep in mind it might be difficult to understand the context of each cell's contents when laid out in a single row and several columns (or several rows and a single column).

<hr>

## Also a Bad Table

    <table>
        <tr>
            <td>Day</td>
            <td>Hours</td>
        </tr>
        <tr>
            <td>Monday</td>
            <td>9:00 AM to 8:00 PM</td>
        </tr>
        <tr>
            <td>Wednesday</td>
            <td>8:00 AM to 10:00 PM</td>
        </tr>
        <tr>
            <td>Friday</td>
            <td>Closed</td>
        </tr>
    </table>

**Screen reader (on page load):** "Day. Hours. Monday. Nine AM to eight PM. Wednesday. Eight AM to ten PM. Friday. Closed."

**Example notes:** The screen reader did not recognize this as a valid table to navigate due to the lack of `<th>` tags, which would defeat the purpose of using a `<table>` element.

<hr>

## A Simplistic Table with One Header

    <table>
        <tr>
            <th>Day</th>
            <th>Hours</th>
        </tr>
        <tr>
            <td>Monday</td>
            <td>9:00 AM to 8:00 PM</td>
        </tr>
        <tr>
            <td>Wednesday</td>
            <td>8:00 AM to 10:00 PM</td>
        </tr>
        <tr>
            <td>Friday</td>
            <td>Closed</td>
        </tr>
    </table>

**Screen reader (Firefox - on page load):** "Table with four rows and two columns. Row one column one day, column two hours. Row two day column one Monday, hours column two nine AM to eight PM. Row three day column one Wednesday, hours column two eight AM to ten PM. Row four day colunn one Friday, hours column two closed. Out of table"

**Screen reader (Chrome and Edge - on page load):** "Table with four rows and two columns. Row one day column one day, hours column two hours. Row two day column one Monday, hours column two nine AM to eight PM. Row three day column one Wednesday, hours column two eight AM to ten PM. Row four day colunn one Friday, hours column two closed. Out of table"

**Example notes:** When manually navigating to a different row, the screen reader announced the row number followed by the contents of the new cell, e.g. "row three Wednesday" or "row four Friday".

When manually navigating to a different column, the screen reader announced the column header and column number followed by the contents of the new cell, e.g. "day column one Monday" or "hours column two nine AM to eight PM".

<hr>

## A Simplistic Table with a Row and Column Header

    <table>
        <caption>Clothing Sold</caption>
        <thead>
            <tr>
                <td></td>
                <th scope="col">2020</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th scope="row">Shirts</th>
                <td>100</td>
            </tr>
            <tr>
                <th scope="row">Pants</th>
                <td>50</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <th scope="row">Total Sold</th>
                <td>150</td>
            </tr>
        </tfoot>
    </table>

**Screen reader (Firefox - on page load):** "Table with four rows and two columns. Caption clothing sold. Row one column one, column two twenty-twenty. Row two column one shirts, twenty-twenty column two one hundred. Row three column one pants, twenty-twenty column two fifty. Row four colunn one total sold, twenty-twenty column two one hundred and fifty. Out of table"

**Screen reader (Chrome and Edge - on page load):** "Table with four rows and two columns. Caption clothing sold. Row one column one twenty-twenty column two twenty-twenty. Shirts row two column one shirts, twenty-twenty column two one hundred. Pants row three column one pants, twenty-twenty column two fifty. Total sold row four colunn one total sold, twenty-twenty column two one hundred and fifty. Out of table"

**Example notes:** When manually navigating to a different row, the screen reader announced either the row number followed by the contents of the new cell (e.g. "row two shirts"), or the row header name and row number followed by the contents of the new cell (e.g. "shirts row two one-hundred").

When manually navigating to a different column, the screen reader announced either the column number followed by the contents of the new cell (e.g. "column one pants"), or the column header name and column number followed by the contents of the new cell (e.g. "twenty-twenty column two fifty").

<hr>

## Table with Irregular Headers

    <table>
        <thead>
            <tr>
                <td rowspan="2"></td>
                <th colspan="2" scope="colgroup">Mars</th>
                <th colspan="2" scope="colgroup">Venus</th>
              </tr>
              <tr>
                <th scope="col">Produced</th>
                <th scope="col">Sold</th>
                <th scope="col">Produced</th>
                <th scope="col">Sold</th>
              </tr>
        </thead>
        <tbody>
            <tr>
                <th scope="row">Teddy Bears</th>
                <td>50,000</td>
                <td>30,000</td>
                <td>100,000</td>
                <td>80,000</td>
              </tr>
              <tr>
                <th scope="row">Board Games</th>
                <td>10,000</td>
                <td>5,000</td>
                <td>12,000</td>
                <td>9,000</td>
              </tr>
        </tbody>
    </table>

**Screen reader (Firefox - on page load):** "Table with four rows and five columns. Row one through two, column one row one, column two through three Mars. Column four through five Venus. Row two Mars column two produced, Mars column three sold. Venus column four produced, Venus column five sold. Row three column one teddy bears. Produced Mars column two fifty-thousand, sold Mars column three thirty-thousand. Produced Venus column four one-hundred-thousand, sold Venus column five eighty-thousand. Row four column one board games. Produced Mars column two ten-thousand, sold Mars column three five-thousand. Produced Venus column four twelve-thousand, sold Venus column five nine-thousand. Out of table."

**Screen reader (Chrome and Edge - on page load):** "Table with four rows and five columns. Row one through two, column one row one, Mars produced column two through three Mars. Venus produced column four through five Venus. Row two Mars produced column one produced, Mars sold column two sold. Venus produced column three produced, Venus sold column four sold. Teddy bears row three column one teddy bears. Mars produced column two fifty-thousand, Mars sold column three thirty-thousand. Venus produced column four one-hundred-thousand, Venus sold column five eighty-thousand. Board games row four column one board games. Mars produced column two ten-thousand, Mars sold column three five-thousand. Venus produced column four twelve-thousand, Venus sold column five nine-thousand. Out of table."

**Example notes:** This example was taken from [Tables with irregular headers](https://www.w3.org/WAI/tutorials/tables/irregular/) on W3.org.

When manually navigating to a different row, the screen reader announced either the row number followed by the contents of the new cell (e.g. "row three teddy bears" or "row two produced") or the row header name and row number followed by the contents of the new cell (e.g. "teddy bears row three fifty-thousand").

When manually navigating to a different column, the screen reader announced either the column number followed by the contents of the new cell (e.g. "column one board games"), or the column subhead and header followed by the column number followed by the contents of the new cell (e.g. "produced mars column two ten-thousand").

<hr>

## Table with Multi-Level Headers
    <table>
        <caption>Room Availability</caption>
        <thead>
            <tr>
                <td></td>
                <th id="chalet" scope="col">Chalet</th>
                <th id="villa" scope="col">Villa</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th id="paris" scope="colgroup" colspan="3">Paris</th>
            </tr>
            <tr>
                <th id="parbed1" headers="paris">1 bedroom</th>
                <td headers="paris parbed1 chalet">25</td>
                <td headers="paris parbed1 villa">23</td>
            </tr>
            <tr>
                <th id="parbed2" headers="paris">2 bedroom</th>
                <td headers="paris parbed2 chalet">52</td>
                <td headers="paris parbed2 villa">32</td>
            </tr>
            <tr>
                <th id="rome" scope="colgroup" colspan="3">Rome</th>
            </tr>
            <tr>
                <th id="romebed1" headers="rome">1 bedroom</th>
                <td headers="rome romebed1 chalet">23</td>
                <td headers="rome romebed1 villa">3</td>
            </tr>
            <tr>
                <th id="romebed2" headers="rome">2 bedroom</th>
                <td headers="rome romebed2 chalet">43</td>
                <td headers="rome romebed2 villa">30</td>
            </tr>
        </tbody>
    </table>

**Screen reader (Firefox - on page load):** "Table with seven rows and three columns. Caption, room availability. Row one column one, column two chalet, column three villa. Row two column one through three Paris. Row three Paris column one one bedroom, Paris chalet column two twenty-five, Paris villa column three twenty-three. Row four Paris column one two bedroom, Paris chalet column two fifty-two, Paris villa column three thirty-two. Row five Paris column one through three Rome. Row six Rome column one one bedroom, Rome chalet column two twenty-three, Rome villa column three three. Row seven Rome column one two bedroom, Rome chalet column two forty-three, Rome villa column three thirty. Out of table."

**Screen reader (Firefox - on page load):** "Table with seven rows and three columns. Caption, room availability. Row one Paris Rome column one, chalet Paris Rome column two chalet, villa Paris Rome column three villa. Row two Paris Rome column one through three Paris. One bedroom row three Paris Rome column one one bedroom, chalet Paris Rome column two twenty-five, villa Paris Rome column three twenty-three. Two bedroom row four Paris Rome column one two bedroom, chalet Paris Rome column two fifty-two, villa Paris Rome column three thirty-two. Row five Paris Rome column one through three Rome. One bedroom row six Paris Rome column one one bedroom, chalet Paris Rome column two twenty-three, villa Paris Rome column three three. Two bedroom row seven Paris Rome column one two bedroom, chalet Paris Rome column two forty-three, villa Paris Rome column three thirty. Out of table."

**Example notes:** Using a table like this may cause issues with conveying the correct context to a screen reader. In Chrome and Edge, the screen reader announced "Paris Rome" instead of the correct heading. The W3.org page on [Tables with multi-level headers](https://www.w3.org/WAI/tutorials/tables/multi-level/) has this example along with a better alternative (example 3).

When manually navigating to a different row, the screen reader announced either the row number and column number followed by the contents of the new cell (e.g. "row two, column one through three, Paris"); the row number followed by the contents of the new cell (e.g. "row four, two bedroom"); the row number, header name, and column number followed by the contents of the new cell (e.g. "row three, Paris, column one, one bedroom"); or the header name and row number followed by the contents of the new cell (e.g. "two bedroom, row four, fifty-two").

When manually navigating to a different column, the screen reader announced the header name and column number followed by the contents of the new cell (e.g. "Paris, column one, two bedroom" or "Paris chalet, column two, fifty-two").
