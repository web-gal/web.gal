---
title: '<ul>: The Unordered List element'
tags:
  - Element
  - HTML
  - HTML grouping content
  - Reference
permalink: html/element/ul
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul'
browserCompact: html.elements.ul
---
{{ HTMLRef }}

The **HTML `<ul>` element** represents an unordered list of items, typically rendered as a bulleted list.

{{ EmbedInteractiveExample("pages/tabbed/ul.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), and if the `<ul>` element's children include at least one [`li`](/html/element/li/) element, [palpable content](/guide/html/content_categories#palpable_content). |
| Permitted content | Zero or more [`li`](/html/element/li/), [`script`](/html/element/script/) and [`template`](/html/element/template/) elements. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | `[list](/accessibility/aria/roles/list_role)` |
| Permitted ARIA roles | [`directory`](https://w3c.github.io/aria/#directory), [`group`](https://w3c.github.io/aria/#group), [`listbox`](https://w3c.github.io/aria/#listbox), [`menu`](https://w3c.github.io/aria/#menu), [`menubar`](https://w3c.github.io/aria/#menubar), [`none`](https://w3c.github.io/aria/#none), [`presentation`](https://w3c.github.io/aria/#presentation), [`radiogroup`](https://w3c.github.io/aria/#radiogroup), [`tablist`](https://w3c.github.io/aria/#tablist), [`toolbar`](https://w3c.github.io/aria/#toolbar), [`tree`](https://w3c.github.io/aria/#tree) |
| DOM Interface | {{ domxref("HTMLUListElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("compact")  }} {{ Deprecated_inline }}
: This Boolean attribute hints that the list should be rendered in a compact style. The interpretation of this attribute depends on the [user agent](/glossary/user_agent/), and it doesn't work in all browsers.

: **Warning:** Do not use this attribute, as it has been deprecated: use [CSS](/en-US/docs/CSS) instead. To give a similar effect as the `compact` attribute, the CSS property {{ cssxref("line-height") }} can be used with a value of `80%`.

{{ htmlattrdef("type")  }} {{ Deprecated_inline }}
: This attribute sets the bullet style for the list. The values defined under HTML3.2 and the transitional version of HTML 4.0/4.01 are:

-   `circle`
-   `disc`
-   `square`

A fourth bullet type has been defined in the WebTV interface, but not all browsers support it: `triangle`.

If not present and if no [CSS](/css) {{ cssxref("list-style-type")  }} property applies to the element, the user agent selects a bullet type depending on the nesting level of the list.

**Warning:** Do not use this attribute, as it has been deprecated; use the [CSS](/css) {{ cssxref("list-style-type")  }} property instead.

## Usage notes

-   The `<ul>` element is for grouping a collection of items that do not have a numerical ordering, and their order in the list is meaningless. Typically, unordered-list items are displayed with a bullet, which can be of several forms, like a dot, a circle, or a square. The bullet style is not defined in the HTML description of the page, but in its associated CSS, using the {{ cssxref("list-style-type")  }} property.
-   The `<ul>` and [`ol`](/html/element/ol/) elements may be nested as deeply as desired. Moreover, the nested lists may alternate between `<ol>` and `<ul>` without restriction.
-   The [`ol`](/html/element/ol/) and `<ul>` elements both represent a list of items. They differ in that, with the [`ol`](/html/element/ol/) element, the order is meaningful. As a rule of thumb to determine which one to use, try changing the order of the list items; if the meaning is changed, the [`ol`](/html/element/ol/) element should be used, otherwise you can use `<ul>`.

## Examples

### Simple example

```html
<ul>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ul>

```

The above HTML will output:

{{ EmbedLiveSample("Simple_example", 400, 100) }}

### Nesting a list

```html
<ul>
  <li>first item</li>
  <li>second item
  <!-- Look, the closing </li> tag is not placed here! -->
    <ul>
      <li>second item first subitem</li>
      <li>second item second subitem
      <!-- Same for the second nested unordered list! -->
        <ul>
          <li>second item second subitem first sub-subitem</li>
          <li>second item second subitem second sub-subitem</li>
          <li>second item second subitem third sub-subitem</li>
        </ul>
      </li> <!-- Closing </li> tag for the li that
                  contains the third unordered list -->
      <li>second item third subitem</li>
    </ul>
  <!-- Here is the closing </li> tag -->
  </li>
  <li>third item</li>
</ul>
```

The above HTML will output:

{{ EmbedLiveSample("Nesting_a_list", 400, 220) }}

### Ordered list inside unordered list

```html
<ul>
  <li>first item</li>
  <li>second item
  <!-- Look, the closing </li> tag is not placed here! -->
    <ol>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ol>
  <!-- Here is the closing </li> tag -->
  </li>
  <li>third item</li>
</ul>

```

The above HTML will output:

{{ EmbedLiveSample("Ordered_list_inside_unordered_list", 400, 150) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<ul>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-ul-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<ul>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-ul-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.ul") }}

## See also

-   Other list-related HTML Elements: [`ol`](/html/element/ol/), [`li`](/html/element/li/), [`menu`](/html/element/menu/)
-   CSS properties that may be specially useful to style the `<ul>` element:
    -   the {{ CSSxRef("list-style") }} property, to choose the way the ordinal displays
    -   [CSS counters](/css/css_lists_and_counters/using_css_counters), to handle complex nested lists
    -   the {{ CSSxRef("line-height") }} property, to simulate the deprecated {{ HTMLAttrxRef("compact", "ul") }} attribute
    -   the {{ CSSxRef("margin") }} property, to control the list indentation