---
title: <slot>
tags:
  - Element
  - HTML
  - HTML Web Components
  - Reference
  - Web Components
  - shadow dom
  - slot
permalink: html/element/slot
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/slot'
browserCompact: html.elements.slot
---
{{ HTMLRef }}

The **HTML `<slot>` element**—part of the [Web Components](/web_components) technology suite—is a placeholder inside a web component that you can fill with your own markup, which lets you create separate DOM trees and present them together.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content) |
| Permitted content | [Transparent](/html/content_categories#transparent_content_model) |
| Events | {{ event("slotchange") }} |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content) |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLSlotElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("name") }}
: The slot's name.

: A **named slot** is a `<slot>` element with a `name` attribute.

## Examples

```html
<template id="element-details-template">
  <style>
    details {font-family: "Open Sans Light", Helvetica, Arial, sans-serif }
    .name {font-weight: bold; color: #217ac0; font-size: 120% }
    h4 {
      margin: 10px 0 -8px 0;
      background: #217ac0;
      color: white;
      padding: 2px 6px;
      border: 1px solid #cee9f9;
      border-radius: 4px;
    }
    .attributes { margin-left: 22px; font-size: 90% }
    .attributes p { margin-left: 16px; font-style: italic }
  </style>
  <details>
    <summary>
      <code class="name">&lt;<slot name="element-name">NEED NAME</slot>&gt;</code>
      <i class="desc"><slot name="description">NEED DESCRIPTION</slot></i>
    </summary>
    <div class="attributes">
      <h4>Attributes</h4>
      <slot name="attributes"><p>None</p></slot>
    </div>
  </details>
  <hr>
</template>
```

**Note**: You can see this complete example in action at [element-details](https://github.com/mdn/web-components-examples/tree/master/element-details) (see it [running live](https://mdn.github.io/web-components-examples/element-details/)). In addition, you can find an explanation at [Using templates and slots](/web_components/using_templates_and_slots).

## Specifications

| Specification | Status | Comments |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<slot>' in that specification](https://html.spec.whatwg.org/multipage/scripting.html#the-slot-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**DOM** The definition of 'Slots' in that specification](https://dom.spec.whatwg.org/#shadow-tree-slots) | {{ Spec2('DOM WHATWG') }} |  |

## Browser compatibility

{{ Compat("html.elements.slot") }}