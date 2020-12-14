---
title: '<style>: The Style Information element'
tags:
  - CSS
  - Element
  - HTML
  - HTML document metadata
  - Reference
  - Style
  - Web
permalink: html/element/style
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style'
browserCompact: html.elements.style
---
{{ HTMLRef }}

The **HTML `<style>` element** contains style information for a document, or part of a document. It contains CSS, which is applied to the contents of the document containing the `<style>` element.

{{ EmbedInteractiveExample("pages/tabbed/style.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

The `<style>` element must be included inside the [`head`](/html/element/head/) of the document. In general, it is better to put your styles in external stylesheets and apply them using [`link`](/html/element/link/) elements.

If you include multiple `<style>` and `<link>` elements in your document, they will be applied to the DOM in the order they are included in the document — make sure you include them in the correct order, to avoid unexpected cascade issues.

In the same manner as `<link>` elements, `<style>` elements can include `media` attributes that contain [media queries](/css/media_queries), allowing you to selectively apply internal stylesheets to your document depending on media features such as viewport width.

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("type") }}
: This attribute defines the styling language as a MIME type (charset should not be specified). This attribute is optional and defaults to `text/css` if it is not specified; values other than the empty string or `text/css` are not used. **Note:** There is very little reason to include this attribute in modern web documents.

{{ htmlattrdef("media") }}
: This attribute defines which media the style should be applied to. Its value is a [media query](/guide/css/media_queries), which defaults to `all` if the attribute is missing.

{{ htmlattrdef("nonce") }}
: A cryptographic nonce (number used once) used to whitelist inline styles in a [style-src Content-Security-Policy](/http/headers/content-security-policy/style-src). The server must generate a unique nonce value each time it transmits a policy. It is critical to provide a nonce that cannot be guessed as bypassing a resource’s policy is otherwise trivial.

{{ htmlattrdef("title") }}
: This attribute specifies [alternative style sheet](/css/alternative_style_sheets) sets.

### Deprecated attributes

{{ htmlattrdef("scoped") }} {{ non-standard_inline }} {{ deprecated_inline }}
: This attribute specifies that the styles only apply to the elements of its parent(s) and children.

This attribute may be re-introduced in the future per [https://github.com/w3c/csswg-drafts/issues/3547](https://github.com/w3c/csswg-drafts/issues/3547). If you want to use the attribute now, you can use a [polyfill](https://github.com/samthor/scoped).

## Examples

### A simple stylesheet

In the following example, we apply a very simple stylesheet to a document:

```html
<!doctype html>
<html>
<head>
  <style>
    p {
      color: red;
    }
  </style>
</head>
<body>
  <p>This is my paragraph.</p>
</body>
</html>
```

{{ EmbedLiveSample('A_simple_stylesheet', '100%', '60') }}

### Multiple style elements

In this example we've included two `<style>` elements — notice how the conflicting declarations in the later `<style>` element override those in the earlier one, if they have equal [specificity](/css/specificity).

```html
<!doctype html>
<html>
<head>
  <style>
    p {
      color: white;
      background-color: blue;
      padding: 5px;
      border: 1px solid black;
    }
  </style>
  <style>
    p {
      color: blue;
      background-color: yellow;
    }
  </style>
</head>
<body>
  <p>This is my paragraph.</p>
</body>
</html>
```

{{ EmbedLiveSample('Multiple_style_elements', '100%', '60') }}

### Including a media query

In this example we build on the previous one, including a `media` attribute on the second `<style>` element so it is only applied when the viewport is less than 500px in width.

```html
<!doctype html>
<html>
<head>
  <style>
    p {
      color: white;
      background-color: blue;
      padding: 5px;
      border: 1px solid black;
    }
  </style>
  <style media="all and (max-width: 500px)">
    p {
      color: blue;
      background-color: yellow;
    }
  </style>
</head>
<body>
  <p>This is my paragraph.</p>
</body>
</html>
```

{{ EmbedLiveSample('Including_a_media_query', '100%', '60') }}

## Technical summary

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Metadata content](/html/content_categories#metadata_content), and if the `scoped` attribute is present: [flow content](/html/content_categories#flow_content). |
| Permitted content | Text content matching the `type` attribute, that is `text/css`. |
| Tag omission | Neither tag is omissible. |
| Permitted parents | Any element that accepts [metadata content](/html/content_categories#metadata_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLStyleElement") }} |

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'style' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-style-element) | {{ Spec2('HTML WHATWG')  }} |  |
| [**HTML 5** The definition of 'style' in that specification](https://www.w3.org/TR/html52/document-metadata.html#the-style-element) | {{ Spec2('HTML5 W3C')  }} | The `type` attribute becomes optional. |
| [**HTML 4.01 Specification** The definition of 'style' in that specification](https://www.w3.org/TR/html401/present/styles.html#h-14.2.3) | {{ Spec2('HTML4.01')  }} |  |

## Browser compatibility

{{ Compat("html.elements.style") }}

## See also

-   The [`link`](/html/element/link/) element, which allows us to apply external stylesheets to a document.
-   [Alternative Style Sheets](/css/alternative_style_sheets)