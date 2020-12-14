---
title: '<figure>: The Figure with Optional Caption element'
tags:
  - Element
  - HTML
  - HTML grouping content
  - Information
  - Presentation
  - Reference
  - figure
permalink: html/element/figure
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure'
browserCompact: html.elements.figure
---
{{ HTMLRef }}

The **HTML `<figure>` (Figure With Optional Caption) element** represents self-contained content, potentially with an optional caption, which is specified using the ([`figcaption`](/html/element/figcaption/)) element. The figure, its caption, and its contents are referenced as a single unit.

{{ EmbedInteractiveExample("pages/tabbed/figure.html","tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [sectioning root](/guide/html/using_html_sections_and_outlines#sectioning_roots), palpable content. |
| Permitted content | A [`figcaption`](/html/element/figcaption/) element, followed by [flow content](/html/content_categories#flow_content); or flow content followed by a [`figcaption`](/html/element/figcaption/) element; or flow content. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [Flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | [figure](/accessibility/aria/roles/figure_role) |
| Permitted ARIA roles | With no [figcaption](/html/element/figcaption) descendant: [any](https://www.w3.org/TR/html-aria/#dfn-any-role), otherwise no permitted roles |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

-   Usually a `<figure>` is an image, illustration, diagram, code snippet, etc., that is referenced in the main flow of a document, but that can be moved to another part of the document or to an appendix without affecting the main flow.
-   Being a [sectioning root](/guide/html/using_html_sections_and_outlines#sectioning_roots), the outline of the content of the `<figure>` element is excluded from the main outline of the document.
-   A caption can be associated with the `<figure>` element by inserting a [`figcaption`](/html/element/figcaption/) inside it (as the first or the last child). The first `<figcaption>` element found in the figure is presented as the figure's caption.

## Examples

### Images

```html
<!-- Just an image -->
<figure>
  <img
  src="https://developer.mozilla.org/static/img/favicon144.png"
  alt="The beautiful MDN logo.">
</figure>

<!-- Image with a caption -->
<figure>
  <img
  src="https://developer.mozilla.org/static/img/favicon144.png"
  alt="The beautiful MDN logo.">
  <figcaption>MDN Logo</figcaption>
</figure>

```

{{ EmbedLiveSample("Images", "100%", 375) }}

### Code snippets

```html
<figure>
  <figcaption>Get browser details using <code>navigator</code>.</figcaption>
  <pre>
function NavigatorExample() {
  var txt;
  txt = "Browser CodeName: " + navigator.appCodeName + "; ";
  txt+= "Browser Name: " + navigator.appName + "; ";
  txt+= "Browser Version: " + navigator.appVersion  + "; ";
  txt+= "Cookies Enabled: " + navigator.cookieEnabled  + "; ";
  txt+= "Platform: " + navigator.platform  + "; ";
  txt+= "User-agent header: " + navigator.userAgent  + "; ";
  console.log("NavigatorExample", txt);
}
  </pre>
</figure>
```

{{ EmbedLiveSample("Code_snippets", "100%", 250) }}

### Quotations

```html
<figure>
  <figcaption><cite>Edsger Dijkstra:</cite></figcaption>
  <blockquote>If debugging is the process of removing software bugs,
  then programming must be the process of putting them in.</blockquote>
</figure>

```

{{ EmbedLiveSample("Quotations") }}

### Poems

```html
<figure>
  <p style="white-space:pre">
Bid me discourse, I will enchant thine ear,
  Or like a fairy trip upon the green,
Or, like a nymph, with long dishevell'd hair,
  Dance on the sands, and yet no footing seen:
Love is a spirit all compact of fire,
  Not gross to sink, but light, and will aspire.</p>
  <figcaption><cite>Venus and Adonis</cite>,
    by William Shakespeare</figcaption>
</figure>
```

{{ EmbedLiveSample("Poems", "100%", 250) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<figure>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-figure-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5.2** The definition of '<figure>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-figure-element) | {{ Spec2('HTML5.2') }} | No changes from HTML 5.0. |
| [**HTML 5** The definition of '<figure>' in that specification](https://www.w3.org/TR/html52/grouping-content.html#the-figure-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.figure") }}

## See also

-   The [`figcaption`](/html/element/figcaption/) element.