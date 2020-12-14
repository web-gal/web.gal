---
title: '<caption>: The Table Caption element'
tags:
  - Element
  - HTML
  - HTML Tables
  - HTML tabular data
  - Reference
  - Table Captions
  - Table Titles
  - Tables
  - Web
  - caption
permalink: html/element/caption
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/caption'
browserCompact: html.elements.caption
---
{{ HTMLRef }}

The **HTML `<caption>` element** specifies the caption (or title) of a table.

{{ EmbedInteractiveExample("pages/tabbed/caption.html", "tabbed-taller") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | [Flow content](/html/content_categories#flow_content). |
| Tag omission | The end tag can be omitted if the element is not immediately followed by ASCII whitespace or a comment. |
| Permitted parents | A [`table`](/html/element/table/) element, as its first descendant. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLTableCaptionElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

### Deprecated attributes

The following attributes are deprecated and should not be used. They are documented below for reference when updating existing code and for historical interest only.

{{ htmlattrdef("align") }} {{ deprecated_inline }}
: This enumerated attribute indicates how the caption must be aligned with respect to the table. It may have one of the following values:

`left`
: The caption is displayed to the left of the table.

`top`
: The caption is displayed above the table.

`right`
: The caption is displayed to the right of the table.

`bottom`
: The caption is displayed below the table.

**Usage note:** Do not use this attribute, as it has been deprecated. The [`caption`](/html/element/caption/) element should be styled using the [CSS](/en-US/docs/CSS) properties {{ cssxref("caption-side") }} and {{ cssxref("text-align") }}.

## Usage notes

The `<caption>` element should be the first child of its parent [`table`](/html/element/table/) element.

When the `<table>` element that contains the `<caption>` is the only descendant of a [`figure`](/html/element/figure/) element, you should use the [`figcaption`](/html/element/figcaption/) element instead of `<caption>`.

## Example

This simple example presents a table that includes a caption.

```html
<table>
  <caption>Example Caption</caption>
  <tr>
    <th>Login</th>
    <th>Email</th>
  </tr>
  <tr>
    <td>user1</td>
    <td>user1@sample.com</td>
  </tr>
  <tr>
    <td>user2</td>
    <td>user2@sample.com</td>
  </tr>
</table>
```

```css
caption {
  caption-side: top;
  align: right;
}
table {
  border-collapse: collapse;
  border-spacing: 0px;
}
table, th, td {
  border: 1px solid black;
}

```

{{ EmbedLiveSample('Example', 650, 100) }}

`table {background: red;}` do not alter caption. For that you need `display: block`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<caption>' in that specification](https://html.spec.whatwg.org/multipage/tables.html#the-caption-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<caption>' in that specification](https://www.w3.org/TR/html52/tabular-data.html#the-caption-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<caption>' in that specification](https://www.w3.org/TR/html401/struct/tables.html#h-11.2.2) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.caption") }}

## See also

-   CSS properties that may be specially useful to style the [`caption`](/html/element/caption/) element:
    -   {{ cssxref("text-align") }}, {{ cssxref("caption-side") }}.