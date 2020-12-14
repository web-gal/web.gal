---
title: <li>
tags:
  - Element
  - HTML
  - HTML grouping content
  - Reference
permalink: html/element/li
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li'
browserCompact: html.elements.li
---
{{ HTMLRef }}

The **HTML `<li>` element** is used to represent an item in a list. It must be contained in a parent element: an ordered list ([`ol`](/html/element/ol/)), an unordered list ([`ul`](/html/element/ul/)), or a menu ([`menu`](/html/element/menu/)). In menus and unordered lists, list items are usually displayed using bullet points. In ordered lists, they are usually displayed with an ascending counter on the left, such as a number or letter.

{{ EmbedInteractiveExample("pages/tabbed/li.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | [Flow content](/html/content_categories#flow_content). |
| Tag omission | The end tag can be omitted if the list item is immediately followed by another [`li`](/html/element/li/) element, or if there is no more content in its parent element. |
| Permitted parents | An [`ul`](/html/element/ul/), [`ol`](/html/element/ol/), or [`menu`](/html/element/menu/) element. Though not a conforming usage, the obsolete [`dir`](/html/element/dir/) can also be a parent. |
| Implicit ARIA role | `[listitem](/accessibility/aria/roles/listitem_role)` when child of an `[ol](/html/element/ol)`, `[ul](/html/element/ul)` or `[menu](/html/element/menu)` |
| Permitted ARIA roles | [`menuitem`](https://w3c.github.io/aria/#menuitem), [`menuitemcheckbox`](https://w3c.github.io/aria/#menuitemcheckbox), [`menuitemradio`](https://w3c.github.io/aria/#menuitemradio), [`option`](https://w3c.github.io/aria/#option), [`none`](https://w3c.github.io/aria/#none), [`presentation`](https://w3c.github.io/aria/#presentation), [`radio`](https://w3c.github.io/aria/#radio), [`separator`](https://w3c.github.io/aria/#separator), [`tab`](https://w3c.github.io/aria/#tab), [`treeitem`](https://w3c.github.io/aria/#treeitem) |
| DOM interface | {{ domxref("HTMLLIElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("value") }}
: This integer attribute indicates the current ordinal value of the list item as defined by the [`ol`](/html/element/ol/) element. The only allowed value for this attribute is a number, even if the list is displayed with Roman numerals or letters. List items that follow this one continue numbering from the value set. The **value** attribute has no meaning for unordered lists ([`ul`](/html/element/ul/)) or for menus ([`menu`](/html/element/menu/)).

**Note**: This attribute was deprecated in HTML4, but reintroduced in HTML5.

{{ htmlattrdef("type") }} {{ Deprecated_inline }}
: This character attribute indicates the numbering type:

-   `a`: lowercase letters
-   `A`: uppercase letters
-   `i`: lowercase Roman numerals
-   `I`: uppercase Roman numerals
-   `1`: numbers

This type overrides the one used by its parent [`ol`](/html/element/ol/) element, if any.

**Note:** This attribute has been deprecated; use the CSS {{ cssxref("list-style-type") }} property instead.

## Examples

For more detailed examples, see the [`ol`](/html/element/ol/) and [`ul`](/html/element/ul/) pages.

### Ordered list

```html
<ol>
    <li>first item</li>
    <li>second item</li>
    <li>third item</li>
</ol>

```

{{ EmbedLiveSample("Ordered_list") }}

### Ordered list with a custom value

```html
<ol type="I">
    <li value="3">third item</li>
    <li>fourth item</li>
    <li>fifth item</li>
</ol>

```

{{ EmbedLiveSample("Ordered_list_with_a_custom_value") }}

### Unordered list

```html
<ul>
    <li>first item</li>
    <li>second item</li>
    <li>third item</li>
</ul>
```

{{ EmbedLiveSample("Unordered_list") }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<li>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-li-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<li>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-li-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<li>' in that specification](https://www.w3.org/TR/html401/struct/lists.html#h-10.2) | {{ Spec2('HTML4.01') }} | The `type` attribute has been deprecated. |

## Browser compatibility

{{ Compat("html.elements.li") }}

## See also

-   Other list-related HTML Elements: [`ul`](/html/element/ul/), [`ol`](/html/element/ol/), [`menu`](/html/element/menu/), and the obsolete [`dir`](/html/element/dir/);
-   CSS properties that may be specially useful to style the `<li>` element:
    -   the {{ cssxref("list-style") }} property, to choose the way the ordinal is displayed,
    -   [CSS counters](/css/css_lists_and_counters/using_css_counters), to handle complex nested lists,
    -   the {{ cssxref("margin") }} property, to control the indent of the list item.