---
title: '<blink>: The Blinking Text element (obsolete)'
tags:
  - Blink
  - Element
  - HTML
  - Obsolete
  - Reference
  - Web
permalink: html/element/blink
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blink'
deprecated: true
obsolete: true
browserCompact: html.elements.blink
---
{{ HTMLRef }} 

The **HTML Blink Element** (`<blink>`) is a non-standard element which causes the enclosed text to flash slowly.

Do not use this element as it is **obsolete** and is bad design practice. Blinking text is frowned upon by several accessibility standards and the CSS specification allows browsers to ignore the `<blink>` element.

## DOM interface

This element is unsupported and thus implements the {{ domxref("HTMLUnknownElement") }} interface.

## Example

```html
<blink>Why would somebody use this?</blink>

```

### Result (toned down!)

![Image:HTMLBlinkElement.gif](/@api/deki/files/247/=HTMLBlinkElement.gif)

## Specification

This element is non-standard and not part of any specification. If you don't believe us, [see for yourself in the HTML spec](https://html.spec.whatwg.org/multipage/obsolete.html#non-conforming-features).

## CSS polyfill

If you really do need a polyfill, then you can use the following CSS polyfill. Works in IE10+.

```css
blink {
  -webkit-animation: 2s linear infinite condemned_blink_effect; /* for Safari 4.0 - 8.0 */
  animation: 2s linear infinite condemned_blink_effect;
}

/* for Safari 4.0 - 8.0 */
@-webkit-keyframes condemned_blink_effect {
  0% {
    visibility: hidden;
  }
  50% {
    visibility: hidden;
  }
  100% {
    visibility: visible;
  }
}

@keyframes condemned_blink_effect {
  0% {
    visibility: hidden;
  }
  50% {
    visibility: hidden;
  }
  100% {
    visibility: visible;
  }
}
```

## Browser compatibility

{{ Compat("html.elements.blink") }}

## See also

-   [History of the creation of the HTML `<blink>` element](http://www.montulli.org/theoriginofthe%3Cblink%3Etag).
-   {{ cssxref("text-decoration") }}, where a blink value exists, though browsers are not required to effectively make it blink.
-   [`marquee`](/html/element/marquee/), another similar non-standard element.
-   [CSS animations](/guide/css/using_css_animations "/en-US/docs/Web/Guide/CSS/Using_CSS_animations") are the way to go to create such an effect.