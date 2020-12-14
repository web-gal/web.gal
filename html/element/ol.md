---
title: '<ol>: The Ordered List element'
tags:
  - Element
  - HTML
  - HTML grouping content
  - 'HTML:Flow content'
  - Reference
permalink: html/element/ol
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol'
browserCompact: html.elements.ol
---
{{ HTMLRef }}

The **HTML `<ol>` element** represents an ordered list of items — typically rendered as a numbered list.

{{ EmbedInteractiveExample("pages/tabbed/ol.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), and if the `<ol>` element's children include at least one [`li`](/html/element/li/) element, [palpable content](/guide/html/content_categories#palpable_content). |
| Permitted content | Zero or more [`li`](/html/element/li/), [`script`](/html/element/script/) and [`template`](/html/element/template/) elements. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/guide/html/content_categories#flow_content). |
| Implicit ARIA role | `[list](/accessibility/aria/roles/list_role)` |
| Permitted ARIA roles | [`directory`](https://w3c.github.io/aria/#directory), [`group`](https://w3c.github.io/aria/#group), [`listbox`](https://w3c.github.io/aria/#listbox), [`menu`](https://w3c.github.io/aria/#menu), [`menubar`](https://w3c.github.io/aria/#menubar), [`none`](https://w3c.github.io/aria/#none), [`presentation`](https://w3c.github.io/aria/#presentation), [`radiogroup`](https://w3c.github.io/aria/#radiogroup), [`tablist`](https://w3c.github.io/aria/#tablist), [`toolbar`](https://w3c.github.io/aria/#toolbar), [`tree`](https://w3c.github.io/aria/#tree) |
| DOM interface | {{ DOMxRef("HTMLOListElement") }} |

## Attributes

This element also accepts the [global attributes](/html/global_attributes).

{{ HTMLAttrDef("reversed") }}
: This Boolean attribute specifies that the list’s items are in reverse order. Items will be numbered from high to low.

{{ HTMLAttrDef("start") }}
: An integer to start counting from for the list items. Always an Arabic numeral (1, 2, 3, etc.), even when the numbering `type` is letters or Roman numerals. For example, to start numbering elements from the letter "d" or the Roman numeral "iv," use `start="4"`.

{{ HTMLAttrDef("type") }}
: Sets the numbering type:

-   `a` for lowercase letters
-   `A` for uppercase letters
-   `i` for lowercase Roman numerals
-   `I` for uppercase Roman numerals
-   `1` for numbers (default)

The specified type is used for the entire list unless a different {{ HTMLAttrxRef("type", "li") }} attribute is used on an enclosed [`li`](/html/element/li/) element.

**Note:** Unless the type of the list number matters (like legal or technical documents where items are referenced by their number/letter), use the CSS {{ CSSxRef("list-style-type") }} property instead.

## Usage notes

Typically, ordered list items display with a preceding [marker](/css/::marker), such as a number or letter.

The `<ol>` and [`ul`](/html/element/ul/) elements may nest as deeply as desired, alternating between `<ol>` and `<ul>` however you like.

The `<ol>` and [`ul`](/html/element/ul/) elements both represent a list of items. The difference is with the `<ol>` element, the order is meaningful. For example:

-   Steps in a recipe
-   Turn-by-turn directions
-   The list of ingredients in decreasing proportion on nutrition information labels

To determine which list to use, try changing the order of the list items; if the meaning changes, use the `<ol>` element — otherwise you can use [`ul`](/html/element/ul/).

## Examples

### Simple example

```html
<ol>
  <li>Fee</li>
  <li>Fi</li>
  <li>Fo</li>
  <li>Fum</li>
</ol>

```

The above HTML will output:

{{ EmbedLiveSample("Simple_example", 400, 100) }}

### Using Roman Numeral type

```html
<ol type="i">
  <li>Introduction</li>
  <li>List of Greivances</li>
  <li>Conclusion</li>
</ol> 
```

The above HTML will output:

{{ EmbedLiveSample("Using_Roman_Numeral_type", 400, 100) }}

### Using the start attribute

```html
<p>Finishing places of contestants not in the winners’ circle:</p>

<ol start="4">
  <li>Speedwalk Stu</li>
  <li>Saunterin’ Sam</li>
  <li>Slowpoke Rodriguez</li>
</ol>

```

The above HTML will output:

{{ EmbedLiveSample("Using_the_start_attribute", 400, 100) }}

### Nesting lists

```html
<ol>
  <li>first item</li>
  <li>second item  <!-- closing </li> tag not here! -->
    <ol>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ol>
  </li>            <!-- Here's the closing </li> tag -->
  <li>third item</li>
</ol>

```

The above HTML will output:

{{ EmbedLiveSample("Nesting_lists", 400, 150) }}

### Unordered list inside ordered list

```html
<ol>
  <li>first item</li>
  <li>second item  <!-- closing </li> tag not here! -->
    <ul>
      <li>second item first subitem</li>
      <li>second item second subitem</li>
      <li>second item third subitem</li>
    </ul>
  </li>            <!-- Here's the closing </li> tag -->
  <li>third item</li>
</ol>

```

The above HTML will output:

{{ EmbedLiveSample("Unordered_list_inside_ordered_list", 400, 150) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<ol>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-ol-element) | {{ Spec2('HTML WHATWG') }} | No change since last W3C snapshot, [**HTML 5**](https://www.w3.org/TR/html52/). |
| [**HTML 5** The definition of 'HTMLOListElement' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-ol-element) | {{ Spec2('HTML5 W3C') }} | Added `reversed` and `start` attributed; un-deprecated `type` |
| [**HTML 4.01 Specification** The definition of '<ol>' in that specification](https://www.w3.org/TR/html401/struct/lists.html#h-10.2) | {{ Spec2('HTML4.01') }} | Deprecated `compact` and `type`. |

## Browser compatibility

{{ Compat("html.elements.ol") }}

## See also

-   Other list-related HTML Elements: [`ul`](/html/element/ul/), [`li`](/html/element/li/), [`menu`](/html/element/menu/)
-   CSS properties that may be specially useful to style the `<ol>` element:
    -   the {{ CSSxRef("list-style") }} property, to choose the way the ordinal displays
    -   [CSS counters](/css/css_lists_and_counters/using_css_counters), to handle complex nested lists
    -   the {{ CSSxRef("line-height") }} property, to simulate the deprecated {{ HTMLAttrxRef("compact", "ol") }} attribute
    -   the {{ CSSxRef("margin") }} property, to control the list indentation