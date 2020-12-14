---
title: '<body>: The Document Body element'
tags:
  - Element
  - HTML
  - Reference
  - Sectioning Root Element
  - Sections
  - Web
permalink: html/element/body
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body'
browserCompact: html.elements.body
---
{{ HTMLRef }}

The **HTML `<body>` Element** represents the content of an HTML document. There can be only one `<body>` element in a document.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Sectioning root](/html/sections_and_outlines_of_an_html5_document#sectioning_roots). |
| Permitted content | [Flow content](/html/content_categories#flow_content). |
| Tag omission | The start tag may be omitted if the first thing inside it is not a space character, comment, [`script`](/html/element/script/) element or [`style`](/html/element/style/) element. The end tag may be omitted if the `<body>` element has contents or has a start tag, and is not immediately followed by a comment. |
| Permitted parents | It must be the second element of an [`html`](/html/element/html/) element. |
| Implicit ARIA role | [document](/accessibility/aria/roles/document_role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLBodyElement") }}
-   The `<body>` element exposes the {{ domxref("HTMLBodyElement") }} interface.
-   You can access the `<body>` element through the {{ domxref("document.body") }} property.

 |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("alink") }} {{ obsolete_inline }}
: Color of text for hyperlinks when selected. _This method is non-conforming, use CSS {{ cssxref("color") }} property in conjunction with the {{ cssxref(":active") }} pseudo-class instead._

{{ htmlattrdef("background") }} {{ obsolete_inline }}
: URI of a image to use as a background. _This method is non-conforming, use CSS {{ cssxref("background") }} property on the element instead._

{{ htmlattrdef("bgcolor") }} {{ obsolete_inline }}
: Background color for the document. _This method is non-conforming, use CSS {{ cssxref("background-color") }} property on the element instead._

{{ htmlattrdef("bottommargin") }} {{ obsolete_inline }}
: The margin of the bottom of the body. _This method is non-conforming, use CSS {{ cssxref("margin-bottom") }} property on the element instead._

{{ htmlattrdef("leftmargin") }} {{ obsolete_inline }}
: The margin of the left of the body. _This method is non-conforming, use CSS {{ cssxref("margin-left") }} property on the element instead._

{{ htmlattrdef("link") }} {{ obsolete_inline }}
: Color of text for unvisited hypertext links. _This method is non-conforming, use CSS {{ cssxref("color") }} property in conjunction with the {{ cssxref(":link") }} pseudo-class instead._

{{ htmlattrdef("onafterprint") }}
: Function to call after the user has printed the document.

{{ htmlattrdef("onbeforeprint") }}
: Function to call when the user requests printing of the document.

{{ htmlattrdef("onbeforeunload") }}
: Function to call when the document is about to be unloaded.

{{ htmlattrdef("onblur") }}
: Function to call when the document loses focus.

{{ htmlattrdef("onerror") }}
: Function to call when the document fails to load properly.

{{ htmlattrdef("onfocus") }}
: Function to call when the document receives focus.

{{ htmlattrdef("onhashchange") }}
: Function to call when the fragment identifier part (starting with the hash (`'#'`) character) of the document's current address has changed.

{{ htmlattrdef("onlanguagechange") }} {{ experimental_inline }}
: Function to call when the preferred languages changed.

{{ htmlattrdef("onload") }}
: Function to call when the document has finished loading.

{{ htmlattrdef("onmessage") }}
: Function to call when the document has received a message.

{{ htmlattrdef("onoffline") }}
: Function to call when network communication has failed.

{{ htmlattrdef("ononline") }}
: Function to call when network communication has been restored.

{{ htmlattrdef("onpopstate") }}
: Function to call when the user has navigated session history.

{{ htmlattrdef("onredo") }}
: Function to call when the user has moved forward in undo transaction history.

{{ htmlattrdef("onresize") }}
: Function to call when the document has been resized.

{{ htmlattrdef("onstorage") }}
: Function to call when the storage area has changed.

{{ htmlattrdef("onundo") }}
: Function to call when the user has moved backward in undo transaction history.

{{ htmlattrdef("onunload") }}
: Function to call when the document is going away.

{{ htmlattrdef("rightmargin") }} {{ obsolete_inline }}
: The margin of the right of the body. _This method is non-conforming, use CSS {{ cssxref("margin-right") }} property on the element instead._

{{ htmlattrdef("text") }} {{ obsolete_inline }}
: Foreground color of text. _This method is non-conforming, use CSS {{ cssxref("color") }} property on the element instead._

{{ htmlattrdef("topmargin") }} {{ obsolete_inline }}
: The margin of the top of the body. _This method is non-conforming, use CSS {{ cssxref("margin-top") }} property on the element instead._

{{ htmlattrdef("vlink") }} {{ obsolete_inline }}
: Color of text for visited hypertext links. _This method is non-conforming, use CSS {{ cssxref("color") }} property in conjunction with the {{ cssxref(":visited") }} pseudo-class instead._

## Example

```html
<html>
  <head>
    <title>Document title</title>
  </head>
  <body>
    <p>This is a paragraph</p>
  </body>
</html>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<body>' in that specification](https://html.spec.whatwg.org/multipage/semantics.html#the-body-element) | {{ Spec2('HTML WHATWG') }} | Changed the list of non-conforming features. |
| [**HTML 5** The definition of '<body>' in that specification](https://www.w3.org/TR/html52/sections.html#the-body-element) | {{ Spec2('HTML5 W3C') }} | Obsoleted the formerly deprecated attributes. Defined the behavior of the non-conforming and never standardized `topmargin`, `leftmargin`, `rightmargin` and `bottommargin`. Added the `on*` attributes. |
| [**HTML 4.01 Specification** The definition of '<body>' in that specification](https://www.w3.org/TR/html401/struct/global.html#h-7.5.1) | {{ Spec2('HTML4.01') }} | Deprecated the `alink`, `background`, `bgcolor`, `link`, `text` and `vlink` attributes. |

## Browser compatibility

{{ Compat("html.elements.body") }}

## See also

-   [`html`](/html/element/html/)
-   [`head`](/html/element/head/)