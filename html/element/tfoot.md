---
title: '<tfoot>: The Table Foot element'
tags:
  - Element
  - HTML
  - HTML tabular data
  - Reference
  - Tables
  - Web
permalink: html/element/tfoot
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tfoot'
browserCompact: html.elements.tfoot
---
{{ HTMLRef }}

The **HTML `<tfoot>` element** defines a set of rows summarizing the columns of the table.

{{ EmbedInteractiveExample("pages/tabbed/tfoot.html","tabbed-taller") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | None. |
| Permitted content | Zero or more [`tr`](/html/element/tr/) elements. |
| Tag omission | The start tag is mandatory. The end tag may be omitted if there is no more content in the parent [`table`](/html/element/table/) element. |
| Permitted parents | A [`table`](/html/element/table/) element. The [`tfoot`](/html/element/tfoot/) must appear after any [`caption`](/html/element/caption/), [`colgroup`](/html/element/colgroup/), [`thead`](/html/element/thead/), [`tbody`](/html/element/tbody/), or [`tr`](/html/element/tr/) element. Note that this is the requirement as of HTML5.  
{{ HTMLVersionInline("4") }} The [`tfoot`](/html/element/tfoot/) element cannot be placed after any [`tbody`](/html/element/tbody/) and [`tr`](/html/element/tr/) element. Note that this directly contradicts the above normative requirement from HTML5. |
| Implicit ARIA role | `[rowgroup](/accessibility/aria/roles/rowgroup_role)` |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLTableSectionElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

### Deprecated attributes

The following attributes are deprecated and should not be used. They are documented below for reference when updating existing code and for historical interest only.

{{ htmlattrdef("align") }} {{ deprecated_inline }}
: This enumerated attribute specifies how horizontal alignment of each cell content will be handled. Possible values are:

-   `left`, aligning the content to the left of the cell
-   `center`, centering the content in the cell
-   `right`, aligning the content to the right of the cell
-   `justify`, inserting spaces into the textual content so that the content is justified in the cell
-   `char`, aligning the textual content on a special character with a minimal offset, defined by the {{ htmlattrxref("char", "tbody") }} and {{ htmlattrxref("charoff", "tbody") }} attributes.

If this attribute is not set, the `left` value is assumed.

**Note:**

-   To achieve the same effect as the `left`, `center`, `right` or `justify` values, use the CSS {{ cssxref("text-align") }} property on it.
-   To achieve the same effect as the `char` value, in CSS3, you can use the value of the {{ htmlattrxref("char", "tfoot") }} as the value of the {{ cssxref("text-align") }} property {{ unimplemented_inline }}.

{{ htmlattrdef("bgcolor") }} {{ Deprecated_inline }}
: The background color of the table. It is a [6-digit hexadecimal RGB code](/css/color_value#rgb_colors), prefixed by a '`#`'. One of the predefined [color kewords](/css/color_value#color_keywords) can also be used.

To achieve a similar effect, use the CSS {{ cssxref("background-color") }} property.

{{ htmlattrdef("char") }} {{ deprecated_inline }}
: This attribute specifies the alignment of the content in a column to a character. Typical values for this include a period (.) when attempting to align numbers or monetary values. If {{ htmlattrxref("align", "tfoot") }} is not set to `char`, this attribute is ignored.

{{ htmlattrdef("charoff") }} {{ deprecated_inline }}
: This attribute is used to indicate the number of characters to offset the column data from the alignment characters specified by the `char` attribute.

{{ htmlattrdef("valign") }} {{ deprecated_inline }}
: This attribute specifies the vertical alignment of the text within each row of cells of the table footer. Possible values for this attribute are:

-   `baseline`, which will put the text as close to the bottom of the cell as it is possible, but align it on the [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29) of the characters instead of the bottom of them. If characters are all of the size, this has the same effect as `bottom`.
-   `bottom`, which will put the text as close to the bottom of the cell as it is possible;
-   `middle`, which will center the text in the cell;
-   and `top`, which will put the text as close to the top of the cell as it is possible.

**Note:** Do not use this attribute as it is obsolete (and not supported) in the latest standard: instead set the CSS {{ cssxref("vertical-align") }} property on it.

## Examples

Please see the [`table`](/html/element/table/) page for examples on `<tfoot>`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'tfoot element' in that specification](https://html.spec.whatwg.org/multipage/tables.html#the-tfoot-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'tfoot element' in that specification](https://www.w3.org/TR/html52/tabular-data.html#the-tfoot-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.tfoot") }}

## See also

-   Other table-related HTML Elements: [`caption`](/html/element/caption/), [`col`](/html/element/col/), [`colgroup`](/html/element/colgroup/), [`table`](/html/element/table/), [`tbody`](/html/element/tbody/), [`td`](/html/element/td/), [`th`](/html/element/th/), [`thead`](/html/element/thead/), [`tr`](/html/element/tr/);
-   CSS properties and pseudo-classes that may be specially useful to style the `<tfoot>` element:
    -   the {{ cssxref(":nth-child") }} pseudo-class to set the alignment on the cells of the column;
    -   the {{ cssxref("text-align") }} property to align all cells content on the same character, like '.'.