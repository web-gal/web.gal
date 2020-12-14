---
title: '<fieldset>: The Field Set element'
tags:
  - Element
  - Forms
  - HTML
  - HTML forms
  - Reference
  - Web
permalink: html/element/fieldset
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset'
browserCompact: html.elements.fieldset
---
{{ HTMLRef }}

The **HTML `<fieldset>` element** is used to group several controls as well as labels ([`label`](/html/element/label/)) within a web form.

{{ EmbedInteractiveExample("pages/tabbed/fieldset.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

As the example above shows, the `<fieldset>` element provides a grouping for a part of an HTML form, with a nested [`legend`](/html/element/legend/) element providing a caption for the `<fieldset>`. It takes few attributes, the most notable of which are `form`, which can contain the `id` of a [`form`](/html/element/form/) on the same page, allowing you to make the `<fieldset>` part of that `<form>` even if it is not nested inside it, and `disabled`, which allows you to disable the `<fieldset>` and all its contents in one go.

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("disabled") }}
: If this Boolean attribute is set, all form controls that are descendants of the `<fieldset>`, are disabled, meaning they are not editable and won't be submitted along with the [`form`](/html/element/form/). They won't receive any browsing events, like mouse clicks or focus-related events. By default browsers display such controls grayed out. Note that form elements inside the [`legend`](/html/element/legend/) element won't be disabled.

{{ htmlattrdef("form") }}
: This attribute takes the value of the {{ htmlattrxref("id") }} attribute of a [`form`](/html/element/form/) element you want the `<fieldset>` to be part of, even if it is not inside the form. Please note that usage of this is confusing — if you want the [`input`](/html/element/input/) elements inside the `<fieldset>` to be associated with the form, you need to use the `form` attribute directly on those elements. You can check which elements are associated with a form via JavaScript, using {{ domxref("HTMLFormElement.elements") }}.

{{ htmlattrdef("name") }}
: The name associated with the group.

**Note**: The caption for the fieldset is given by the first [`legend`](/html/element/legend/) element nested inside it.

## Styling with CSS

There are several special styling considerations for `<fieldset>`.

Its {{ cssxref("display") }} value is `block` by default, and it establishes a [block formatting context](/guide/css/block_formatting_context). If the `<fieldset>` is styled with an inline-level `display` value, it will behave as `inline-block`, otherwise it will behave as `block`. By default there is a `2px` `groove` border surrounding the contents, and a small amount of default padding. The element has {{ cssxref("min-inline-size", "min-inline-size: min-content") }} by default.

If a [`legend`](/html/element/legend/) is present, it is placed over the `block-start` border. The `<legend>` shrink-wraps, and also establishes a formatting context. The `display` value is blockified. (For example, `display: inline` behaves as `block`.)

There will be an anonymous box holding the contents of the `<fieldset>`, which inherits certain properties from the `<fieldset>`. If the `<fieldset>` is styled with `display: grid` or `display: inline-grid`, then the anonymous box will be a grid formatting context. If the `<fieldset>` is styled with `display: flex` or `display: inline-flex`, then the anonymous box will be a flex formatting context. Otherwise, it establishes a block formatting context.

You can feel free to style the `<fieldset>` and `<legend>` in any way you want to suit your page design.

## Examples

### Simple fieldset

This example shows a really simple `<fieldset>` example, with a `<legend>`, and a single control inside it.

```html
<form action="#">
  <fieldset>
    <legend>Simple fieldset</legend>
    <input type="radio" id="radio">
    <label for="radio">Spirit of radio</label>
  </fieldset>
</form>
```

{{ EmbedLiveSample('Simple_fieldset', '100%', '80')  }}

### Disabled fieldset

This example shows a disabled `<fieldset>` with two controls inside it. Note how both the controls are disabled due to being inside a disabled `<fieldset>`.

```html
<form action="#">
  <fieldset disabled>
    <legend>Disabled fieldset</legend>
    <div>
      <label for="name">Name: </label>
      <input type="text" id="name" value="Chris">
    </div>
    <div>
      <label for="pwd">Archetype: </label>
      <input type="password" id="pwd" value="Wookie">
    </div>
  </fieldset>
</form>
```

{{ EmbedLiveSample('Disabled_fieldset', '100%', '110')  }}

## Technical summary

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [sectioning root](/en-US/docs/Sections_and_Outlines_of_an_HTML5_document#sectioning_root), [listed](/html/content_categories#form_listed), [form-associated](/html/content_categories#form-associated_content) element, palpable content. |
| Permitted content | An optional [`legend`](/html/element/legend/) element, followed by flow content. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/html/content_categories#flow_content). |
| Implicit ARIA role | [`group`](https://w3c.github.io/aria/#group) |
| Permitted ARIA roles | [`radiogroup`](https://w3c.github.io/aria/#radiogroup), [`presentation`](https://w3c.github.io/aria/#presentation), [`none`](https://w3c.github.io/aria/#none) |
| DOM interface | {{ domxref("HTMLFieldSetElement") }} |

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<fieldset>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-fieldset-element) | {{ Spec2('HTML WHATWG') }} | Definition of the `fieldset` element |
| [**HTML 5** The definition of '<fieldset>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-fieldset-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<fieldset>' in that specification](https://www.w3.org/TR/html401/interact/forms.html#h-17.10) | {{ Spec2('HTML4.01') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.fieldset") }}

## See also

-   The [`legend`](/html/element/legend/) element
-   The [`input`](/html/element/input/) element
-   The [`label`](/html/element/label/) element
-   The [`form`](/html/element/form/) element