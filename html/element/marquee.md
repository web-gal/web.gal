---
title: '<marquee>: The Marquee element (Obsolete)'
tags:
  - Element
  - HTML
  - Obsolete
  - Reference
  - Web
  - marquee
permalink: html/element/marquee
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/marquee'
obsolete: true
browserCompact: html.elements.marquee
---
The HTML `<marquee>` element is used to insert a scrolling area of text. You can control what happens when the text reaches the edges of its content area using its attributes.

| Property | Value |
| --- | --- |
| DOM interface | {{ DOMxRef("HTMLMarqueeElement") }} |

## Attributes

{{ htmlattrdef("behavior") }}
: Sets how the text is scrolled within the marquee. Possible values are `scroll`, `slide` and `alternate`. If no value is specified, the default value is `scroll`.

{{ htmlattrdef("bgcolor") }}
: Sets the background color through color name or hexadecimal value.

{{ htmlattrdef("direction") }}
: Sets the direction of the scrolling within the marquee. Possible values are `left`, `right`, `up` and `down`. If no value is specified, the default value is `left`.

{{ htmlattrdef("height") }}
: Sets the height in pixels or percentage value.

{{ htmlattrdef("hspace") }}
: Sets the horizontal margin

{{ htmlattrdef("loop") }}
: Sets the number of times the marquee will scroll. If no value is specified, the default value is −1, which means the marquee will scroll continuously.

{{ htmlattrdef("scrollamount") }}
: Sets the amount of scrolling at each interval in pixels. The default value is 6.

{{ htmlattrdef("scrolldelay") }}
: Sets the interval between each scroll movement in milliseconds. The default value is 85. Note that any value smaller than 60 is ignored and the value 60 is used instead, unless `truespeed` is specified.

{{ htmlattrdef("truespeed") }}
: By default, `scrolldelay` values lower than 60 are ignored. If `truespeed` is present, those values are not ignored.

{{ htmlattrdef("vspace") }}
: Sets the vertical margin in pixels or percentage value.

{{ htmlattrdef("width") }}
: Sets the width in pixels or percentage value.

## Event handlers

{{ htmlattrdef("onbounce") }}
: Fires when the marquee has reached the end of its scroll position. It can only fire when the behavior attribute is set to `alternate`.

{{ htmlattrdef("onfinish") }}
: Fires when the marquee has finished the amount of scrolling that is set by the loop attribute. It can only fire when the loop attribute is set to some number that is greater than 0.

{{ htmlattrdef("onstart") }}
: Fires when the marquee starts scrolling.

## Methods

`start()`
: Starts scrolling of the marquee.

`stop()`
: Stops scrolling of the marquee.

## Examples

```html
<marquee>This text will scroll from right to left</marquee>

<marquee direction="up">This text will scroll from bottom to top</marquee>

<marquee direction="down" width="250" height="200" behavior="alternate" style="border:solid">
  <marquee behavior="alternate">
    This text will bounce
  </marquee>
</marquee>
```

{{ EmbedLiveSample("Examples", 600, 450) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<marquee>' in that specification](https://html.spec.whatwg.org/multipage/obsolete.html#the-marquee-element-2) | {{ Spec2('HTML WHATWG') }} | Make it obsolete in favor of CSS but define its expected behavior, for backward compatibility. However, the development of the marquee features of CSS have since been [abandoned](https://www.w3.org/TR/css3-marquee/). |
| [**HTML 5** The definition of '<marquee>' in that specification](https://www.w3.org/TR/html52/obsolete.html#the-marquee-element-0) | {{ Spec2('HTML5 W3C') }} | Make it obsolete in favor of CSS but define its expected behavior, for backward compatibility. However, the development of the marquee features of CSS have since been [abandoned](https://www.w3.org/TR/css3-marquee/). |

## Browser compatibility

{{ Compat("html.elements.marquee") }}

## See also

-   {{ DOMxRef("HTMLMarqueeElement") }}