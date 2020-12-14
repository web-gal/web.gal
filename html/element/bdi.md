---
title: '<bdi>: The Bidirectional Isolate element'
tags:
  - BDI
  - BiDi
  - Directionality
  - Element
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Internationalization
  - Left-to-Right
  - Reference
  - Right-to-left
  - Text
  - Web
  - direction
  - i18n
  - ltr
  - rtl
permalink: html/element/bdi
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/bdi'
browserCompact: html.elements.bdi
---
{{ HTMLRef }}

The HTML **Bidirectional Isolate element** (**`<bdi>`**)  tells the browser's bidirectional algorithm to treat the text it contains in isolation from its surrounding text. It's particularly useful when a website dynamically inserts some text and doesn't know the directionality of the text being inserted.

{{ EmbedInteractiveExample("pages/tabbed/bdi.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

Bidirectional text is text that may contain both sequences of characters that are arranged left-to-right (LTR) and sequences of characters that are arranged right-to-left (RTL), such as an Arabic quotation embedded in an English string. Browsers implement the [Unicode Bidirectional Algorithm](https://www.w3.org/International/articles/inline-bidi-markup/uba-basics) to handle this. In this algorithm, characters are given an implicit directionality: for example, Latin characters are treated as LTR while Arabic characters are treated as RTL. Some other characters (such as spaces and some punctuation) are treated as neutral and are assigned directionality based on that of their surrounding characters.

Usually, the bidirectional algorithm will do the right thing without the author having to provide any special markup but, occasionally, the algorithm needs help. That's where `<bdi>` comes in.

The `<bdi>` element is used to wrap a span of text and instructs the bidirectional algorithm to treat this text in isolation from its surroundings. This works in two ways:

-   The directionality of text embedded in `<bdi>` _does not influence_ the directionality of the surrounding text.
-   The directionality of text embedded in `<bdi>` _is not influenced by_ the directionality of the surrounding text.

For example, consider some text like:

```
EMBEDDED-TEXT - 1st place
```

If `EMBEDDED-TEXT` is LTR, this works fine. But if `EMBEDDED-TEXT` is RTL, then   `- 1` will be treated as RTL text (because it consists of neutral and weak characters). The result will be garbled:

```
1 - EMBEDDED-TEXTst place
```

If you know the directionality of `EMBEDDED-TEXT` in advance, you can fix this problem by wrapping `EMBEDDED-TEXT` in a [`span`](/html/element/span/) with the {{ htmlattrxref("dir") }} attribute set to the known directionality. But if you don't know the directionality - for example, because `EMBEDDED-TEXT` is being read from a database or entered by the user - you should use `<bdi>` to prevent the directionality of `EMBEDDED-TEXT` from affecting its surroundings.

Though the same visual effect can be achieved using the CSS rule {{ cssxref("unicode-bidi") }}`: isolate` on a [`span`](/html/element/span/) or another text-formatting element, HTML authors should not use this approach because it is not semantic and browsers are allowed to ignore CSS styling.

Embedding the characters in `<span dir="auto">` has the same effect as using `<bdi>`, but its semantics are less clear.

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

Like all other HTML elements, this element supports the [global attributes](/html/global_attributes), except that the {{ htmlattrxref("dir") }} attribute behaves differently than normal: it defaults to `auto`, meaning its value is never inherited from the parent element. This means that unless you specify a value of either `rtl` or `ltr` for `dir`, the [user agent](/glossary/user_agent/) will determine the correct directionality to use based on the contents of the `<bdi>`.

## Examples

### No <bdi> with only LTR

This example lists the winners of a competition using [`span`](/html/element/span/) elements only. When the names only contain LTR text the results look fine:

```html
<ul>
 <li><span class="name">Henrietta Boffin</span> - 1st place</li>
 <li><span class="name">Jerry Cruncher</span> - 2nd place</li>
</ul>

```

```css
body {
  border: 1px solid #3f87a6;
  max-width: calc(100% - 40px - 6px);
  padding: 20px;
  width: calc(100% - 40px - 6px);
  border-width: 1px 1px 1px 5px;
}

```

{{ EmbedLiveSample('bdi-sample-1','','120','','','bdi-example')  }}

### No <bdi> with RTL text

This example lists the winners of a competition using [`span`](/html/element/span/) elements only, and one of the winners has a name consisting of RTL text. In this case the "`- 1`", which consists of characters with neutral or weak directionality, will adopt the directionality of the RTL text, and the result will be garbled:

```html
<ul>
 <li><span class="name">اَلأَعْشَى</span> - 1st place</li>
 <li><span class="name">Jerry Cruncher</span> - 2nd place</li>
</ul>

```

```css
body {
  border: 1px solid #3f87a6;
  max-width: calc(100% - 40px - 6px);
  padding: 20px;
  width: calc(100% - 40px - 6px);
  border-width: 1px 1px 1px 5px;
}

```

{{ EmbedLiveSample('bdi-sample-2','','120','','','bdi-example')  }}

### Using <bdi> with LTR and RTL text

This example lists the winners of a competition using `<bdi>` elements. These elements instruct the browser to treat the name in isolation from its embedding context, so the example output is properly ordered:

```html
<ul>
 <li><bdi class="name">اَلأَعْشَى</bdi> - 1st place</li>
 <li><bdi class="name">Jerry Cruncher</bdi> - 2nd place</li>
</ul>

```

```css
body {
  border: 1px solid #3f87a6;
  max-width: calc(100% - 40px - 6px);
  padding: 20px;
  width: calc(100% - 40px - 6px);
  border-width: 1px 1px 1px 5px;
}

```

{{ EmbedLiveSample('bdi-sample-3','','120','','','bdi-example')  }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<bdi>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-bdi-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<bdi>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-bdi-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.bdi") }}

## See also

-   [Inline markup and bidirectional text in HTML](https://www.w3.org/International/articles/inline-bidi-markup/)
-   [Unicode Bidirectional Algorithm basics](https://www.w3.org/International/articles/inline-bidi-markup/uba-basics)
-   [Localization and Internationalization](/localization)
-   Related HTML element: [`bdo`](/html/element/bdo/)
-   Related CSS properties: {{ cssxref("direction") }}, {{ cssxref("unicode-bidi") }}