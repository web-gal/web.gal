---
title: draggable
tags:
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/draggable
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/draggable'
browserCompact: html.global_attributes.draggable
---
The **draggable** [global attribute](/html/global_attributes) is an enumerated attribute that indicates whether the element can be dragged, either with native browser behavior or the [HTML Drag and Drop API](/api/html_drag_and_drop_api).

`draggable` can have the following values:

-   `true`: the element can be dragged.
-   `false`: the element cannot be dragged.

This attribute is _enumerated_ and not _Boolean_. A value of `true` or `false` is mandatory, and shorthand like `<img draggable>` is forbidden. The correct usage is `<img draggable="false">`.

If this attribute is not set, its default value is `auto`, which means drag behavior is the default browser behavior: only text selections, images, and links can be dragged. For other elements, the event {{ domxref('GlobalEventHandlers.ondragstart', 'ondragstart') }} must be set for drag and drop to work, as shown in this [comprehensive example](/api/html_drag_and_drop_api/drag_operations).

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'draggable' in that specification](https://html.spec.whatwg.org/multipage/interaction.html#the-draggable-attribute) | {{ Spec2("HTML WHATWG") }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.2** The definition of 'draggable' in that specification](https://www.w3.org/TR/html52/interaction.html#the-draggable-attribute) | {{ Spec2("HTML5.2") }} | No change |
| [**HTML 5.1** The definition of 'draggable' in that specification](https://www.w3.org/TR/html51/editing.html#the-draggable-attribute) | {{ Spec2("HTML5.1") }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), initial definition |

## Browser compatibility

{{ Compat("html.global_attributes.draggable") }}

## See also

-   All [global attributes](/html/global_attributes).