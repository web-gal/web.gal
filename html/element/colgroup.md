---
title: <colgroup>
tags:
  - Element
  - HTML
  - HTML tabular data
  - Reference
  - Tables
  - Web
permalink: html/element/colgroup
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/colgroup'
browserCompact: html.elements.colgroup
---
{{ HTMLRef }}

The **HTML `<colgroup>` element** defines a group of columns within a table.

{{ EmbedInteractiveExample("pages/tabbed/colgroup.html","tabbed-taller") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | If the {{ htmlattrxref("span", "colgroup") }} attribute is present: none, it is an [empty element](/glossary/empty_element/).  
If the attribute is not present: zero or more [`col`](/html/element/col/) element |
| Tag omission | The start tag may be omitted, if it has a [`col`](/html/element/col/) element as its first child and if it is not preceded by a [`colgroup`](/html/element/colgroup/) whose end tag has been omitted.  
The end tag may be omitted, if it is not followed by a space or a comment. |
| Permitted parents | A [`table`](/html/element/table/) element. The [`colgroup`](/html/element/colgroup/) must appear after any optional [`caption`](/html/element/caption/) element but before any [`thead`](/html/element/thead/), [`th`](/html/element/th/), [`tbody`](/html/element/tbody/), [`tfoot`](/html/element/tfoot/) and [`tr`](/html/element/tr/) element. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLTableColElement") }} |

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

{{ htmlattrdef("span") }}
: This attribute contains a positive integer indicating the number of consecutive columns the `<colgroup>` element spans. If not present, its default value is `1`.

**Note:** This attribute is applied on the attributes of the column group, it has no effect on the CSS styling rules associated with it or, even more, to the cells of the column's members of the group.

-   The `span` attribute is not permitted if there are one or more `<col>` elements within the `<colgroup>`.

### Deprecated attributes

The following attributes are deprecated and should not be used. They are documented below for reference when updating existing code and for historical interest only.

{{ htmlattrdef("align") }} {{ deprecated_inline }}
: This enumerated attribute specifies how horizontal alignment of each column cell content will be handled. Possible values are:

-   `left`, aligning the content to the left of the cell
-   `center`, centering the content in the cell
-   `right`, aligning the content to the right of the cell
-   `justify`, inserting spaces into the textual content so that the content is justified in the cell
-   `char`, aligning the textual content on a special character with a minimal offset, defined by the {{ htmlattrxref("char", "col") }} and {{ htmlattrxref("charoff", "col") }} attributes.

If this attribute is not set, the `left` value is assumed. The descendant [`col`](/html/element/col/) elements may override this value using their own {{ htmlattrxref("align", "col") }} attribute.

**Note:**

-   Do not try to set the {{ cssxref("text-align") }} property on a selector giving a [`colgroup`](/html/element/colgroup/) element. Because [`td`](/html/element/td/) elements are not descendant of the [`colgroup`](/html/element/colgroup/) element, they won't inherit it.
-   If the table doesn't use a {{ htmlattrxref("colspan", "td") }} attribute, use one `td:nth-child(an+b)` CSS selector per column, where a is the total number of the columns in the table and b is the ordinal position of this column in the table. Only after this selector the `text-align` property can be used.
-   If the table does use a {{ htmlattrxref("colspan", "td") }} attribute, the effect can be achieved by combining adequate CSS attribute selectors like `[colspan=n]`, though this is not trivial.

{{ htmlattrdef("bgcolor") }} {{ Deprecated_inline }}
: The background color of the table. It is a [6-digit hexadecimal RGB code](/css/color_value#rgb_colors), prefixed by a '`#`'. One of the predefined [color kewords](/css/color_value#color_keywords) can also be used.

To achieve a similar effect, use the CSS {{ cssxref("background-color") }} property.

{{ htmlattrdef("char") }} {{ deprecated_inline }}
: This attribute specifies the alignment of the content in a column group to a character. Typical values for this include a period (.) when attempting to align numbers or monetary values. If {{ htmlattrxref("align", "colgroup") }} is not set to `char`, this attribute is ignored, though it will still be used as the default value for the {{ htmlattrxref("align", "col") }} of the [`col`](/html/element/col/) which are members of this column group.

{{ htmlattrdef("charoff") }} {{ deprecated_inline }}
: This attribute is used to indicate the number of characters to offset the column data from the alignment character specified by the `char` attribute.

{{ htmlattrdef("valign") }} {{ deprecated_inline }}
: This attribute specifies the vertical alignment of the text within each cell of the column. Possible values for this attribute are:

-   `baseline`, which will put the text as close to the bottom of the cell as it is possible, but align it on the [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29) of the characters instead of the bottom of them. If characters are all of the size, this has the same effect as `bottom`.
-   `bottom`, which will put the text as close to the bottom of the cell as it is possible;
-   `middle`, which will center the text in the cell;
-   and `top`, which will put the text as close to the top of the cell as it is possible.

**Note:**

-   Do not try to set the {{ cssxref("vertical-align") }} property on a selector giving a `<colgroup>` element. Because [`td`](/html/element/td/) elements are not descendant of the `<colgroup>` element, they won't inherit it.
-   If the table doesn't use a {{ htmlattrxref("colspan", "td") }} attribute, use the `td:nth-child(an+b)` CSS selector per column, where a is the total number of the columns in the table and b is the ordinal position of the column in the table. Only after this selector the `vertical-align` property can be used.
-   If the table does use a {{ htmlattrxref("colspan", "td") }} attribute, the effect can be achieved by combining adequate CSS attribute selectors like `[colspan=n]`, though this is not trivial.

## Examples

Please see the [`table`](/html/element/table/) page for examples on `<colgroup>`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<colgroup>' in that specification](https://html.spec.whatwg.org/multipage/tables.html#the-colgroup-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<colgroup>' in that specification](https://www.w3.org/TR/html52/tabular-data.html#the-colgroup-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<colgroup>' in that specification](https://www.w3.org/TR/html401/tables.html#edef-COLGROUP) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.colgroup") }}

## See also

-   CSS properties and [pseudo-classes](/css/pseudo-classes) that may be specially useful to style the `<col>` element:
    -   the {{ cssxref("width") }} property to control the width of the column;
    -   the {{ cssxref(":nth-child") }} pseudo-class to set the alignment on the cells of the column;
    -   the {{ cssxref("text-align") }} property to align all cells content on the same character, like '.'.