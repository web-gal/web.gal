---
title: '<html>: The HTML Document / Root element'
tags:
  - Element
  - HTML
  - HTML Root Element
  - Reference
  - Web
permalink: html/element/html
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html'
browserCompact: html.elements.html
---
{{ HTMLRef }}

The **HTML `<html>` element** represents the root (top-level element) of an HTML document, so it is also referred to as the _root element_. All other elements must be descendants of this element.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None. |
| Permitted content | One [`head`](/html/element/head/) element, followed by one [`body`](/html/element/body/) element. |
| Tag omission | The start tag may be omitted if the first thing inside the `<html>` element is not a comment.  
The end tag may be omitted if the `<html>` element is not immediately followed by a comment. |
| Permitted parents | None. This is the root element of a document. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLHtmlElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("manifest") }} {{ obsolete_inline }}
: Specifies the [URI](/glossary/uri/) of a resource manifest indicating resources that should be cached locally. See [Using the application cache](/html/using_the_application_cache) for details.

{{ htmlattrdef("version") }} {{ obsolete_inline }}
: Specifies the version of the HTML [Document Type Definition](/glossary/dtd/) that governs the current document. This attribute is not needed, because it is redundant with the version information in the document type declaration.

{{ htmlattrdef("xmlns") }}
: Specifies the [XML](/glossary/xml/) [Namespace](/glossary/namespace/) of the document. Default value is `"http://www.w3.org/1999/xhtml"`. This is required in documents parsed with XML [parsers](/glossary/parser/), and optional in text/html documents.

## Example

```html
<!DOCTYPE html>
<html lang="en">
  <head>...</head>
  <body>...</body>
</html>

```

## Accessibility concerns

Providing a {{ htmlattrxref("lang") }} attribute with a [valid IETF identifying language tag](https://www.ietf.org/rfc/bcp/bcp47.txt) on the `<html>` element will help screen reading technology determine the proper language to announce. The identifying language tag should describe the language used by the majority of the content of the page. Without it, screen readers will typically default to the operating system's set language, which may cause mispronunciations.

Including a valid `lang` declaration on the `<html>` element also ensures that important metadata contained in the page's [`head`](/html/element/head/), such as the page's [`title`](/html/element/title/), are also announced properly.

-   [MDN Understanding WCAG, Guideline 3.1 explanations](/accessibility/understanding_wcag/understandable#guideline_3.1_%e2%80%94_readable_make_text_content_readable_and_understandable)
-   [Understanding Success Criterion 3.1.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/2016/NOTE-UNDERSTANDING-WCAG20-20161007/meaning-doc-lang-id.html)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<html>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-html-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<html>' in that specification](https://www.w3.org/TR/html52/semantics.html#the-html-element) | {{ Spec2('HTML5 W3C') }} | Added support for the `manifest` attribute (deprecated later).  
Obsoleted the `version` attribute |
| [**HTML 4.01 Specification** The definition of '<html>' in that specification](https://www.w3.org/TR/html401/struct/global.html#h-7.3) | {{ Spec2('HTML4.01') }} | Deprecated the `version` attribute |

## Browser compatibility

{{ Compat("html.elements.html") }}

## See also

-   MathML top-level element: {{ MathMLElement("math") }}
-   SVG top-level element: {{ SVGElement("svg") }}