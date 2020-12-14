---
title: tabindex
tags:
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/tabindex
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/tabindex'
browserCompact: html.global_attributes.tabindex
---
The **`tabindex`** [global attribute](/html/global_attributes) indicates that its element can be focused, and where it participates in sequential keyboard navigation (usually with the Tab key, hence the name).

{{ EmbedInteractiveExample("pages/tabbed/attribute-tabindex.html","tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

It accepts an integer as a value, with different results depending on the integer's value:

-   A _negative value_ (usually `tabindex="-1"`) means that the element is not reachable via sequential keyboard navigation, but could be focused with Javascript or visually by clicking with the mouse. It's mostly useful to create accessible widgets with JavaScript.
    
    A negative value is useful when you have off-screen content that appears on a specific event. The user won't be able to focus any element with a negative `tabindex` using the keyboard, but a script can do so by calling the `focus()` [method](/api/htmlelement/focus).
    
-   `tabindex="0"` means that the element should be focusable in sequential keyboard navigation, after any positive tabindex values and its order is defined by the document's source order.
-   A _positive value_ means the element should be focusable in sequential keyboard navigation, with its order defined by the value of the number. That is, `tabindex="4"` is focused before `tabindex="5"` and `tabindex="0"`, but after `tabindex="3"`. If multiple elements share the same positive `tabindex` value, their order relative to each other follows their position in the document source. The maximum value for `tabindex` is 32767. If not specified, it takes the default value 0.
    
    Avoid using `tabindex` values greater than 0. Doing so makes it difficult for people who rely on assistive technology to navigate and operate page content. Instead, write the document with the elements in a logical sequence.
    

If you set the `tabindex` attribute on a [`div`](/html/element/div/), then its child content cannot be scrolled with the arrow keys unless you set `tabindex` on the content, too. [Check out this fiddle to understand the scrolling effects of `tabindex`](https://jsfiddle.net/jainakshay/0b2q4Lgv/).

## Accessibility concerns

Avoid using the `tabindex` attribute in conjunction with non-[interactive content](/guide/html/content_categories#interactive_content) to make something intended to be interactive focusable by keyboard input. An example of this would be using a [`div`](/html/element/div/) element to describe a button, instead of the [`button`](/html/element/button/) element.

Interactive components authored using non-interactive elements are not listed in the [accessibility tree](/en-US/docs/Learn/Accessibility/What_is_accessibility#Accessibility_APIs). This prevents assistive technology from being able to navigate to and manipulate those components. The content should be semantically described using interactive elements ([`a`](/html/element/a/), [`button`](/html/element/button/), [`details`](/html/element/details/), [`input`](/html/element/input/), [`select`](/html/element/select/), [`textarea`](/html/element/textarea/), etc.) instead. These elements have built-in roles and states that communicate status to the accessibility that would otherwise have to be managed by [ARIA](/accessibility/aria).

-   [Using the tabindex attribute | The Paciello Group](https://developer.paciellogroup.com/blog/2014/08/using-the-tabindex-attribute/)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'tabindex' in that specification](https://html.spec.whatwg.org/multipage/interaction.html#attr-tabindex) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/). |
| [**HTML 5.1** The definition of 'tabindex' in that specification](https://www.w3.org/TR/html51/editing.html#the-tabindex-attribute) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), no change from [**HTML 5**](https://www.w3.org/TR/html52/). |
| [**HTML 5** The definition of 'tabindex' in that specification](https://www.w3.org/TR/html52/editing.html#attr-tabindex) | {{ Spec2('HTML5 W3C') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/). From [**HTML 4.01 Specification**](https://www.w3.org/TR/html401/), the attribute is now supported on all elements (global attributes). |
| [**HTML 4.01 Specification** The definition of 'tabindex' in that specification](https://www.w3.org/TR/html401/interact/forms.html#adef-tabindex) | {{ Spec2('HTML4.01') }} | Only supported on [`a`](/html/element/a/), [`area`](/html/element/area/), [`button`](/html/element/button/), [`input`](/html/element/input/), [`object`](/html/element/object/), [`select`](/html/element/select/), and [`textarea`](/html/element/textarea/). |

## Browser compatibility

The compatibility table on this page is generated from structured data. If you'd like to contribute to the data, check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.global_attributes.tabindex") }}

## See also

-   All [global attributes](/html/global_attributes)
-   {{ domxref("HTMLElement.tabIndex") }} that reflects this attribute
-   Accessibility problems with tabindex: see [Don’t Use Tabindex Greater than 0](http://adrianroselli.com/2014/11/dont-use-tabindex-greater-than-0.html) by Adrian Roselli