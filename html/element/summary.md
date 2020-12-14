---
title: '<summary>: The Disclosure Summary element'
tags:
  - Disclosure Box
  - Disclosure Control
  - Disclosure Summary
  - Element
  - HTML
  - HTML interactive elements
  - Reference
  - Summary
  - Web
permalink: html/element/summary
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/summary'
browserCompact: html.elements.summary
---
{{ HTMLRef }}

The **HTML Disclosure Summary element** (**`<summary>`**) element specifies a summary, caption, or legend for a [`details`](/html/element/details/) element's disclosure box. Clicking the `<summary>` element toggles the state of the parent `<details>` element open and closed.

{{ EmbedInteractiveExample("pages/tabbed/summary.html","tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| Permitted content | [Phrasing content](/guide/html/content_categories#phrasing_content) or one element of [Heading content](/guide/html/content_categories#heading_content) |
| Tag omission | None, both the start tag and the end tag are mandatory. |
| Permitted parents | The [`details`](/html/element/details/) element. |
| Implicit ARIA role | `[button](/accessibility/aria/roles/button_role)` |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

## Usage notes

The `<summary>` element's contents can be any heading content, plain text, or HTML that can be used within a paragraph.

A `<summary>` element may _only_ be used as the first child of a `<details>` element. When the user clicks on the summary, the parent `<details>` element is toggled open or closed, and then a {{ event("toggle") }} event is sent to the `<details>` element, which can be used to let you know when this state change occurs.

### Default label text

If a `<details>` element's first child is not a `<summary>` element, the [user agent](/glossary/user_agent/) will use a default string (typically "Details") as the label for the disclosure box.

### Default style

Per the HTML specification, the default style for `<summary>` elements includes `display: list-item`. This makes it possible to change or remove the icon displayed as the disclosure widget next to the label from the default, which is typically a triangle.

You can also change the style to `display: block` to remove the disclosure triangle.

See the {{ anch("Browser compatibility") }} section for details, as not all browsers support full functionality of this element yet.

## Examples

Below are some examples showing `<summary>` in use. You can find more examples in the documentation for the [`details`](/html/element/details/) element.

### Basic example

A simple example showing the use of `<summary>` in a [`details`](/html/element/details/) element:

```html
<details open>
  <summary>Overview</summary>
  <ol>
    <li>Cash on hand: $500.00</li>
    <li>Current invoice: $75.30</li>
    <li>Due date: 5/6/19</li>
  </ol>
</details>
```

{{ EmbedLiveSample("Basic_example", 650, 120) }}

### Summaries as headings

You can use heading elements in `<summary>`, like this:

```html
<details open>
  <summary><h4>Overview</h4></summary>
    <ol>
    <li>Cash on hand: $500.00</li>
    <li>Current invoice: $75.30</li>
    <li>Due date: 5/6/19</li>
  </ol>
</details>
```

{{ EmbedLiveSample("Summaries_as_headings", 650, 120) }}

This currently has some spacing issues that could be addressed using CSS.

**Warning:** Because the `<summary>` element has a default role of [button](/accessibility/aria/roles/button_role) (which strips all roles from child elements), this example will not work for users of assistive technologies such as screen readers. The `<h4>` will have its role removed and thus will not be treated as a heading for these users.

### HTML in summaries

This example adds some semantics to the `<summary>` element to indicate the label as important:

```html
<details open>
  <summary><strong>Overview</strong></summary>
  <ol>
    <li>Cash on hand: $500.00</li>
    <li>Current invoice: $75.30</li>
    <li>Due date: 5/6/19</li>
  </ol>
</details>
```

{{ EmbedLiveSample("HTML_in_summaries", 650, 120) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<summary>' in that specification](https://html.spec.whatwg.org/multipage/interactive-elements.html#the-summary-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5.1** The definition of '<summary>' in that specification](https://www.w3.org/TR/html51/interactive-elements.html#the-summary-element) | {{ Spec2('HTML5.1') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.summary") }}

## See also

-   [`details`](/html/element/details/)