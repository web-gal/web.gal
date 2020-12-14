---
title: '<details>: The Details disclosure element'
tags:
  - Disclosure Box
  - Disclosure Widget
  - Element
  - HTML
  - HTML interactive elements
  - Reference
  - Web
  - details
permalink: html/element/details
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details'
browserCompact: html.elements.details
---
{{ HTMLRef }}

The **HTML Details Element (`<details>`)** creates a disclosure widget in which information is visible only when the widget is toggled into an "open" state. A summary or label can be provided using the [`summary`](/html/element/summary/) element.

A disclosure widget is typically presented onscreen using a small triangle which rotates (or twists) to indicate open/closed status, with a label next to the triangle. If the first child of the `<details>` element is a `<summary>`, the contents of the `<summary>` element are used as the label for the disclosure widget.

{{ EmbedInteractiveExample("pages/tabbed/details.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

**Note:** The common use of a triangle which rotates or twists around to represent opening or closing the widget is why these are sometimes called "twisties."

A `<details>` widget can be in one of two states. The default _closed_ state displays only the triangle and the label inside `<summary>` (or a [user agent](/glossary/user_agent/)-defined default string if no `<summary>`). This might look like the following:

![Screenshot of closed <details> widget. A black left-pointing triangle sits to the right of the text “System Requirements”.](https://mdn.mozillademos.org/files/15717/details-closed.png)

Here we see a standard disclosure widget with the label "System Requirements", in its default closed state. When the user clicks on the widget or focuses it then presses the space bar, it "twists" open, revealing its contents:

![Screenshot of open <details> widget. The triangle now points downward, and a detailed description of what “System Requirements” means is shown.](https://mdn.mozillademos.org/files/15718/details-open.png)

From there, you can use CSS to style the disclosure widget, and you can programmatically open and close the widget by setting/removing its {{ htmlattrxref("open", "details") }} attribute.

By default when closed, the widget is only tall enough to display the disclosure triangle and summary. When open, it expands to display the details contained within.

**Note:** Unfortunately, at this time there's no built-in way to animate the transition between open and closed.

Fully standards-compliant implementations automatically apply the CSS `{{ cssxref("display") }}: list-item` to the [`summary`](/html/element/summary/) element. You can use this to customize its appearance further. See {{ anch("Customizing the disclosure widget") }} for further details.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), sectioning root, interactive content, palpable content. |
| Permitted content | One [`summary`](/html/element/summary/) element followed by [flow content](/html/content_categories#flow_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | [`group`](https://w3c.github.io/aria/#group) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLDetailsElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("open") }}
: This Boolean attribute indicates whether or not the details — that is, the contents of the `<details>` element — are currently visible. The default, `false`, means the details are not visible.

## Events

In addition to the usual events supported by HTML elements, the `<details>` element supports the {{ event("toggle") }} event, which is dispatched to the `<details>` element whenever its state changes between open and closed. It is sent _after_ the state is changed, although if the state changes multiple times before the browser can dispatch the event, the events are coalesced so that only one is sent.

You can use an event listener for the `toggle` event to detect when the widget changes state:

```js
details.addEventListener("toggle", event => {
  if (details.open) {
    /* the element was toggled open */
  } else {
    /* the element was toggled closed */
  }
});
```

## Examples

### A simple disclosure example

This example shows a `<details>` element with no provided summary.

```html
<details>
  <p>Requires a computer running an operating system. The computer
  must have some memory and ideally some kind of long-term storage.
  An input device as well as some form of output device is
  recommended.</p>
</details>
```

In this situation, the browser will use a default summary string (usually "Details"). Here's what your browser does with it:

{{ EmbedLiveSample("A_simple_disclosure_example", 650, 150) }}

### Providing a summary

This example adds a summary to the above example by using the [`summary`](/html/element/summary/) element inside `<details>`, like this:

```html
<details>
  <summary>System Requirements</summary>
  <p>Requires a computer running an operating system. The computer
  must have some memory and ideally some kind of long-term storage.
  An input device as well as some form of output device is
  recommended.</p>
</details>
```

The result from this HTML is this:

{{ EmbedLiveSample("Providing_a_summary", 650, 150) }}

### Creating an open disclosure box

To start the `<details>` box in its open state, add the Boolean `open` attribute:

```html
<details open>
  <summary>System Requirements</summary>
  <p>Requires a computer running an operating system. The computer
  must have some memory and ideally some kind of long-term storage.
  An input device as well as some form of output device is
  recommended.</p>
</details>
```

This results in:

{{ EmbedLiveSample("Creating_an_open_disclosure_box", 650, 150) }}

### Customizing the appearance

Now let's apply some CSS to customize the appearance of the disclosure box.

#### CSS

```css
details {
  font: 16px "Open Sans", Calibri, sans-serif;
  width: 620px;
}

details > summary {
  padding: 2px 6px;
  width: 15em;
  background-color: #ddd;
  border: none;
  box-shadow: 3px 3px 4px black;
  cursor: pointer;
}

details > p {
  border-radius: 0 0 10px 10px;
  background-color: #ddd;
  padding: 2px 6px;
  margin: 0;
  box-shadow: 3px 3px 4px black;
}

```

This CSS creates a look similar to a tabbed interface, where clicking the tab opens it to reveal its contents.

#### HTML

```html
<details>
  <summary>System Requirements</summary>
  <p>Requires a computer running an operating system. The computer
  must have some memory and ideally some kind of long-term storage.
  An input device as well as some form of output device is
  recommended.</p>
</details>
```

#### Result

{{ EmbedLiveSample("Customizing_the_appearance", 650, 150) }}

### Customizing the disclosure widget

The disclosure triangle itself can be customized, although this is not as broadly supported. There are variations in how browsers support this customization due to experimental implementations as the element was standardized, so we'll have to use multiple approaches for a while.

The [`summary`](/html/element/summary/) element supports the {{ cssxref("list-style") }} shorthand property and its longhand properties, such as {{ cssxref("list-style-type") }}, to change the disclosure triangle to whatever you choose (usually with {{ cssxref("list-style-image") }}). For example, we can remove the disclosure widget icon by setting `list-style: none`.

Chrome doesn't support this yet, however, so we also need to use its non-standard `::-webkit-details-marker` [pseudo-element](/css/pseudo-elements) to customize the appearance in that browser.

#### CSS

```css
details {
  font: 16px "Open Sans", Calibri, sans-serif;
  width: 620px;
}

details > summary {
  padding: 2px 6px;
  width: 15em;
  background-color: #ddd;
  border: none;
  box-shadow: 3px 3px 4px black;
  cursor: pointer;
  list-style: none;
}

details > summary::-webkit-details-marker {
  display: none;
}

details > p {
  border-radius: 0 0 10px 10px;
  background-color: #ddd;
  padding: 2px 6px;
  margin: 0;
  box-shadow: 3px 3px 4px black;
}

```

This CSS creates a look similar to a tabbed interface, where activating the tab expands and opens it to reveal its contents.

#### HTML

```html
<details>
  <summary>System Requirements</summary>
  <p>Requires a computer running an operating system. The computer
  must have some memory and ideally some kind of long-term storage.
  An input device as well as some form of output device is
  recommended.</p>
</details>
```

#### Result

{{ EmbedLiveSample("Customizing_the_disclosure_widget", 650, 150) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<details>' in that specification](https://html.spec.whatwg.org/multipage/interactive-elements.html#the-details-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5.1** The definition of '<details>' in that specification](https://www.w3.org/TR/html51/interactive-elements.html#the-details-element) | {{ Spec2('HTML5.1') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.details") }}

## See also

-   [`summary`](/html/element/summary/)