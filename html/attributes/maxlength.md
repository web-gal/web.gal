---
title: 'HTML attribute: maxlength'
tags:
  - Attribute
  - Attributes
  - Constraint validation
  - HTML
permalink: html/attributes/maxlength
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/maxlength'
draft: true
browserCompact: html.elements.attribute.maxlength
---
The **`maxlength`** attribute defines the maximum number of characters (as UTF-16 code units) the user can enter into an [`input`](/html/element/input/) or [`textarea`](/html/element/textarea/). This must be an integer value 0 or higher. If no maxlength is specified, or an invalid value is specified, the input or textarea has no maximum length.

Any `maxlength` value must be greater than or equal to the value of `minlength`, if present and valid. The input will fail constraint validation if the length of the text value of the field is greater than maxlength UTF-16 code units long. Constraint validation is only applied when the value is changed by the user.

### Constraint validation

While the browser will generally prevent user from entering more text than the maxlength attribute allows, should the length be longer than the maxlength allows, the read-only {{ domxref("ValidityState.tooLong", "tooLong") }} property of a {{ domxref("ValidityState") }} object will be true.

## Examples

```html
<input type="password" maxlength="4"/>

```

{{ EmbedLiveSample('Examples', '100%', 200) }}

## Specifications

| Specification | Status |
| --- | --- |
| [**HTML Living Standard** The definition of 'maxlength attribute' in that specification](https://html.spec.whatwg.org/multipage/input.html#attr-input-maxlength) | {{ Spec2('HTML WHATWG') }} |
| [**HTML 5.1** The definition of 'maxlength attribute' in that specification](https://www.w3.org/TR/html51/input.html#attr-maxlength-accept) | {{ Spec2('HTML5.1') }} |

## Browser compatibility

{{ Compat("html.elements.attribute.maxlength") }}

## See also

-   `[minlength](/html/attributes/minlength)`
-   `[size](/html/attributes/size)`