---
title: '<i>: The Idiomatic Text element'
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Web
  - em
permalink: html/element/i
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/i'
browserCompact: html.elements.i
---
{{ HTMLRef }}

The **HTML Idiomatic Text element (`<i>`)** represents a range of text that is set off from the normal text for some reason, such as idiomatic text, technical terms, taxonomical designations, among others. Historically, these have been presented using italicized type, which is the original source of the `<i>` naming of this element.

{{ EmbedInteractiveExample("pages/tabbed/i.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

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

-   Use the `<i>` element for text that is set off from the normal prose for readability reasons. This would be a range of text with different semantic meaning than the surrounding text. Among the use cases for the `<i>` element are spans of text representing a different quality or mode of text, such as:
    -   Alternative voice or mood
    -   Taxonomic designations (such as the genus and species "_Homo sapiens_")
    -   Idiomatic terms from another language (such as "_et cetera_"); these should include the {{ htmlattrxref("lang") }} attribute to identify the language
    -   Technical terms
    -   Transliterations
    -   Thoughts (such as "She wondered,_What is this writer talking about, anyway?_")
    -   Ship or vessel names in Western writing systems (such as "They searched the docks for the _Empress of the Galaxy_, the ship to which they were assigned.")
-   In earlier versions of the HTML specification, the `<i>` element was merely a presentational element used to display text in italics, much like the `<b>` element was used to display text in bold letters. This is no longer true, as these tags now define semantics rather than typographic appearance. A browser will typically still display the contents of the `<i>` element in italic type, but is, by definition, no longer required to do so. To display text in italic type, authors should use the CSS {{ cssxref("font-style") }} property.
-   Be sure the text in question is not actually more appropriately marked up with another element.
    -   Use [`em`](/html/element/em/) to indicate stress emphasis.
    -   Use [`strong`](/html/element/strong/) to indicate importance, seriousness, or urgency.
    -   Use [`mark`](/html/element/mark/) to indicate relevance.
    -   Use [`cite`](/html/element/cite/) to mark up the name of a work, such as a book, play, or song.
    -   Use [`dfn`](/html/element/dfn/) to mark up the defining instance of a term.

## Examples

This example demonstrates using the `<i>` element to mark text that is in another language.

```html
<p>The Latin phrase <i>Veni, vidi, vici</i> is often
mentioned in music, art, and literature.</p>

```

### Result

{{ EmbedLiveSample("Examples") }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<i>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-i-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<i>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-i-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<b>' in that specification](https://www.w3.org/TR/html401/present/graphics.html#h-15.2.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.i") }}

## See also

-   [`em`](/html/element/em/)
-   Other italicized elements: [`var`](/html/element/var/), [`dfn`](/html/element/dfn/), [`cite`](/html/element/cite/), [`address`](/html/element/address/)