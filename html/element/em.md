---
title: '<em>: The Emphasis element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Web
permalink: html/element/em
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em'
browserCompact: html.elements.em
---
{{ HTMLRef }}

The **HTML `<em>` element** marks text that has stress emphasis. The `<em>` element can be nested, with each level of nesting indicating a greater degree of emphasis.

{{ EmbedInteractiveExample("pages/tabbed/em.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | [Flow content](/guide/html/content_categories#flow_content), [phrasing content](/guide/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/guide/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/guide/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} Up to Gecko 1.9.2 (Firefox 4) inclusive, Firefox implements the {{ domxref("HTMLSpanElement") }} interface for this element. |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

The `<em>` element is for words that have a stressed emphasis compared to surrounding text, which is often limited to a word or words of a sentence and affects the meaning of the sentence itself.

Typically this element is displayed in italic type. However, it should not be used simply to apply italic styling; use the CSS {{ cssxref("font-style") }} property for that purpose. Use the [`cite`](/html/element/cite/) element to mark the title of a work (book, play, song, etc.). Use the [`i`](/html/element/i/) element to mark text that is in an alternate tone or mood, which covers many common situations for italics such as scientific names or words in other languages. Use the [`strong`](/html/element/strong/) element to mark text that has greater importance than surrounding text.

### <i> vs. <em>

New developers are often confused at seeing multiple elements that produce similar results. `<em>` and `<i>` are a common example, since they both italicize text. What's the difference? Which should you use?

By default, the visual result is the same. However, the semantic meaning is different. The `<em>` element represents stress emphasis of its contents, while the `<i>` element represents text that is set off from the normal prose, such a foreign word, fictional character thoughts, or when the text refers to the definition of a word instead of representing its semantic meaning. (The title of a work, such as the name of a book or movie, should use `<cite>`.)

This means the right one to use depends on the situation. Neither is for purely decorational purposes, that's what CSS styling is for.

An example for `<em>` could be: "Just _do_ it already!", or: "We _had_ to do something about it". A person or software reading the text would pronounce the words in italics with an emphasis, using verbal stress.

An example for `<i>` could be: "The _Queen Mary_ sailed last night". Here, there is no added emphasis or importance on the word "Queen Mary". It is merely indicated that the object in question is not a queen named Mary, but a ship named _Queen Mary_. Another example for `<i>` could be: "The word _the_ is an article".

## Example

The `<em>` element is often used to indicate an implicit or explicit contrast.

```html
<p>
  In HTML 5, what was previously called
  <em>block-level</em> content is now called
  <em>flow</em> content.
</p>
```

### Result

{{ EmbedLiveSample("Example") }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<em>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-em-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<em>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-em-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<em>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.2.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.em") }}

## See also

-   [`i`](/html/element/i/)