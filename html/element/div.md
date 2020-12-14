---
title: '<div>: The Content Division element'
tags:
  - Content Division
  - Element
  - HTML
  - HTML grouping content
  - 'HTML:Flow content'
  - Layout
  - Reference
  - Web
  - div
permalink: html/element/div
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div'
browserCompact: html.elements.div
---
{{ HTMLRef }}

The **HTML Content Division element** (**`<div>`**) is the generic container for flow content. It has no effect on the content or layout until styled in some way using [CSS](/glossary/css/) (e.g. styling is directly applied to it, or some kind of layout model like [Flexbox](/css/css_flexible_box_layout) is applied to its parent element).

{{ EmbedInteractiveExample("pages/tabbed/div.html","tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

As a "pure" container, the `<div>` element does not inherently represent anything. Instead, it's used to group content so it can be easily styled using the {{ htmlattrxref("class") }} or {{ htmlattrxref("id") }} attributes, marking a section of a document as being written in a different language (using the {{ htmlattrxref("lang") }} attribute), and so on.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), palpable content. |
| Permitted content | [Flow content](/html/content_categories#flow_content).  
Or (in [WHATWG](/glossary/whatwg/) HTML): If the parent is a [`dl`](/html/element/dl/) element: one or more [`dt`](/html/element/dt/) elements followed by one or more [`dd`](/html/element/dd/) elements, optionally intermixed with [`script`](/html/element/script/) and [`template`](/html/element/template/) elements. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content).  
Or (in [WHATWG](/glossary/whatwg/) HTML): [`dl`](/html/element/dl/) element. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLDivElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

**Note:** The `align` attribute is obsolete; do not use it anymore. Instead, you should use CSS properties or techniques such as [CSS Grid](/css/css_grid_layout) or [CSS Flexbox](/en-US/docs/Learn/CSS/CSS_layout/Flexbox) to align and position `<div>` elements on the page.

## Usage notes

-   The `<div>` element should be used only when no other semantic element (such as [`article`](/html/element/article/) or [`nav`](/html/element/nav/)) is appropriate.

## Examples

### A simple example

```html
<div>
  <p>Any kind of content here. Such as
  &lt;p&gt;, &lt;table&gt;. You name it!</p>
</div> 
```

The result looks like this:

{{ EmbedLiveSample("A_simple_example", 650, 60) }}

### A styled example

This example creates a shadowed box by applying a style to the `<div>` using CSS. Note the use of the {{ htmlattrxref("class") }} attribute on the `<div>` to apply the style named `"shadowbox"` to the element.

#### HTML

```html
<div class="shadowbox">
  <p>Here's a very interesting note displayed in a
  lovely shadowed box.</p>
</div>
```

#### CSS

```css
.shadowbox {
  width: 15em;
  border: 1px solid #333;
  box-shadow: 8px 8px 5px #444;
  padding: 8px 12px;
  background-image: linear-gradient(180deg, #fff, #ddd 40%, #ccc);
}
```

#### Result

{{ EmbedLiveSample("A_styled_example", 650, 120) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<div>' in that specification](https://html.spec.whatwg.org/multipage/grouping-content.html#the-div-element) | {{ Spec2('HTML WHATWG') }} | No changes since the latest snapshot |
| [**HTML 5** The definition of '<div>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-div-element) | {{ Spec2('HTML5 W3C') }} | Obsoleted `align` |
| [**HTML 4.01 Specification** The definition of '<div>' in that specification](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.div") }}

## See also

-   Semantic sectioning elements: [`section`](/html/element/section/), [`article`](/html/element/article/), [`nav`](/html/element/nav/), [`header`](/html/element/header/), [`footer`](/html/element/footer/)
-   [`span`](/html/element/span/) element for styling of phrasing content