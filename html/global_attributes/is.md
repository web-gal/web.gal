---
title: is
tags:
  - Global attributes
  - HTML
  - Reference
  - is
permalink: html/global_attributes/is
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/is'
browserCompact: html.global_attributes.is
---
The **`is`** [global attribute](/html/global_attributes) allows you to specify that a standard HTML element should behave like a defined custom built-in element (see [Using custom elements](/web_components/using_custom_elements) for more details).

This attribute can only be used if the specified custom element name has been successfully [defined](/api/customelementregistry/define) in the current document, and extends the element type it is being applied to.

## Examples

The following code is taken from our [word-count-web-component](https://github.com/mdn/web-components-examples/tree/master/word-count-web-component) example ([see it live also](https://mdn.github.io/web-components-examples/word-count-web-component/)).

```js
// Create a class for the element
class WordCount extends HTMLParagraphElement {
  constructor() {
    // Always call super first in constructor
    super();

    // Constructor contents ommitted for brevity
    ...

  }
}

// Define the new element
customElements.define('word-count', WordCount, { extends: 'p' });
```
```html
<p is="word-count"></p>
```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'is' in that specification](https://html.spec.whatwg.org/multipage/custom-elements.html#attr-is) | {{ Spec2('HTML WHATWG') }} |   |

## Browser compatibility

{{ Compat("html.global_attributes.is") }}

## See also

-   All [global attributes](/html/global_attributes).