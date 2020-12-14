---
title: spellcheck
tags:
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/spellcheck
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/spellcheck'
browserCompact: html.global_attributes.spellcheck
---
The **`spellcheck`** [global attribute](/html/global_attributes) is an enumerated attribute defines whether the element may be checked for spelling errors.

{{ EmbedInteractiveExample("pages/tabbed/attribute-spellcheck.html","tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

It may have the following values:

-   `true`, which indicates that the element should be, if possible, checked for spelling errors;
-   `false`, which indicates that the element should not be checked for spelling errors.

**Note:** The `spellcheck` attribute is an _enumerated_ one and not a _Boolean_ one. This means that the explicit usage of one of the values `true` or `false` is mandatory, and that a shorthand like `<textarea spellcheck></textarea>` is not allowed. The correct usage is `<textarea spellcheck="true"></textarea>`.

If this attribute is not set, its default value is element-type and browser-defined. This default value may also be _inherited_, which means that the element content will be checked for spelling errors only if its nearest ancestor has a _spellcheck_ state of `true`.

This attribute is merely a hint for the browser: browsers are not required to check for spelling errors. Typically non-editable elements are not checked for spelling errors, even if the `spellcheck` attribute is set to `true` and the browser supports spellchecking.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'spellcheck' in that specification](https://html.spec.whatwg.org/multipage/interaction.html#spelling-and-grammar-checking) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of 'spellcheck' in that specification](https://www.w3.org/TR/html51/editing.html#spelling-and-grammar-checking) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), initial definition |

## Browser compatibility

{{ Compat("html.global_attributes.spellcheck") }}

## See also

-   All [global attributes](/html/global_attributes).