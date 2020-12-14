---
title: '<td>: The Table Data Cell element'
tags:
  - Cells
  - Data Cell
  - Element
  - HTML
  - HTML tabular data
  - Reference
  - Table Cell
  - Table Data
  - Tables
  - Web
  - cell
  - data
  - td
permalink: html/element/td
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td'
browserCompact: html.elements.td
---
{{ HTMLRef }}

The **HTML `<td>` element** defines a cell of a table that contains data. It participates in the _table model_.

{{ EmbedInteractiveExample("pages/tabbed/td.html","tabbed-taller") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | Sectioning root. |
| Permitted content | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content). |
| Tag omission | The start tag is mandatory.  
The end tag may be omitted, if it is immediately followed by a [`th`](/html/element/th/) or [`td`](/html/element/td/) element or if there are no more data in its parent element. |
| Permitted parents | A [`tr`](/html/element/tr/) element. |
| Implicit ARIA role | `[cell](/accessibility/aria/roles/cell_role)` if a descendant of a [`table`](/html/element/table/) element |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLTableDataCellElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("colspan") }}
: This attribute contains a non-negative integer value that indicates for how many columns the cell extends. Its default value is `1`. Values higher than 1000 will be considered as incorrect and will be set to the default value (1).

{{ htmlattrdef("headers") }}
: This attribute contains a list of space-separated strings, each corresponding to the **id** attribute of the [`th`](/html/element/th/) elements that apply to this element.

{{ htmlattrdef("rowspan") }}
: This attribute contains a non-negative integer value that indicates for how many rows the cell extends. Its default value is `1`; if its value is set to `0`, it extends until the end of the table section ([`thead`](/html/element/thead/), [`tbody`](/html/element/tbody/), [`tfoot`](/html/element/tfoot/), even if implicitly defined), that the cell belongs to. Values higher than 65534 are clipped down to 65534.

### Deprecated attributes

{{ htmlattrdef("abbr") }} {{ deprecated_inline }}
: This attribute contains a short abbreviated description of the cell's content. Some user-agents, such as speech readers, may present this description before the content itself.

**Note:** Do not use this attribute as it is obsolete in the latest standard. Alternatively, you can put the abbreviated description inside the cell and place the long content in the **title** attribute.

{{ htmlattrdef("align") }} {{ deprecated_inline }}
: This enumerated attribute specifies how the cell content's horizontal alignment will be handled. Possible values are:

-   `left`: The content is aligned to the left of the cell.
-   `center`: The content is centered in the cell.
-   `right`: The content is aligned to the right of the cell.
-   `justify` (with text only): The content is stretched out inside the cell so that it covers its entire width.
-   `char` (with text only): The content is aligned to a character inside the `<th>` element with minimal offset. This character is defined by the {{ htmlattrxref("char", "td") }} and {{ htmlattrxref("charoff", "td") }} attributes {{ unimplemented_inline(2212) }}.

The default value when this attribute is not specified is `left`.

**Note:**

-   To achieve the same effect as the `left`, `center`, `right` or `justify` values, apply the CSS {{ cssxref("text-align") }} property to the element.
-   To achieve the same effect as the `char` value, give the {{ cssxref("text-align") }} property the same value you would use for the {{ htmlattrxref("char", "td") }}. {{ unimplemented_inline }} in CSS3.

{{ htmlattrdef("axis") }} {{ deprecated_inline }}
: This attribute contains a list of space-separated strings. Each string is the `id` of a group of cells that this header applies to.

{{ htmlattrdef("bgcolor") }} {{ deprecated_inline }}
: This attribute defines the background color of each cell in a column. It is a [6-digit hexadecimal RGB code](/css/color_value#rgb_colors), prefixed by a '`#`'. One of the predefined [color kewords](/css/color_value#color_keywords) can also be used.

To achieve a similar effect, use the CSS {{ cssxref("background-color") }} property.

{{ htmlattrdef("char") }} {{ deprecated_inline }}
: The content in the cell element is aligned to a character. Typical values include a period (.) to align numbers or monetary values. If {{ htmlattrxref("align", "td") }} is not set to `char`, this attribute is ignored.

{{ htmlattrdef("charoff") }} {{ deprecated_inline }}
: This attribute is used to shift column data to the right of the character specified by the **char** attribute. Its value specifies the length of this shift.

{{ htmlattrdef("height") }} {{ deprecated_inline }}
: This attribute is used to define a recommended cell height. Use the CSS {{ cssxref("height") }} property instead.

{{ htmlattrdef("scope") }} {{ deprecated_inline }}
: This enumerated attribute defines the cells that the header (defined in the [`th`](/html/element/th/)) element relates to. Only use this attribute with the `<th>` element to define the row or column for which it is a header.

{{ htmlattrdef("valign") }} {{ deprecated_inline }}
: This attribute specifies how a text is vertically aligned inside a cell. Possible values for this attribute are:

-   `baseline`: Positions the text near the bottom of the cell and aligns it with the [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29) of the characters instead of the bottom. If characters don't descend below the baseline, the baseline value achieves the same effect as `bottom`.
-   `bottom`: Positions the text near the bottom of the cell.
-   `middle`: Centers the text in the cell.
-   and `top`: Positions the text near the top of the cell.

To achieve a similar effect, use the CSS {{ cssxref("vertical-align") }} property.

{{ htmlattrdef("width") }} {{ deprecated_inline }}
: This attribute is used to define a recommended cell width. Use the CSS {{ cssxref("width") }} property instead.

## Examples

See [`table`](/html/element/table/) for examples on `<td>`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'td element' in that specification](https://html.spec.whatwg.org/multipage/tables.html#the-td-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'td element' in that specification](https://www.w3.org/TR/html52/tabular-data.html#the-td-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.td") }}