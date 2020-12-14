---
title: 'HTML attribute: size'
tags:
  - Attribute
  - HTML
  - Input
  - Reference
  - Select
permalink: html/attributes/size
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/size'
browserCompact: html.elements.attribute.size
---
The **`size`** attribute defines the width of the [`input`](/html/element/input/) and the height of the [`select`](/html/element/select/) element. For the `input`, if the `type` attribute is [`input/text`](/html/element/input/text/) or [`input/password`](/html/element/input/password/) then it's the number of characters. This must be an integer value 0 or higher. If no `size` is specified, or an invalid value is specified, the input has no size declared, and the form control will be the default width based on the user agent. If CSS targets the element with properties impacting the width, CSS takes precedence.

The `size` attribute has no impact on constraint validation.

## Examples

By adding `size` on some input types, the width of the input can be controlled. Adding size on a select changes the height, definining how many options are visible in the closed state.

```html
<label for="fruit">Enter a fruit</label> <input type="text" size="15" id="fruit">
<label for="vegetable">Enter a vegetable</label> <input type="text" id="vegetable">

<select name="fruits" size="5">
  <option>banana</option>
  <option>cherry</option>
  <option>strawberry</option>
  <option>durian</option>
  <option>blueberry</option>
</select>

<select name="vegetables" size="5">
<option>carrot</option>
<option>cucumber</option>
<option>cauliflower</option>
<option>celery</option>
<option>collard greens</option>
</select>
```

{{ EmbedLiveSample('Examples', '100%', 200) }}

## Specifications

| Specification | Status |
| --- | --- |
| [**HTML Living Standard** The definition of 'size attribute' in that specification](https://html.spec.whatwg.org/multipage/input.html#attr-input-size) | {{ Spec2('HTML WHATWG') }} |
| [**HTML 5.1** The definition of 'size attribute' in that specification](https://www.w3.org/TR/html51/input.html#attr-size-accept) | {{ Spec2('HTML5.1') }} |

## Browser compatibility

{{ Compat("html.elements.attribute.size") }}

## See also

-   `[maxlength](/html/attributes/maxlength)`
-   `[minlength](/html/attributes/minlength)`
-   `[pattern](/html/attributes/pattern)`