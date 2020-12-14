---
title: '<dl>: The Description List element'
tags:
  - Element
  - HTML
  - HTML grouping content
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - Reference
  - Web
permalink: html/element/dl
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl'
browserCompact: html.elements.dl
---
{{ HTMLRef }}

The **HTML `<dl>`** element represents a description list. The element encloses a list of groups of terms (specified using the [`dt`](/html/element/dt/) element) and descriptions (provided by [`dd`](/html/element/dd/) elements). Common uses for this element are to implement a glossary or to display metadata (a list of key-value pairs).

{{ EmbedInteractiveExample("pages/tabbed/dl.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), and if the `<dl>` element's children include one name-value group, palpable content. |
| Permitted content | 
Either: Zero or more groups each consisting of one or more [`dt`](/html/element/dt/) elements followed by one or more [`dd`](/html/element/dd/) elements, optionally intermixed with [`script`](/html/element/script/) and [`template`](/html/element/template/) elements.  
Or: One or more [`div`](/html/element/div/) elements, optionally intermixed with [`script`](/html/element/script/) and [`template`](/html/element/template/) elements.

 |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | [`group`](https://w3c.github.io/aria/#group), `[list](/accessibility/aria/roles/list_role)`, [`none`](https://w3c.github.io/aria/#none), [`presentation`](https://w3c.github.io/aria/#presentation) |
| DOM interface | {{ domxref("HTMLDListElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Examples

### Single term and description

```html
<dl>
  <dt>Firefox</dt>
  <dd>
    A free, open source, cross-platform,
    graphical web browser developed by the
    Mozilla Corporation and hundreds of
    volunteers.
  </dd>

  <!-- Other terms and descriptions -->
</dl>

```

{{ EmbedLiveSample("Single_term_and_description") }}

### Multiple terms, single description

```html
<dl>
  <dt>Firefox</dt>
  <dt>Mozilla Firefox</dt>
  <dt>Fx</dt>
  <dd>
    A free, open source, cross-platform,
    graphical web browser developed by the
    Mozilla Corporation and hundreds of
    volunteers.
  </dd>

  <!-- Other terms and descriptions -->
</dl>

```

{{ EmbedLiveSample("Multiple_terms_single_description") }}

### Single term, multiple descriptions

```html
<dl>
  <dt>Firefox</dt>
  <dd>
    A free, open source, cross-platform,
    graphical web browser developed by the
    Mozilla Corporation and hundreds of
    volunteers.
  </dd>
  <dd>
    The Red Panda also known as the Lesser
    Panda, Wah, Bear Cat or Firefox, is a
    mostly herbivorous mammal, slightly larger
    than a domestic cat (60 cm long).
  </dd>

  <!-- Other terms and descriptions -->
</dl>

```

{{ EmbedLiveSample("Single_term_multiple_descriptions") }}

### Multiple terms and descriptions

It is also possible to define multiple terms with multiple corresponding descriptions, by combining the examples above.

### Metadata

Description lists are useful for displaying metadata as a list of key-value pairs.

```html
<dl>
  <dt>Name</dt>
  <dd>Godzilla</dd>
  <dt>Born</dt>
  <dd>1952</dd>
  <dt>Birthplace</dt>
  <dd>Japan</dd>
  <dt>Color</dt>
  <dd>Green</dd>
</dl>

```

Tip: It can be handy to define a key-value separator in the CSS, such as:

```css
dt::after {
  content: ": ";
}
```

### Wrapping name-value groups in [`div`](/html/element/div/) elements

[WHATWG](/en-US/docs/Glossary/WHATWG) HTML allows wrapping each name-value group in a [`dl`](/html/element/dl/) element in a [`div`](/html/element/div/) element. This can be useful when using [microdata](/html/microdata), or when [global attributes](/html/global_attributes) apply to a whole group, or for styling purposes.

```html
<dl>
  <div>
    <dt>Name</dt>
    <dd>Godzilla</dd>
  </div>
  <div>
    <dt>Born</dt>
    <dd>1952</dd>
  </div>
  <div>
    <dt>Birthplace</dt>
    <dd>Japan</dd>
  </div>
  <div>
    <dt>Color</dt>
    <dd>Green</dd>
  </div>
</dl>

```

## Notes

Do not use this element (nor [`ul`](/html/element/ul/) elements) to merely create indentation on a page. Although it works, this is a bad practice and obscures the meaning of description lists.

To change the indentation of a description term, use the [CSS](/en-US/docs/CSS) {{ cssxref("margin") }} property.

## Accessibility concerns

Each screen reader announces `<dl>` content differently. Some screen readers, such as VoiceOver on iOS, will not announce that `<dl>` content is a list. Because of this, make sure each list item's content is written in such a way that it communicates its relationship to the other list items in the list grouping.

-   [CodePen - HTML Buddies: dt & dd](https://codepen.io/aardrian/debug/NzGaKP)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<dl>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-dl-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<dl>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-dl-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<dl>' in that specification](https://www.w3.org/TR/html401/struct/lists.html#h-10.3) | {{ Spec2('HTML4.01') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.dl") }}

## See also

-   [`dt`](/html/element/dt/) element
-   [`dd`](/html/element/dd/) element