# Lists

## `<ul>`

### Simple Unordered List

    <ul>
        <li>First Item</li>
        <li>Second Item</li>
        <li>Third Item</li>
    </ul>

**Screen reader:** "List with three items, bullet first item, bullet second item, bullet third item, out of list."

<br><br>

### Nested Unordered List

    <ul>
        <li>First Item</li>
        <li>Second Item</li>
        <ul>
            <li>Subitem A</li>
        </ul>
        <li>Third Item</li>
    </ul>

**Screen reader:** "List with four items, bullet first item, bullet second item, list with one items white bullet subitem a, out of list, bullet third item, out of list."

<br>

**Notes:** The screen reader may announce the list-style-type marker. Using "circle" as the list-style-type caused the screen reader to announce "white circle", and using "none" caused no announcement of any marker.

<br>
<hr>
<br>

## `<ol>`

### Simple Ordered List

    <ol>
        <li>First Item</li>
        <li>Second Item</li>
        <li>Third Item</li>
    </ol>

**Screen reader:** "List with three items, one first item, two second item, three third item, out of list."

<br>
<hr>
<br>

## `<dl>`

### Simple Description List

    <dl>
        <dt>First Item</dt>
        <dd>The first item in the list</dd>
        <dt>Second Item</dt>
        <dd>The second item in the list</dd>
        <dt>Third Item</dt>
        <dd>The third item in the list</dd>
    </dl>

**Screen reader:** "List with six items, first item, the first item in the list, second item, the second item in the list, third item, the third item in the list, out of list."
