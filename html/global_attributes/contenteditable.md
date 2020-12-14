---
title: contenteditable
tags:
  - Editing
  - Global attributes
  - HTML
  - Reference
  - Text Editing
  - contenteditable
  - text entry
  - text input
permalink: html/global_attributes/contenteditable
mdn: >-
  https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contenteditable
browserCompact: html.global_attributes.contenteditable
---
The **`contenteditable`** [global attribute](/html/global_attributes) is an enumerated attribute indicating if the element should be editable by the user. If so, the browser modifies its widget to allow editing.

{{ EmbedInteractiveExample("pages/tabbed/attribute-contenteditable.html","tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

The attribute must take one of the following values:

-   `true` or an _empty string_, which indicates that the element is editable.
-   `false`, which indicates that the element is not editable.

If the attribute is given without a value, like `<label contenteditable>Example Label</label>`, its value is treated as an empty string.

If this attribute is missing or its value is invalid, its value is _inherited_ from its parent element: so the element is editable if its parent is editable.

Note that although it's allowed values include `true` and `false`, this attribute is an _enumerated_ one and not a _Boolean_ one.

You can set the color used to draw the text insertion [caret](/glossary/caret/) with the CSS {{ cssxref("caret-color") }} property.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'contenteditable' in that specification](https://html.spec.whatwg.org/multipage/editing.html#attr-contenteditable) | {{ Spec2("HTML WHATWG") }} | No change from latest snapshot, [**HTML 5.2**](https://www.w3.org/TR/html52/) |
| [**HTML 5.2** The definition of 'contenteditable' in that specification](https://www.w3.org/TR/html52/editing.html#making-document-regions-editable-the-contenteditable-content-attribute) | {{ Spec2("HTML5.2") }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), no change from [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of 'contenteditable' in that specification](https://www.w3.org/TR/html51/editing.html#making-document-regions-editable-the-contenteditable-content-attribute) | {{ Spec2("HTML5.1") }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), no change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of 'contenteditable' in that specification](https://www.w3.org/TR/html52/editing.html#attr-contenteditable) | {{ Spec2("HTML5 W3C") }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), initial definition. |

## Browser compatibility

{{ Compat("html.global_attributes.contenteditable") }}

## See also

-   [Making content editable](/guide/html/editable_content)
-   All [global attributes](/html/global_attributes)
-   {{ domxref("HTMLElement.contentEditable") }} and {{ domxref("HTMLElement.isContentEditable") }}
-   The CSS {{ cssxref("caret-color") }} property
-   [`HTMLElement` `input` event](/api/htmlelement/input_event)