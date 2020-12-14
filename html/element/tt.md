---
title: '<tt>: The Teletype Text element (obsolete)'
tags:
  - Element
  - HTML
  - Monospace
  - Monotype
  - Non-proportional Type
  - Obsolete
  - Reference
  - Teletype
  - Teletype Text
  - Web
  - font-family
  - tt
permalink: html/element/tt
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tt'
obsolete: true
browserCompact: html.elements.tt
---
{{ HTMLRef }}

The obsolete **HTML Teletype Text element** (**`<tt>`**) creates inline text which is presented using the [user agent's](/glossary/user_agent/) default monospace font face. This element was created for the purpose of rendering text as it would be displayed on a fixed-width display such as a teletype, text-only screen, or line printer.

The terms **non-proportional**, **monotype**, and **monospace** are used interchangeably and have the same general meaning: they describe a typeface whose characters are all the same number of pixels wide.

This element is obsolete, however. You should use the more semantically helpful [`code`](/html/element/code/), [`kbd`](/html/element/kbd/), [`samp`](/html/element/samp/), or [`var`](/html/element/var/) elements for inline text that needs to be presented in monospace type, or the [`pre`](/html/element/pre/) tag for content that should be presented as a separate block.

If none of the semantic elements are appropriate for your use case (for example, if you simply need to show some content in a non-proportional font), you should consider using the [`span`](/html/element/span/) element, styling it as desired using CSS. The {{ cssxref("font-family") }} property is a good place to start.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/en-US/docs/HTML/Content_categories#Flow_content), [phrasing content](/en-US/docs/HTML/Content_categories#Phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/en-US/docs/HTML/Content_categories#Phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/en-US/docs/HTML/Content_categories#Phrasing_content). |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes)

## Examples

### Basic example

This example uses `<tt>` to show text entered into, and output by, a terminal application.

```html
<p>Enter the following at the telnet command prompt: <code>set localecho</code><br />

The telnet client should display: <tt>Local Echo is on</tt></p>

```

#### Result

{{ EmbedLiveSample("Basic_example", 650, 80) }}

### Overriding the default font

You can override the browser's default font—if the browser permits you to do so, which it isn't required to do—using CSS:

#### CSS

```css
tt {
  font-family: "Lucida Console", "Menlo", "Monaco", "Courier",
               monospace;
}
```

#### HTML

```html
<p>Enter the following at the telnet command prompt: <code>set localecho</code><br />

The telnet client should display: <tt>Local Echo is on</tt></p>
```

#### Result

{{ EmbedLiveSample("Overriding_the_default_font", 650, 80) }}

## Usage notes

The `<tt>` element is, by default, rendered using the browser's default non-proportional font. You can override this using CSS by creating a rule using the `tt` selector, as seen in the example {{ anch("Overriding the default font") }} above.

User-configured changes to the default monospace font setting may take precedence over your CSS.

Although this element wasn't officially deprecated in HTML 4.01, its use was discouraged in favor of the semantic elements and/or CSS. The `<tt>` element is obsolete in HTML 5.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML 5** The definition of '<tt>' in that specification](https://www.w3.org/TR/html52/obsolete.html#elementdef-tt) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<tt>' in that specification](https://www.w3.org/TR/html401/present/graphics.html#h-15.2.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.tt") }}

## See also

-   The semantic [`code`](/html/element/code/), [`var`](/html/element/var/), [`kbd`](/html/element/kbd/), and [`samp`](/html/element/samp/) elements
-   The [`pre`](/html/element/pre/) element for displaying preformatted text blocks