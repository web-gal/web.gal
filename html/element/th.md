---
title: <th>
tags:
  - Element
  - HTML
  - HTML tabular data
  - Heading Cell
  - Reference
  - Table Cell
  - Table Head
  - Table Header
  - Table Heading
  - Table Heading Cell
  - Tables
  - Web
  - cell
permalink: html/element/th
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th'
browserCompact: html.elements.th
---
{{ HTMLRef }}

The **HTML `<th>` element** defines a cell as header of a group of table cells. The exact nature of this group is defined by the {{ htmlattrxref("scope", "th") }} and {{ htmlattrxref("headers", "th") }} attributes.

{{ EmbedInteractiveExample("pages/tabbed/th.html","tabbed-taller") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | None. |
| Permitted content | [Flow content](/guide/html/content_categories#flow_content), but with no header, footer, sectioning content, or heading content descendants. |
| Tag omission | The start tag is mandatory.  
The end tag may be omitted, if it is immediately followed by a [`th`](/html/element/th/) or [`td`](/html/element/td/) element or if there are no more data in its parent element. |
| Permitted parents | A [`tr`](/html/element/tr/) element. |
| Implicit ARIA role | [`columnheader`](https://w3c.github.io/aria/#columnheader) or [`rowheader`](https://w3c.github.io/aria/#rowheader) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLTableHeaderCellElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("abbr") }}
: This attribute contains a short abbreviated description of the cell's content. Some user-agents, such as speech readers, may present this description before the content itself.

{{ htmlattrdef("colspan") }}
: This attribute contains a non-negative integer value that indicates for how many columns the cell extends. Its default value is `1`. Values higher than 1000 will be considered as incorrect and will be set to the default value (1).

{{ htmlattrdef("headers") }}
: This attribute contains a list of space-separated strings, each corresponding to the **id** attribute of the [`th`](/html/element/th/) elements that apply to this element.

{{ htmlattrdef("rowspan") }}
: This attribute contains a non-negative integer value that indicates for how many rows the cell extends. Its default value is `1`; if its value is set to `0`, it extends until the end of the table section ([`thead`](/html/element/thead/), [`tbody`](/html/element/tbody/), [`tfoot`](/html/element/tfoot/), even if implicitly defined), that the cell belongs to. Values higher than 65534 are clipped down to 65534.

{{ htmlattrdef("scope") }}
: This enumerated attribute defines the cells that the header (defined in the [`th`](/html/element/th/)) element relates to. It may have the following values:

-   `row`: The header relates to all cells of the row it belongs to.
-   `col`: The header relates to all cells of the column it belongs to.
-   `rowgroup`: The header belongs to a rowgroup and relates to all of its cells. These cells can be placed to the right or the left of the header, depending on the value of the `[dir](/html/global_attributes/dir)` attribute in the [`table`](/html/element/table/) element.
-   `colgroup`: The header belongs to a colgroup and relates to all of its cells.
-   `auto`

The default value when this attribute is not specified is `auto`.

### Deprecated attributes

{{ htmlattrdef("align") }} {{ obsolete_inline("html5") }}
: This enumerated attribute specifies how the cell content's horizontal alignment will be handled. Possible values are:

-   `left`: The content is aligned to the left of the cell.
-   `center`: The content is centered in the cell.
-   `right`: The content is aligned to the right of the cell.
-   `justify` (with text only): The content is stretched out inside the cell so that it covers its entire width.
-   `char` (with text only): The content is aligned to a character inside the `<th>` element with minimal offset. This character is defined by the {{ htmlattrxref("char", "th") }} and {{ htmlattrxref("charoff", "th") }} attributes.

The default value when this attribute is not specified is `left`.

**Note:** Do not use this attribute as it is obsolete in the latest standard.

-   To achieve the same effect as the `left`, `center`, `right` or `justify` values, apply the CSS {{ cssxref("text-align") }} property to the element.
-   To achieve the same effect as the `char` value, give the {{ cssxref("text-align") }} property the same value you would use for the {{ htmlattrxref("char", "th") }}. {{ unimplemented_inline }} in CSS3.

{{ htmlattrdef("axis") }} {{ obsolete_inline("html5") }}
: This attribute contains a list of space-separated strings. Each string is the `id` of a group of cells that this header applies to.

**Note:** Do not use this attribute as it is obsolete in the latest standard: use the {{ htmlattrxref("scope", "th") }} attribute instead.

{{ htmlattrdef("bgcolor") }} {{ Non-standard_inline }}
: This attribute defines the background color of each cell in a column. It consists of a 6-digit hexadecimal code as defined in [sRGB](https://www.w3.org/Graphics/Color/sRGB) and is prefixed by '#'. This attribute may be used with one of sixteen predefined color strings:

<table><tbody><tr><td style="background-color: black; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>black</code> = "#000000"</td><td style="background-color: green; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>green</code> = "#008000"</td></tr><tr><td style="background-color: silver; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>silver</code> = "#C0C0C0"</td><td style="background-color: lime; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>lime</code> = "#00FF00"</td></tr><tr><td style="background-color: gray; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>gray</code> = "#808080"</td><td style="background-color: olive; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>olive</code> = "#808000"</td></tr><tr><td style="background-color: white; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>white</code> = "#FFFFFF"</td><td style="background-color: yellow; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>yellow</code> = "#FFFF00"</td></tr><tr><td style="background-color: maroon; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>maroon</code> = "#800000"</td><td style="background-color: navy; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>navy</code> = "#000080"</td></tr><tr><td style="background-color: red; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>red</code> = "#FF0000"</td><td style="background-color: blue; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>blue</code> = "#0000FF"</td></tr><tr><td style="background-color: purple; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>purple</code> = "#800080"</td><td style="background-color: teal; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>teal</code> = "#008080"</td></tr><tr><td style="background-color: fuchsia; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>fuchsia</code> = "#FF00FF"</td><td style="background-color: aqua; width: 24px; height: 24px; border: 1px solid black;"></td><td><code>aqua</code> = "#00FFFF"</td></tr></tbody></table>

**Note:** Do not use this attribute, as it is non-standard and only implemented in some versions of Microsoft Internet Explorer: The [`th`](/html/element/th/) element should be styled using [CSS](/css). To create a similar effect use the {{ cssxref("background-color") }} property in [CSS](/css) instead.

{{ htmlattrdef("char") }} {{ obsolete_inline("html5") }}
: The content in the cell element is aligned to a character. Typical values include a period (.) to align numbers or monetary values. If {{ htmlattrxref("align", "th") }} is not set to `char`, this attribute is ignored.

**Note:** Do not use this attribute as it is obsolete in the latest standard. To achieve the same effect, you can specify the character as the first value of the {{ cssxref("text-align") }} property, {{ unimplemented_inline }} in CSS3.

{{ htmlattrdef("charoff") }} {{ obsolete_inline("html5") }}
: This attribute is used to shift column data to the right of the character specified by the **char** attribute. Its value specifies the length of this shift.

**Note:** Do not use this attribute as it is obsolete in the latest standard.

{{ htmlattrdef("height") }} {{ Deprecated_inline("html 4") }}, {{ obsolete_inline("html5") }}
: This attribute is used to define a recommended cell height.

**Note:** Do not use this attribute as it is obsolete in the latest standard: use the CSS {{ cssxref("height") }} property instead.

{{ htmlattrdef("valign") }} {{ obsolete_inline("html5") }}
: This attribute specifies how a text is vertically aligned inside a cell. Possible values for this attribute are:

-   `baseline`: Positions the text near the bottom of the cell and aligns it with the [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29) of the characters instead of the bottom. If characters don't descend below the baseline, the baseline value achieves the same effect as `bottom`.
-   `bottom`: Positions the text near the bottom of the cell.
-   `middle`: Centers the text in the cell.
-   and `top`: Positions the text near the top of the cell.

**Note:** Do not use this attribute as it is obsolete in the latest standard: use the CSS {{ cssxref("vertical-align") }} property instead.

{{ htmlattrdef("width") }} {{ Deprecated_inline("html 4") }}, {{ obsolete_inline("html5") }}
: This attribute is used to define a recommended cell width. Additional space can be added with the {{ domxref("HTMLTableElement.cellSpacing", "cellspacing") }} and {{ domxref("HTMLTableElement.cellPadding", "cellpadding") }} properties and the width of the [`col`](/html/element/col/) element can also create extra width. But, if a column's width is too narrow to show a particular cell properly, it will be widened when displayed.

**Note:** Do not use this attribute as it is obsolete in the latest standard: use the CSS {{ cssxref("width") }} property instead.

## Examples

See [`table`](/html/element/table/) for examples on `<th>`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'th element' in that specification](https://html.spec.whatwg.org/multipage/tables.html#the-th-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'th element' in that specification](https://www.w3.org/TR/html52/tabular-data.html#the-th-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.th") }}

## See also

-   Other table-related HTML Elements: [`caption`](/html/element/caption/), [`col`](/html/element/col/), [`colgroup`](/html/element/colgroup/), [`table`](/html/element/table/), [`tbody`](/html/element/tbody/), [`td`](/html/element/td/), [`tfoot`](/html/element/tfoot/), [`thead`](/html/element/thead/), [`tr`](/html/element/tr/).