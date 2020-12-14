---
title: '<dfn>: The Definition element'
tags:
  - Definition
  - Definitions
  - Element
  - HTML
  - HTML text-level semantics
  - Reference
  - Semantic Markup
  - Web
  - dfn
permalink: html/element/dfn
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dfn'
browserCompact: html.elements.dfn
---
{{ HTMLRef }}

The **HTML Definition element** (`**<dfn>**`) is used to indicate the term being defined within the context of a definition phrase or sentence. The [`p`](/html/element/p/) element, the [`dt`](/html/element/dt/)/[`dd`](/html/element/dd/) pairing, or the [`section`](/html/element/section/) element which is the nearest ancestor of the `<dfn>` is considered to be the definition of the term.

{{ EmbedInteractiveExample("pages/tabbed/dfn.html", "tabbed-shorter") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content), but no [`dfn`](/html/element/dfn/) element must be a descendant. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [`term`](https://w3c.github.io/aria/#term) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

In HTML5, the {{ htmlattrxref("title") }} attribute has special meaning, as noted below.

## Usage notes

There are some not-entirely-obvious aspects to using the `<dfn>` element. We examine those here.

### Specifying the term being defined

The term being defined is identified following these rules:

1.  If the `<dfn>` element has a {{ htmlattrxref("title") }} attribute, the value of the `title` attribute is considered to be the term being defined. The element must still have text within it, but that text may be an abbreviation (perhaps using [`abbr`](/html/element/abbr/)) or another form of the term.
2.  If the `<dfn>` contains a single child element and does not have any text content of its own, and the child element is an [`abbr`](/html/element/abbr/) element with a `title` attribute itself, then the exact value of the `<abbr>` element's `title` is the term being defined.
3.  Otherwise, the text content of the `<dfn>` element is the term being defined. This is shown {{ anch("Basic identification of a term", "in the first example below") }}.

If the `<dfn>` element has a `title` attribute, it _must_ contain the term being defined and no other text.

### Links to `<dfn>` elements

If you include an {{ htmlattrxref("id") }} attribute on the `<dfn>` element, you can then link to it using [`a`](/html/element/a/) elements. Such links should be uses of the term, with the intent being that the reader can quickly navigate to the term's definition if they're not already aware of it, by clicking on the term's link.

This is shown in the example under {{ anch("Links to definitions") }} below.

## Examples

Let's take a look at some examples of various usage scenarios.

### Basic identification of a term

This example simply uses a plain `<dfn>` element to identify the location of a term within the definition.

#### HTML

```html
<p>The <strong>HTML Definition element</strong>
(<strong><dfn>&lt;dfn&gt;</dfn></strong>) is used to indicate the
term being defined within the context of a definition phrase or
sentence.</p>
```

Since the `<dfn>` element has no `title`, the text contents of the `<dfn>` element itself are used as the term being defined.

#### Result

This looks like this rendered in your browser:

{{ EmbedLiveSample("Basic_identification_of_a_term", 650, 120) }}

### Links to definitions

To add links to the definitions, you create the link the same way you always do, with the [`a`](/html/element/a/) element.

#### HTML

```html
<p>The <strong>HTML Definition element</strong>
(<strong><dfn id="definition-dfn">&lt;dfn&gt;</dfn></strong>) is
used to indicate the term being defined within the context of a
definition phrase or sentence.</p>

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Graece
donan, Latine voluptatem vocant. Confecta res esset. Duo Reges:
constructio interrete. Scrupulum, inquam, abeunti; </p>

<p>Negare non possum. Dat enim intervalla et relaxat. Quonam modo?
Equidem e Cn. Quid de Pythagora? In schola desinis. </p>

<p>Ubi ut eam caperet aut quando? Cur iustitia laudatur? Aperiendum
est igitur, quid sit voluptas; Quid enim? Non est igitur voluptas
bonum. Urgent tamen et nihil remittunt. Quid enim possumus hoc
agere divinius? </p>

<p>Because of all of that, we decided to use the
<code><a href="#definition-dfn">&lt;dfn&gt;</a></code> element for
this project.</p>
```

Here we see the definition — now with an {{ htmlattrxref("id") }} attribute, `"definition-dfn"`, which can be used as the target of a link. Later on, a link is created using `<a>` with the {{ htmlattrxref("href", "a") }} attribute set to `"#definition-dfn"` to set up the link back to the definition.

#### Result

The resulting content looks like this:

{{ EmbedLiveSample("Links_to_definitions", 650, 300) }}

### Using abbreviations and definitions together

In some cases, you may wish to use an abbreviation for a term when defining it. This can be done by using the `<dfn>` and [`abbr`](/html/element/abbr/) elements in tandem, like this:

#### HTML

```html
<p>The <dfn><abbr title="Hubble Space Telescope">HST</abbr></dfn>
is among the most productive scientific instruments ever constructed.
It has been in orbit for over 20 years, scanning the sky and
returning data and photographs of unprecedented quality and
detail.</p>

<p>Indeed, the <abbr title="Hubble Space Telescope">HST</abbr> has
arguably done more to advance science than any device ever built.</p>
```

Note the `<abbr>` element nested inside the `<dfn>`. The former establishes that the term is an abbreviation ("HST") and specifies the full term ("Hubble Space Telescope") in its `title` attribute. The latter indicates that the abbreviated term represents a term being defined.

#### Result

The output of the above code looks like this:

{{ EmbedLiveSample("Using_abbreviations_and_definitions_together", 650, 200) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<dfn>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-dfn-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<dfn>' in that specification](https://www.w3.org/TR/html52/textlevel-semantics.html#the-dfn-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<dfn>' in that specification](https://www.w3.org/TR/html401/struct/text.html#h-9.2.1) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.dfn") }}

## See also

-   Elements related to definition lists: [`dl`](/html/element/dl/), [`dt`](/html/element/dt/), [`dd`](/html/element/dd/)
-   [`abbr`](/html/element/abbr/)