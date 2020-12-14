---
title: hidden
tags:
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/hidden
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/hidden'
browserCompact: html.global_attributes.hidden
---
The **`hidden`** [global attribute](/html/global_attributes) is a Boolean attribute indicating that the element is not yet, or is no longer, _relevant_. For example, it can be used to hide elements of the page that can't be used until the login process has been completed. Browsers won't render elements with the `hidden` attribute set.

{{ EmbedInteractiveExample("pages/tabbed/attribute-hidden.html","tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

The `hidden` attribute must not be used to hide content just from one presentation. If something is marked hidden, it is hidden from all presentations, including, for instance, screen readers.

Hidden elements shouldn't be linked from non-hidden elements, and elements that are descendants of a hidden element are still active, which means that script elements can still execute and form elements can still submit. Elements and scripts may, however, refer to elements that are hidden in other contexts.

For example, it would be incorrect to use the `href` attribute to link to a section marked with the `hidden` attribute. If the content is not applicable or relevant, then there is no reason to link to it.

It would be fine, however, to use the ARIA `aria-describedby` attribute to refer to descriptions that are themselves hidden. While hiding the descriptions implies that they are not useful on their own, they could be written in such a way that they are useful in the specific context of being referenced from the element that they describe.

Similarly, a canvas element with the `hidden` attribute could be used by a scripted graphics engine as an off-screen buffer, and a form control could refer to a hidden form element using its form attribute.

**Note:** Changing the value of the CSS {{ cssxref("display") }} property on an element with the `hidden` attribute overrides the behavior. For instance, elements styled `display: flex` will be displayed despite the `hidden` attribute's presence.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'hidden' in that specification](https://html.spec.whatwg.org/multipage/interaction.html#the-hidden-attribute) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML Living Standard** The definition of 'Hidden elements' in that specification](https://html.spec.whatwg.org/multipage/rendering.html#hiddenCSS) | {{ Spec2('HTML WHATWG') }} | Defines the suggested default rendering of the `hidden` attribute using CSS |
| [**HTML 5.1** The definition of 'hidden' in that specification](https://www.w3.org/TR/html51/editing.html#the-hidden-attribute) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), initial definition |

## Browser compatibility

{{ Compat("html.global_attributes.hidden") }}

## See also

-   {{ DOMxRef("HTMLElement.hidden") }}
-   All [global attributes](/html/global_attributes).
-   [`aria-hidden` attribute](/accessibility/aria/aria_techniques/using_the_aria-hidden_attribute)