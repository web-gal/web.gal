---
title: <label>
tags:
  - Element
  - Forms
  - HTML
  - HTML forms
  - Reference
  - Web
permalink: html/element/label
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label'
browserCompact: html.elements.label
---
{{ HTMLRef }}

The **HTML `<label>` element** represents a caption for an item in a user interface.

{{ EmbedInteractiveExample("pages/tabbed/label.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

Associating a `<label>` with an [`input`](/html/element/input/) element offers some major advantages:

-   The label text is not only visually associated with its corresponding text input; it is programmatically associated with it too. This means that, for example, a screen reader will read out the label when the user is focused on the form input, making it easier for an assistive technology user to understand what data should be entered.
-   You can click the associated label to focus/activate the input, as well as the input itself. This increased hit area provides an advantage to anyone trying to activate the input, including those using a touch-screen device.

To associate the `<label>` with an `<input>` element, you need to give the `<input>` an `id` attribute. The `<label>` then needs a `for` an attribute whose value is the same as the input's `id`.

Alternatively, you can nest the `<input>` directly inside the `<label>`, in which case the `for` and `id` attributes are not needed because the association is implicit:

```html
<label>Do you like peas?
  <input type="checkbox" name="peas">
</label>

```

Other usage notes:

-   The form control that the label is labeling is called the _labeled control_ of the label element. One input can be associated with multiple labels.
-   When a `<label>` is clicked or tapped and it is associated with a form control, the resulting `click` event is also raised for the associated control.

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("for") }}
: The {{ htmlattrxref("id") }} of a [labelable](/guide/html/content_categories#form_labelable) form-related element in the same document as the `<label>` element. The first element in the document with an `id` matching the value of the `for` attribute is the _labeled control_ for this label element if it is a [labelable element](https://html.spec.whatwg.org/multipage/forms.html#category-label). If it is not labelable then the `for` attribute has no effect. If there are other elements that also match the `id` value, later in the document, they are not considered.

**Note**: A `<label>` element can have both a `for` attribute and a contained control element, as long as the `for` attribute points to the contained control element.

## Styling with CSS

There are no special styling considerations for `<label>` elements — structurally they are simple inline elements, and so can be styled in much the same way as a [`span`](/html/element/span/) or [`a`](/html/element/a/) element. You can apply styling to them in any way you want, as long as you don't cause the text to become difficult to read.

## Examples

### Simple label example

```html
<label>Click me <input type="text"></label>
```

{{ EmbedLiveSample('Simple_label_example', '200', '50', '') }}

### Using the "for" attribute

```html
<label for="username">Click me</label>
<input type="text" id="username">
```

{{ EmbedLiveSample('Using_the_for_attribute', '200', '50', '') }}

## Accessibility concerns

### Interactive content

Don't place interactive elements such as [`a`](/html/element/a/) or [`button`](/html/element/button/) inside a `label`. Doing so makes it difficult for people to activate the form input associated with the `label`.

#### Don't

```html
<label for="tac">
  <input id="tac" type="checkbox" name="terms-and-conditions">
  I agree to the <a href="terms-and-conditions.html">Terms and Conditions</a>
</label>

```

#### Do

```html
<label for="tac">
  <input id="tac" type="checkbox" name="terms-and-conditions">
  I agree to the Terms and Conditions
</label>
<p>
  <a href="terms-and-conditions.html">Read our Terms and Conditions</a>
</p>

```

### Headings

Placing [heading elements](/html/element/heading_elements) within a `<label>` interferes with many kinds of assistive technology, because headings are commonly used as [a navigation aid](/html/element/heading_elements#navigation). If the label's text needs to be adjusted visually, use CSS classes applied to the `<label>` element instead.

If a [form](/html/element/form), or a section of a form needs a title, use the [`legend`](/html/element/legend/) element placed within a [`fieldset`](/html/element/fieldset/).

#### Don't

```html
<label for="your-name">
  <h3>Your name</h3>
  <input id="your-name" name="your-name" type="text">
</label>

```

#### Do

```html
<label class="large-label" for="your-name">
  Your name
  <input id="your-name" name="your-name" type="text">
</label> 
```

### Buttons

An [`input`](/html/element/input/) element with a `type="button"` declaration and a valid `value` attribute does not need a label associated with it. Doing so may actually interfere with how assistive technology parses the button input. The same applies for the [`button`](/html/element/button/) element.

## Technical summary

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), [interactive content](/html/content_categories#interactive_content), [form-associated element](/html/content_categories#form-associated_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content), but no descendant `label` elements. No [labelable](/guide/html/content_categories#form_labelable) elements other than the labeled control are allowed. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLLabelElement") }} |

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<label>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-label-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<label>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-label-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<label>' in that specification](https://www.w3.org/TR/html401/interact/forms.html#h-17.9.1) | {{ Spec2('HTML4.01') }} |  |
| [HTML 4.0 Specification  
The definition of '<label>' in that specification.](https://www.w3.org/TR/REC-html40-971218/interact/forms.html#h-17.9.1) | {{ Spec2('HTML4.01') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.label") }}