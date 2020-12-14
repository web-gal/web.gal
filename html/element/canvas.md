---
title: '<canvas>: The Graphics Canvas element'
tags:
  - Canvas
  - Element
  - HTML
  - HTML scripting
  - HTML5
  - Reference
  - Web
permalink: html/element/canvas
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas'
browserCompact: html.elements.canvas
---
{{ HTMLRef }}

Use the **HTML `<canvas>` element** with either the [canvas scripting API](/api/canvas_api) or the [WebGL API](/api/webgl_api) to draw graphics and animations.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), [embedded content](/html/content_categories#embedded_content), palpable content. |
| Permitted content | Transparent but with no [interactive content](/html/content_categories#interactive_content) descendants except for [`a`](/html/element/a/) elements, [`button`](/html/element/button/) elements, [`input`](/html/element/input/) elements whose {{ htmlattrxref("type", "input") }} attribute is `checkbox`, `radio`, or `button`. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLCanvasElement") }} |

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

{{ htmlattrdef("height") }}
: The height of the coordinate space in CSS pixels. Defaults to 150.

{{ htmlattrdef("moz-opaque") }} {{ non-standard_inline }} {{ deprecated_inline }}
: Lets the canvas know whether or not translucency will be a factor. If the canvas knows there's no translucency, painting performance can be optimized. This is only supported by Mozilla-based browsers; use the standardized {{domxref("HTMLCanvasElement.getContext()", "canvas.getContext('2d', { alpha: false })")}} instead.

{{ htmlattrdef("width") }}
: The width of the coordinate space in CSS pixels. Defaults to 300.

## Usage notes

### Alternative content

You may (and should) provide alternate content inside the `<canvas>` block. That content will be rendered both on older browsers that don't support canvas and in browsers with JavaScript disabled. Providing a useful fallback text or sub DOM helps to [make the the canvas more accessible](/api/canvas_api/tutorial/hit_regions_and_accessibility).

### Required </canvas> tag

Unlike the [`img`](/html/element/img/) element, the [`canvas`](/html/element/canvas/) element **requires** the closing tag (`</canvas>`).

### Sizing the canvas using CSS versus HTML

The displayed size of the canvas can be changed using CSS, but if you do this the image is scaled during rendering to fit the styled size, which can make the final graphics rendering end up being distorted.

It is better to specify your canvas dimensions by setting the `width` and `height` attributes directly on the `<canvas>` elements, either directly in the HTML or by using JavaScript.

### Maximum canvas size

The maximum size of a `<canvas>` element is very large, but the exact size depends on the browser. The following is some data we've collected from various tests and other sources (e.g. [Stack Overflow](https://stackoverflow.com/questions/6081483/maximum-size-of-a-canvas-element)):

| Browser | Maximum height | Maximum width | Maximum area |
| --- | --- | --- | --- |
| Chrome | 32,767 pixels | 32,767 pixels | 268,435,456 pixels (i.e., 16,384 x 16,384) |
| Firefox | 32,767 pixels | 32,767 pixels | 472,907,776 pixels (i.e., 22,528 x 20,992) |
| Safari | 32,767 pixels | 32,767 pixels | 268,435,456 pixels (i.e., 16,384 x 16,384) |
| IE | 8,192 pixels | 8,192 pixels | ? |

**Note**: Exceeding the maximum dimensions or area renders the canvas unusable — drawing commands will not work.

## Examples

### HTML

This code snippet adds a canvas element to your HTML document. A fallback text is provided if a browser is unable to render the canvas, or if can't read a canvas.

```html
<canvas width="300" height="300">
  An alternative text describing what your canvas displays.
</canvas>

```

### JavaScript

Then in the JavaScript code, call {{ domxref("HTMLCanvasElement.getContext()") }} to get a drawing context and start drawing onto the canvas:

```js
const canvas = document.querySelector('canvas');
const ctx = canvas.getContext('2d');
ctx.fillStyle = 'green';
ctx.fillRect(10, 10, 100, 100);
```

### Result

{{ EmbedLiveSample('Examples') }}

## Accessibility concerns

### Alternative content

The `<canvas>` element on its own is just a bitmap and does not provide information about any drawn objects. Canvas content is not exposed to accessibility tools as semantic HTML is. In general, you should avoid using canvas in an accessible website or app. The following guides can help to make it more accessible.

-   [MDN Hit regions and accessability](/api/canvas_api/tutorial/hit_regions_and_accessibility)
-   [Canvas accessibility use cases](https://www.w3.org/WAI/PF/HTML/wiki/Canvas_Accessibility_Use_Cases)
-   [Canvas element accessibility issues](https://www.w3.org/html/wg/wiki/AddedElementCanvas)
-   [HTML5 Canvas Accessibility in Firefox 13 – by Steve Faulkner](https://developer.paciellogroup.com/blog/2012/06/html5-canvas-accessibility-in-firefox-13/)
-   [Best practices for interactive canvas elements](https://html.spec.whatwg.org/multipage/scripting.html#best-practices)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<canvas>' in that specification](https://html.spec.whatwg.org/multipage/scripting.html#the-canvas-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<canvas>' in that specification](https://www.w3.org/TR/html52/semantics-scripting.html#the-canvas-element) | {{ Spec2('HTML5 W3C') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.canvas") }}

## See also

-   [MDN canvas portal](/api/canvas_api)
-   [Canvas tutorial](/api/canvas_api/tutorial)
-   [Canvas cheat sheet](https://simon.html5.org/dump/html5-canvas-cheat-sheet.html)
-   [Canvas-related demos](/en-US/demos/tag/tech:canvas)
-   [Canvas introduction by Apple](https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/HTML-canvas-guide/Introduction/Introduction.html)