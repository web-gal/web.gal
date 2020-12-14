---
title: '<var>: The Variable element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Reference
  - Web
  - var
  - variable
permalink: html/element/var
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/var'
browserCompact: html.elements.var
---
{{ HTMLRef }}

The HTML **Variable element** (**`<var>`**) represents the name of a variable in a mathematical expression or a programming context. It's typically presented using an italicized version of the current typeface, although that behavior is browser-dependent.

{{ EmbedInteractiveExample("pages/tabbed/var.html", "tabbed-shorter") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

### Related elements

Other elements that are used in contexts in which `<var>` is commonly used include:

-   [`code`](/html/element/code/): The HTML Code element
-   [`kbd`](/html/element/kbd/): The HTML Keyboard input element
-   [`samp`](/html/element/samp/): The HTML Sample Output element

If you encounter code that is mistakenly using `<var>` for style purposes rather than semantic purposes, you should either use a [`span`](/html/element/span/) with appropriate CSS or, an appropriate semantic element among the following:

-   [`em`](/html/element/em/)
-   [`i`](/html/element/i/)
-   [`q`](/html/element/q/)

### Default style

Most browsers apply {{ cssxref("font-style") }} to `"italic"` when rendering `<var>`. This can be overridden in CSS, like this:

```css
var {
  font: bold 15px "Courier", "Courier New", monospace;
}
```

## Examples

### Basic example

Here's a simple example, using `<var>` to denote variable names in a mathematical equation.

```html
<p>A simple equation:
  <var>x</var> = <var>y</var> + 2 </p>

```

The output:

{{ EmbedLiveSample("Basic_example", 650,80) }}

### Overriding the default style

Using CSS, you can override the default style for the `<var>` element. In this example, variable names are rendered using bold Courier if it's available, otherwise it falls back to the default monospace font.

#### CSS

```css
var {
  font: bold 15px "Courier", "Courier New", monospace;
}
```

#### HTML

```html
<p>The variables <var>minSpeed</var> and <var>maxSpeed</var> control
   the minimum and maximum speed of the apparatus in revolutions
   per minute (RPM).</p>
```

This HTML uses `<var>` to enclose the names of two variables.

#### Result

{{ EmbedLiveSample("Overriding_the_default_style", 650, 120) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<var>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-var-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<var>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-var-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.var") }}