# Tables

Screen reader users may be able to navigate tables with keyboard shortcuts specifically meant for navigating tables. This allows them to manually go to the next or previous cell in a row or column, and the screen reader will announce "edge of table" when a user reaches the last row or column in the table.

The use (or lack of use) of the `<colgroup>` tag did not seem to affect what the NVDA screen reader announced. It seems that using the tag may be more helpful for visual styling, so it has been omitted from these examples. See [MDN's page on the `<colgroup>` tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/colgroup) to see and edit their example (try moving the `class="batman"` attribute from the `<colgroup>` tag and placing it on one of the `<th>` or `<td>` tags).

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


