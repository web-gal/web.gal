---
title: '<abbr>: The Abbreviation element'
tags:
  - Acronym
  - Definitions
  - Element
  - HTML
  - HTML text-level semantics
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Reference
  - Web
  - abbr
  - abbreviation
  - semantics
permalink: html/element/abbr
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr'
browserCompact: html.elements.abbr
---
{{ HTMLRef }}

The **HTML Abbreviation element** (**`<abbr>`**) represents an abbreviation or acronym; the optional {{ htmlattrxref("title") }} attribute can provide an expansion or description for the abbreviation. If present, `title` must contain this full description and nothing else.

{{ EmbedInteractiveExample("pages/tabbed/abbr.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content) |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content) |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM Interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only supports the [global attributes](/html/global_attributes). The {{ htmlattrxref("title") }} attribute has a specific semantic meaning when used with the `<abbr>` element; it _must_ contain a full human-readable description or expansion of the abbreviation. This text is often presented by browsers as a tooltip when the mouse cursor is hovered over the element.

Each `<abbr>` element you use is independent from all others; providing a `title` for one does not automatically attach the same expansion text to others with the same content text.

## Usage notes

### Typical use cases

It's certainly not required that all abbreviations be marked up using `<abbr>`. There are, though, a few cases where it's helpful to do so:

-   When an abbreviation is used and you want to provide an expansion or definition outside the flow of the document's content, use `<abbr>` with an appropriate {{ htmlattrxref("title") }}.
-   To define an abbreviation which may be unfamiliar to the reader, present the term using `<abbr>` and either a `title` attribute or inline text providing the definition.
-   When an abbreviation's presence in the text needs to be semantically noted, the `<abbr>` element is useful. This can be used, in turn, for styling or scripting purposes.
-   You can use `<abbr>` in concert with [`dfn`](/html/element/dfn/) to establish definitions for terms which are abbreviations or acronyms. See the example {{ anch("Defining an abbreviation") }} below.

### Grammar considerations

In languages with [`grammatical number`](https://en.wikipedia.org/wiki/grammatical_number) (that is, languages where the number of items affects the grammar of a sentence), use the same grammatical number in your `title` attribute as inside your `<abbr>` element. This is especially important in languages with more than two numbers, such as Arabic, but is also relevant in English.

## Default styling

The purpose of this element is purely for the convenience of the author and all browsers display it inline ({{ cssxref('display') }}`: inline`) by default, though its default styling varies from one browser to another:

-   Some browsers, like Internet Explorer, do not style it differently than a [`span`](/html/element/span/) element.
-   Opera, Firefox, and some others add a dotted underline to the content of the element.
-   A few browsers not only add a dotted underline, but also put it in small caps; to avoid this styling, adding something like {{ cssxref('font-variant') }}`: none` in the CSS takes care of this case.

## Examples

### Marking up an abbreviation semantically

To mark up an abbreviation without providing an expansion or description, simply use `<abbr>` without any attributes, as seen in this example.

#### HTML

```html
<p>Using <abbr>HTML</abbr> is fun and easy!</p>
```

#### Result

{{ EmbedLiveSample("Marking_up_an_abbreviation_semantically") }}

### Styling abbreviations

You can use CSS to set a custom style to be used for abbreviations, as seen in this simple example.

#### HTML

```html
<p>Using <abbr>CSS</abbr>, you can style your abbreviations!</p>
```

#### CSS

```css
abbr {
  font-variant: all-small-caps;
}
```

#### Result

{{ EmbedLiveSample("Styling_abbreviations") }}

### Providing an expansion

Adding a {{ htmlattrxref("title") }} attribute lets you provide an expansion or definition for the abbreviation or acronym.

#### HTML

```html
<p>Ashok's joke made me <abbr title="Laugh Out Loud">LOL</abbr> big
time.</p>
```

#### Result

{{ EmbedLiveSample("Providing_an_expansion") }}

### Defining an abbreviation

You can use `<abbr>` in tandem with [`dfn`](/html/element/dfn/) to more formally define an abbreviation, as shown here.

#### HTML

```html
<p><dfn id="html"><abbr title="HyperText Markup Language">HTML</abbr>
</dfn> is a markup language used to create the semantics and structure
of a web page.</p>

<p>A <dfn id="spec">Specification</dfn>
(<abbr title="Specification">spec</abbr>) is a document that outlines
in detail how a technology or API is intended to function and how it is
accessed.</p>
```

#### Result

{{ EmbedLiveSample("Defining_an_abbreviation", 600, 120) }}

## Accessibility concerns

Spelling out the acronym or abbreviation in full the first time it is used on a page is beneficial for helping people understand it, especially if the content is technical or industry jargon.

#### Example

```html
<p>JavaScript Object Notation (<abbr>JSON</abbr>) is a lightweight data-interchange format.</p>

```

This is especially helpful for people who are unfamiliar with the terminology or concepts discussed in the content, people who are new to the language, and people with cognitive concerns.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<abbr>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-abbr-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<abbr>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-abbr-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<abbr>' in that specification](https://www.w3.org/TR/html401/struct/text.html#edef-ABBR) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.abbr") }}

## See also

-   [Using the `<abbr>` element](/en-US/Learn/HTML/Element/abbr)