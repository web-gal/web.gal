---
title: '<pre>: The Preformatted Text element'
tags:
  - Element
  - HTML
  - HTML grouping content
  - 'HTML:Flow content'
  - Reference
  - Web
permalink: html/element/pre
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre'
browserCompact: html.elements.pre
---
{{ HTMLRef }}

The **HTML `<pre>` element** represents preformatted text which is to be presented exactly as written in the HTML file. The text is typically rendered using a non-proportional ("[monospace](/en-US/docs/XUL/Style/monospace)") font. Whitespace inside this element is displayed as written.

{{ EmbedInteractiveExample("pages/tabbed/pre.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | [Flow content](/guide/html/content_categories#flow_content), palpable content. |
| Permitted content | [Phrasing content](/guide/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/guide/html/content_categories#flow_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLPreElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("cols") }} {{ non-standard_inline }}{{ obsolete_inline }}
: Contains the _preferred_ count of characters that a line should have. It was a non-standard synonym of {{ htmlattrxref("width", "pre") }}. To achieve such an effect, use CSS {{ Cssxref("width") }} instead.

{{ htmlattrdef("width") }} {{ obsolete_inline }}
: Contains the _preferred_ count of characters that a line should have. Though technically still implemented, this attribute has no visual effect; to achieve such an effect, use CSS {{ Cssxref("width") }} instead.

{{ htmlattrdef("wrap") }} {{ non-standard_inline }}
: Is a _hint_ indicating how the overflow must happen. In modern browser this hint is ignored and no visual effect results in its present; to achieve such an effect, use CSS {{ Cssxref("white-space") }} instead.

## Example

### HTML

```html
<p>Using CSS to change the font color is easy.</p>
<pre>
body {
  color: red;
}
</pre>

```

### Result

{{ EmbedLiveSample("Example") }}

## Accessibility concerns

It is important to provide an alternate description for any images or diagrams created using preformatted text. The alternate description should clearly and concisely describe the image or diagram's content.

People experiencing low vision conditions and browsing with the aid of assistive technology such as a screen reader may not understand what the preformatted text characters are representing when they are read out in sequence.

A combination of the [`figure`](/html/element/figure/) and [`figcaption`](/html/element/figcaption/) elements, supplemented by a combination of an {{ htmlattrxref("id") }} and the [ARIA](/accessibility/aria) `role` and `aria-labelledby` attributes allow the preformatted text to be announced as an image, with the `figcaption` serving as the image's alternate description.

### Example

```
<figure role="img" aria-labelledby="cow-caption">
  <pre>
  ___________________________
< I'm an expert in my field. >
  ---------------------------
         \   ^__^
          \  (oo)\_______
             (__)\       )\/\
                 ||----w |
                 ||     ||
  </pre>
  <figcaption id="cow-caption">
    A cow saying, "I'm an expert in my field." The cow is illustrated using preformatted text characters.
  </figcaption>
</figure>

```

-   [MDN Understanding WCAG, Guideline 1.1 explanations](/accessibility/understanding_wcag/perceivable#guideline_1.1_—_providing_text_alternatives_for_non-text_content)
-   [H86: Providing text alternatives for ASCII art, emoticons, and leetspeak | W3C Techniques for WCAG 2.0](https://www.w3.org/TR/WCAG20-TECHS/H86.html)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<pre>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-pre-element) | {{ Spec2('HTML WHATWG') }} | No significant change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of '<pre>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-pre-element) | {{ Spec2('HTML5 W3C') }} | No significant change from [**HTML 4.01 Specification**](https://www.w3.org/TR/html401/) |
| [**HTML 4.01 Specification** The definition of '<pre>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.3.4) | {{ Spec2('HTML4.01') }} | Deprecated the `cols` attribute |

## Browser compatibility

{{ Compat("html.elements.pre") }}

## See also

-   CSS: {{ Cssxref('white-space') }}, {{ Cssxref('word-break') }}
-   Related element: [`code`](/html/element/code/)