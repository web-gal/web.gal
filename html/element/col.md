---
title: <col>
tags:
  - Element
  - HTML
  - HTML tabular data
  - Reference
  - Tables
  - Web
permalink: html/element/col
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/col'
browserCompact: html.elements.col
---
{{ HTMLRef }}

The **HTML `<col>` element** defines a column within a table and is used for defining common semantics on all common cells. It is generally found within a [`colgroup`](/html/element/colgroup/) element.

{{ EmbedInteractiveExample("pages/tabbed/col.html","tabbed-taller") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

`<col>` allows styling columns using CSS, but only a few properties will have an effect on the column ([see the CSS 2.1 specification](https://www.w3.org/TR/CSS21/tables.html#columns) for a list).

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | It must have start tag, but must not have an end tag. |
| Permitted parents | [`colgroup`](/html/element/colgroup/) only, though it can be implicitly defined as its start tag is not mandatory. The [`colgroup`](/html/element/colgroup/) must not have a {{ htmlattrxref("span", "colgroup") }} attribute. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLTableColElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("span") }}
: This attribute contains a positive integer indicating the number of consecutive columns the `<col>` element spans. If not present, its default value is `1`.

### Deprecated attributes

The following attributes are deprecated and should not be used. They are documented below for reference when updating existing code and for historical interest only.

{{ htmlattrdef("align") }} {{ deprecated_inline }}
: This enumerated attribute specifies how horizontal alignment of each column cell content will be handled. Possible values are:

-   `left`, aligning the content to the left of the cell
-   `center`, centering the content in the cell
-   `right`, aligning the content to the right of the cell
-   `justify`, inserting spaces into the textual content so that the content is justified in the cell

If this attribute is not set, its value is inherited from the {{ htmlattrxref("align", "colgroup") }} of the [`colgroup`](/html/element/colgroup/) element this `<col>` element belongs too. If there are none, the `left` value is assumed.

**Note:**

-   To achieve the same effect as the `left`, `center`, `right` or `justify` values:
    -   Do not try to set the {{ cssxref("text-align") }} property on a selector giving a `<col>` element. Because [`td`](/html/element/td/) elements are not descendant of the `<col>` element, they won't inherit it.
    -   If the table doesn't use a {{ htmlattrxref("colspan", "td") }} attribute, use the `td:nth-child(an+b)` CSS selector. Set `a` to zero and `b` to the position of the column in the table, e.g. `td:nth-child(2) { text-align: right; }` to right-align the second column.
    -   If the table does use a {{ htmlattrxref("colspan", "td") }} attribute, the effect can be achieved by combining adequate CSS attribute selectors like `[colspan=n]`, though this is not trivial.

{{ htmlattrdef("bgcolor") }} {{ Deprecated_inline }}
: The background color of the table. It is a [6-digit hexadecimal RGB code](/css/color_value#rgb_colors), prefixed by a '`#`'. One of the predefined [color kewords](/css/color_value#color_keywords) can also be used.

To achieve a similar effect, use the CSS {{ cssxref("background-color") }} property.

{{ htmlattrdef("char") }} {{ deprecated_inline }}
: This attribute is used to set the character to align the cells in a column on. Typical values for this include a period (.) when attempting to align numbers or monetary values. If {{ htmlattrxref("align", "col") }} is not set to `char`, this attribute is ignored.

{{ htmlattrdef("charoff") }} {{ deprecated_inline }}
: This attribute is used to indicate the number of characters to offset the column data from the alignment characters specified by the `char` attribute.

{{ htmlattrdef("valign") }} {{ deprecated_inline }}
: This attribute specifies the vertical alignment of the text within each cell of the column. Possible values for this attribute are:

-   `baseline`, which will put the text as close to the bottom of the cell as it is possible, but align it on the [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29) of the characters instead of the bottom of them. If characters are all of the size, this has the same effect as `bottom`.
-   `bottom`, which will put the text as close to the bottom of the cell as it is possible;
-   `middle`, which will center the text in the cell;
-   and `top`, which will put the text as close to the top of the cell as it is possible.

**Note:**

-   Do not try to set the {{ cssxref("vertical-align") }} property on a selector giving a `<col>` element. Because [`td`](/html/element/td/) elements are not descendant of the `<col>` element, they won't inherit it.
-   If the table doesn't use a {{ htmlattrxref("colspan", "td") }} attribute, use the `td:nth-child(an+b)` CSS selector where a is the total number of the columns in the table and b is the ordinal position of the column in the table. Only after this selector the `vertical-align` property can be used.
-   If the table does use a {{ htmlattrxref("colspan", "td") }} attribute, the effect can be achieved by combining adequate CSS attribute selectors like `[colspan=n]`, though this is not trivial.

{{ htmlattrdef("width") }} {{ deprecated_inline }}
: This attribute specifies a default width for each column in the current column group. In addition to the standard pixel and percentage values, this attribute might take the special form `0*`, which means that the width of each column in the group should be the minimum width necessary to hold the column's contents. Relative widths such as `5*` also can be used.

## Examples

Please see the [`table`](/html/element/table/) page for examples on `<col>`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<col>' in that specification](https://html.spec.whatwg.org/multipage/tables.html#the-col-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<col>' in that specification](https://www.w3.org/TR/html52/tabular-data.html#the-col-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<col>' in that specification](https://www.w3.org/TR/html401/struct/tables.html#h-11.2.4.2) | {{ Spec2('HTML4.01') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.col") }}

## See also

-   CSS properties and pseudo-classes that may be specially useful to style the `<col>` element:
    -   the {{ cssxref("width") }} property to control the width of the column;
    -   the {{ cssxref(":nth-child") }} pseudo-class to set the alignment on the cells of the column;
    -   the {{ cssxref("text-align") }} property to align all cells content on the same character, like '.'.