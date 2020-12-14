---
title: '<tbody>: The Table Body element'
tags:
  - Element
  - HTML
  - HTML tabular data
  - Reference
  - Table Body
  - Table Contents
  - Tables
  - Web
  - tbody
permalink: html/element/tbody
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody'
browserCompact: html.elements.tbody
---
{{ HTMLRef }}

The **HTML Table Body element** (**`<tbody>`**) encapsulates a set of table rows ([`tr`](/html/element/tr/) elements), indicating that they comprise the body of the table ([`table`](/html/element/table/)).

{{ EmbedInteractiveExample("pages/tabbed/tbody.html","tabbed-taller") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

The `<tbody>` element, along with its cousins [`thead`](/html/element/thead/) and [`tfoot`](/html/element/tfoot/), provide useful semantic information that can be used when rendering for either screen or printer as well as for [accessibility](/glossary/accessibility/) purposes.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | Zero or more [`tr`](/html/element/tr/) elements. |
| Tag omission | The `<tbody>` element is not a required child element for a parent [`table`](/html/element/table/) element to graphically render. However, it must not be present, if its parent [`table`](/html/element/table/) element has a [`tr`](/html/element/tr/) element as a child. |
| Permitted parents | Within the required parent [`table`](/html/element/table/) element, the `<tbody>` element can be added after a [`caption`](/html/element/caption/), [`colgroup`](/html/element/colgroup/), and a [`thead`](/html/element/thead/) element. |
| Implicit ARIA role | `[rowgroup](/accessibility/aria/roles/rowgroup_role)` |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLTableSectionElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

### Deprecated attributes

{{ htmlattrdef("align")  }} {{ deprecated_inline }}
: This enumerated attribute specifies how horizontal alignment of each cell content will be handled. Possible values are:

-   `left`, aligning the content to the left of the cell
-   `center`, centering the content in the cell
-   `right`, aligning the content to the right of the cell
-   `justify`, inserting spaces into the textual content so that the content is justified in the cell
-   `char`, aligning the textual content on a special character with a minimal offset, defined by the {{ htmlattrxref("char", "tbody")  }} and {{ htmlattrxref("charoff", "tbody")  }} attributes.

If this attribute is not set, the `left` value is assumed.

As this attribute is deprecated, use the CSS {{ cssxref("text-align") }} property instead.

**Note:** The equivalent `text-align` property for the `align="char"` is not implemented in any browsers yet. See the [`text-align`'s browser compatibility section](/css/text-align#browser_compatibility) for the `<string>` value.

{{ htmlattrdef("bgcolor") }} {{ Deprecated_inline }}
: The background color of the table. It is a [6-digit hexadecimal RGB code](/css/color_value#rgb_colors), prefixed by a '`#`'. One of the predefined [color kewords](/css/color_value#color_keywords) can also be used.

As this attribute is deprecated, use the CSS {{ cssxref("background-color") }} property instead.

{{ htmlattrdef("char")  }} {{ deprecated_inline }}
: This attribute is used to set the character to align the cells in a column on. Typical values for this include a period (`.`) when attempting to align numbers or monetary values. If {{ htmlattrxref("align", "tbody") }} is not set to `char`, this attribute is ignored.

{{ htmlattrdef("charoff")  }} {{ deprecated_inline }}
: This attribute is used to indicate the number of characters to offset the column data from the alignment characters specified by the `char` attribute.

{{ htmlattrdef("valign")  }} {{ deprecated_inline }}
: This attribute specifies the vertical alignment of the text within each row of cells of the table header. Possible values for this attribute are:

-   `baseline`, which will put the text as close to the bottom of the cell as it is possible, but align it on the [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29) of the characters instead of the bottom of them. If characters are all of the size, this has the same effect as `bottom`.
-   `bottom`, which will put the text as close to the bottom of the cell as it is possible;
-   `middle`, which will center the text in the cell;
-   and `top`, which will put the text as close to the top of the cell as it is possible.

As this attribute is deprecated, use the CSS {{ cssxref("vertical-align") }} property instead.

## Usage notes

-   If the table includes a [`thead`](/html/element/thead/) block (to semantically identify header rows), the `<tbody>` block _must_ come after it.
-   If you use `<tbody>`, you can't also have table rows ([`tr`](/html/element/tr/) elements) which are direct children of the [`table`](/html/element/table/) but not included inside the `<tbody>`. All non-header and non-footer rows must be inside the `<tbody>` if one is used.
-   When printing a document, the `<thead>` and [`tfoot`](/html/element/tfoot/) elements specify information that may be the same—or at least very similar—on every page of a multi-page table, while the `<tbody>` element's contents generally will differ from page to page.
-   When a table is presented in a screen context (such as a window) which is not large enough to display the entire table, the [user agent](/glossary/user_agent/) may let the user scroll the contents of the `<thead>`, `<tbody>`, `<tfoot>`, and [`caption`](/html/element/caption/) blocks separately from one another for the same parent table.
-   You _may_ use more than one `<tbody>` per table as long as they are all consecutive. This lets you divide the rows in large tables into sections, each of which may be separately formatted if so desired.

## Examples

Below are some examples showing the use of the `<tbody>` element. For more examples of this tag in use, see the examples for [`table`](/html/element/table/).

### Basic example

In this relatively simple example, we create a table listing information about a group of students with a [`thead`](/html/element/thead/) and a [`tbody`](/html/element/tbody/), with a number of rows in the body.

#### HTML

The table's HTML is shown here. Note that all of the body cells including information about students are contained within a single `<tbody>` element.

```html
<table>
  <thead>
    <tr>
      <th>Student ID</th>
      <th>Name</th>
      <th>Major</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3741255</td>
      <td>Jones, Martha</td>
      <td>Computer Science</td>
    </tr>
    <tr>
      <td>3971244</td>
      <td>Nim, Victor</td>
      <td>Russian Literature</td>
    </tr>
    <tr>
      <td>4100332</td>
      <td>Petrov, Alexandra</td>
      <td>Astrophysics</td>
    </tr>
  </tbody>
</table>
```

#### CSS

The CSS to style our table is shown next.

```css
table {
  border: 2px solid #555;
  border-collapse: collapse;
  font: 16px "Lucida Grande", "Helvetica", "Arial", sans-serif;
}
```

First, the table's overall style attributes are set, configuring the thickness, style, and color of the table's exterior borders and using {{ cssxref("border-collapse") }} to ensure that the border lines are shared among adjacent cells rather than each having its own borders with space in between. {{ cssxref("font") }} is used to establish an initial font for the table.

```css
th, td {
  border: 1px solid #bbb;
  padding: 2px 8px 0;
  text-align: left;
}
```

Then the style is set for the majority of the cells in the table, including all data cells but also those styles shared between our [`td`](/html/element/td/) and [`th`](/html/element/th/) cells. The cells are given a light gray outline which is a single pixel thick, padding is adjusted, and all cells are left-aligned using {{ cssxref("text-align") }}

```css
thead > tr > th {
  background-color: #cce;
  font-size: 18px;
  border-bottom: 2px solid #999;
}
```

Finally, header cells contained within the [`thead`](/html/element/thead/) block are given additional styling. They use a darker {{ cssxref("background-color") }}, a larger font size, and a thicker, darker bottom border than the other cell borders.

#### Result

The resulting table looks like this:

{{ EmbedLiveSample("Basic_example", 650, 150) }}

### Multiple bodies

You can create multiple sections within a table by using multiple `<tbody>` elements. Each may potentially have its own header row or rows; however, _there can be only one [`thead`](/html/element/thead/) per table!_ Because of that, you need to use a [`tr`](/html/element/tr/) filled with [`th`](/html/element/th/) elements to create headers within each `<tbody>`. Let's see how that's done.

Let's take the previous example, add some more students to the list, and update the table so that instead of listing each student's major on every row, the students are grouped by major, with heading rows for each major.

#### Result

First, the resulting table, so you know what we're building:

{{ EmbedLiveSample("Multiple_bodies", 650, 250) }}

#### HTML

The revised HTML looks like this:

```html
<table>
  <thead>
    <tr>
      <th>Student ID</th>
      <th>Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th colspan="2">Computer Science</th>
    </tr>
    <tr>
      <td>3741255</td>
      <td>Jones, Martha</td>
    </tr>
    <tr>
      <td>4077830</td>
      <td>Pierce, Benjamin</td>
    </tr>
    <tr>
      <td>5151701</td>
      <td>Kirk, James</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th colspan="2">Russian Literature</th>
    </tr>
    <tr>
      <td>3971244</td>
      <td>Nim, Victor</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th colspan="2">Astrophysics</th>
    </tr>
    <tr>
      <td>4100332</td>
      <td>Petrov, Alexandra</td>
    </tr>
    <tr>
      <td>8892377</td>
      <td>Toyota, Hiroko</td>
    </tr>
  </tbody>
</table>
```

Notice that each major is placed in a separate `<tbody>` block, the first row of which contains a single [`th`](/html/element/th/) element with a {{ htmlattrxref("colspan", "th") }} attribute that spans the entire width of the table. That heading lists the name of the major contained within the `<tbody>`.

Then each remaining row in each major's `<tbody>` consists of two cells: the first for the student's ID and the second for their name.

#### CSS

```css
table {
  border: 2px solid #555;
  border-collapse: collapse;
  font: 16px "Lucida Grande", "Helvetica", "Arial", sans-serif;
}

th, td {
  border: 1px solid #bbb;
  padding: 2px 8px 0;
  text-align: left;
}

thead > tr > th {
  background-color: #cce;
  font-size: 18px;
  border-bottom: 2px solid #999;
}
```

Most of the CSS is unchanged. We do, however, add a slightly more subtle style for header cells contained directly within a `<tbody>` (as opposed to those which reside in a [`thead`](/html/element/thead/)). This is used for the headers indicating each table section's corresponding major.

```css
tbody > tr > th {
  background-color: #dde;
  border-bottom: 1.5px solid #bbb;
  font-weight: normal;
}
```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'tbody element' in that specification](https://html.spec.whatwg.org/multipage/tables.html#the-tbody-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'tbody element' in that specification](https://www.w3.org/TR/html52/tabular-data.html#the-tbody-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.tbody") }}

## See also

-   CSS properties and [pseudo-classes](/css/pseudo-classes) that may be specially useful to style the `<tbody>` element:
    -   the {{ cssxref(":nth-child")  }} pseudo-class to set the alignment on the cells of the column;
    -   the {{ cssxref("text-align")  }} property to align all cells content on the same character, like '.'.