---
title: '<thead>: The Table Head element'
tags:
  - Element
  - HTML
  - HTML tabular data
  - Reference
  - Tables
  - Web
permalink: html/element/thead
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead'
browserCompact: html.elements.thead
---
{{ HTMLRef }}

The **HTML `<thead>` element** defines a set of rows defining the head of the columns of the table.

{{ EmbedInteractiveExample("pages/tabbed/thead.html","tabbed-taller") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | None. |
| Permitted content | Zero or more [`tr`](/html/element/tr/) elements. |
| Tag omission | The start tag is mandatory. The end tag may be omitted if the [`thead`](/html/element/thead/) element is immediately followed by a [`tbody`](/html/element/tbody/) or [`tfoot`](/html/element/tfoot/) element. |
| Permitted parents | A [`table`](/html/element/table/) element. The [`thead`](/html/element/thead/) must appear after any [`caption`](/html/element/caption/) or [`colgroup`](/html/element/colgroup/) element, even implicitly defined, but before any [`tbody`](/html/element/tbody/), [`tfoot`](/html/element/tfoot/) and [`tr`](/html/element/tr/) element. |
| Implicit ARIA role | `[rowgroup](/accessibility/aria/roles/rowgroup_role)` |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLTableSectionElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

### Deprecated attributes

{{ htmlattrdef("align") }} {{ Deprecated_inline }} in {{ HTMLVersionInline("4") }}, {{ obsolete_inline }} in {{ HTMLVersionInline("5") }}
: This enumerated attribute specifies how horizontal alignment of each cell content will be handled. Possible values are:

-   `left`, aligning the content to the left of the cell
-   `center`, centering the content in the cell
-   `right`, aligning the content to the right of the cell
-   `justify`, inserting spaces into the textual content so that the content is justified in the cell
-   `char`, aligning the textual content on a special character with a minimal offset, defined by the {{ htmlattrxref("char", "thead") }} and {{ htmlattrxref("charoff", "thead") }} attributes {{ unimplemented_inline("2212") }}.

If this attribute is not set, the `left` value is assumed.

**Note:** Do not use this attribute as it is obsolete (not supported) in the latest standard.

-   To achieve the same effect as the `left`, `center`, `right` or `justify` values, use the CSS {{ cssxref("text-align") }} property on it.
-   To achieve the same effect as the `char` value, in CSS3, you can use the value of the {{ htmlattrxref("char", "thead") }} as the value of the {{ cssxref("text-align") }} property {{ unimplemented_inline }}.

{{ htmlattrdef("bgcolor") }} {{ Non-standard_inline }}
: This attribute defines the background color of each cell of the column. It is one of the 6-digit hexadecimal code as defined in [sRGB](https://www.w3.org/Graphics/Color/sRGB), prefixed by a '#'. One of the sixteen predefined color strings may be used:

<table style="width: 80%;"><tbody><tr><td style="background-color: black; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>black</code> = "#000000"</td><td style="background-color: green; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>green</code> = "#008000"</td></tr><tr><td style="background-color: silver; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>silver</code> = "#C0C0C0"</td><td style="background-color: lime; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>lime</code> = "#00FF00"</td></tr><tr><td style="background-color: gray; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>gray</code> = "#808080"</td><td style="background-color: olive; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>olive</code> = "#808000"</td></tr><tr><td style="background-color: white; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>white</code> = "#FFFFFF"</td><td style="background-color: yellow; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>yellow</code> = "#FFFF00"</td></tr><tr><td style="background-color: maroon; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>maroon</code> = "#800000"</td><td style="background-color: navy; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>navy</code> = "#000080"</td></tr><tr><td style="background-color: red; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>red</code> = "#FF0000"</td><td style="background-color: blue; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>blue</code> = "#0000FF"</td></tr><tr><td style="background-color: purple; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>purple</code> = "#800080"</td><td style="background-color: teal; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>teal</code> = "#008080"</td></tr><tr><td style="background-color: fuchsia; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>fuchsia</code> = "#FF00FF"</td><td style="background-color: aqua; width: 24px; height: 24px; border-width: 1px; border-color: black; border-style: solid;"></td><td><code>aqua</code> = "#00FFFF"</td></tr></tbody></table>

**Usage note:** Do not use this attribute, as it is non-standard and only implemented in some versions of Microsoft Internet Explorer: the [`thead`](/html/element/thead/) element should be styled using [CSS](/css). To give a similar effect to the **bgcolor** attribute, use the [CSS](/css) property {{ cssxref("background-color") }}, on the relevant [`td`](/html/element/td/) or [`th`](/html/element/th/) elements.

{{ htmlattrdef("char") }} {{ Deprecated_inline }} in {{ HTMLVersionInline("4") }}, {{ obsolete_inline }} in {{ HTMLVersionInline("5") }}
: This attribute is used to set the character to align the cells in a column on. Typical values for this include a period (.) when attempting to align numbers or monetary values. If {{ htmlattrxref("align", "thead") }} is not set to `char`, this attribute is ignored.

**Note:** Do not use this attribute as it is obsolete (and not supported) in the latest standard. To achieve the same effect as the {{ htmlattrxref("char", "thead") }}, in CSS3, you can use the character set using the {{ htmlattrxref("char", "thead") }} attribute as the value of the {{ cssxref("text-align") }} property {{ unimplemented_inline }}.

{{ htmlattrdef("charoff") }} {{ Deprecated_inline }} in {{ HTMLVersionInline("4") }}, {{ obsolete_inline }} in {{ HTMLVersionInline("5") }}
: This attribute is used to indicate the number of characters to offset the column data from the alignment characters specified by the **char** attribute.

**Note:** Do not use this attribute as it is obsolete (and not supported) in the latest standard.

{{ htmlattrdef("valign") }} {{ Deprecated_inline }} in {{ HTMLVersionInline("4") }}, {{ obsolete_inline }} in {{ HTMLVersionInline("5") }}
: This attribute specifies the vertical alignment of the text within each row of cells of the table header. Possible values for this attribute are:

-   `baseline`, which will put the text as close to the bottom of the cell as it is possible, but align it on the [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29) of the characters instead of the bottom of them. If characters are all of the size, this has the same effect as `bottom`.
-   `bottom`, which will put the text as close to the bottom of the cell as it is possible;
-   `middle`, which will center the text in the cell;
-   `top`, which will put the text as close to the top of the cell as it is possible.

**Note:** Do not use this attribute as it is obsolete (and not supported) in the latest standard: instead set the CSS {{ cssxref("vertical-align") }} property on it.

## Examples

See [`table`](/html/element/table/) for examples on `<thead>`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'thead element' in that specification](https://html.spec.whatwg.org/multipage/tables.html#the-thead-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'thead element' in that specification](https://www.w3.org/TR/html52/tabular-data.html#the-thead-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.thead") }}

## See also

-   Other table-related HTML Elements: [`caption`](/html/element/caption/), [`col`](/html/element/col/), [`colgroup`](/html/element/colgroup/), [`table`](/html/element/table/), [`tbody`](/html/element/tbody/), [`td`](/html/element/td/), [`tfoot`](/html/element/tfoot/), [`th`](/html/element/th/), [`tr`](/html/element/tr/);
-   CSS properties and pseudo-classes that may be specially useful to style the `<thead>` element:
    -   the {{ cssxref(":nth-child") }} pseudo-class to set the alignment on the cells of the column;
    -   the {{ cssxref("text-align") }} property to align all cells content on the same character, like '.'.