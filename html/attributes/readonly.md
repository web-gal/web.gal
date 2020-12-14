---
title: 'HTML attribute: readonly'
tags:
  - Attribute
  - Attributes
  - Constraint validation
  - Forms
  - required
permalink: html/attributes/readonly
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/readonly'
draft: true
browserCompact: html.elements.attributes.readonly
---
The Boolean `**readonly**` attribute, when present, makes the element not mutable, meaning the user can not edit the control. If the `readonly` attribute is specified on an input element, because the user can not edit the input, the element does not participate in constraint validation.

The `readonly` attribute is supported by  `[`input/text`](/html/element/input/text/)`, `[`input/search`](/html/element/input/search/)`, `[`input/url`](/html/element/input/url/)`, `[`input/tel`](/html/element/input/tel/)`, `[`input/email`](/html/element/input/email/)`, `[`input/password`](/html/element/input/password/)`, `[`input/date`](/html/element/input/date/)`, `[`input/month`](/html/element/input/month/)`, `[`input/week`](/html/element/input/week/)`, `[`input/time`](/html/element/input/time/)`, `[`input/datetime-local`](/html/element/input/datetime-local/)`, and `[`input/number`](/html/element/input/number/)``[`input`](/html/element/input/)` types and the `[`textarea`](/html/element/textarea/)` form control elements. If present on any of these input types and elements, the `{{ cssxref(':read-only') }}` pseudo class will match. If the attribute is not included, the `{{ cssxref(':read-write') }}` pseudo class will match.

The attribute is not supported or relevant to `[`select`](/html/element/select/)` or input types that are already not mutable, such as [`input/checkbox`](/html/element/input/checkbox/) and [`input/radio`](/html/element/input/radio/) or cannot, by definition, start with a value, such as the [`input/file`](/html/element/input/file/)  input type. [`input/range`](/html/element/input/range/) and [`input/color`](/html/element/input/color/), as both have default values. It is also not supported on [`input/hidden`](/html/element/input/hidden/) as it can not be expected that a user to fill out a form that is hidden. Nor is it supported on any of the button types, including `image`.

**Note:** Only text controls can be made read-only, since for other controls (such as checkboxes and buttons) there is no useful distinction between being read-only and being disabled, so the `readonly` attribute does not apply.

When an input has the `readonly` attribute, the {{ cssxref(":read-only") }} pseudo-class also applies to it. Conversely, inputs that support the `readonly` attribute but don't have the attribute set match the {{ cssxref(":read-write") }} pseudo-class.

### Attribute interactions

The difference between `[disabled](/html/attributes/disabled)` and `readonly` is that read-only controls can still function and are still focusable, whereas disabled controls can not receive focus and are not submitted with the form and generally do not function as controls until they are enabled.

Because a read-only field cannot have it's value changed by a user interaction, `[required](/html/attributes/required)` does not have any effect on inputs with the `readonly` attribute also specified.

The only way to modify dynamically the value of the readonly attribute is through a script.

**Note:** The `required` attribute is not permitted on inputs with the `readonly` attribute specified.

### Usability

Browsers display the `readonly` attribute...

### Constraint validation

If the element is readonly, then the element's value can not be updated by the user, and does not participate in constraint validation.

## Example

### HTML

```html
<div class="group">
  <input type="textbox" value="Some value" readonly="readonly"/>
  <label>Textbox</label>
</div>
<div class="group">
  <input type="date" value="2020-01-01" readonly="readonly"/>
  <label>Date</label>
</div>
<div class="group">
  <input type="email" value="Some value" readonly="readonly"/>
  <label>Email</label>
</div>
<div class="group">
  <input type="password" value="Some value" readonly="readonly"/>
  <label>Password</label>
</div>
<div class="group">
  <textarea readonly="readonly">Some value</textarea>
  <label>Message</label>
</div>

```

### Result

{{ EmbedLiveSample('Example') }}

## Examples

```html
<fieldset>
  <legend>Checkboxes buttons</legend>
  <p><label>
    <input type="checkbox" name="chbox" value="regular"> Regular
  </label></p>
  <p><label>
    <input type="checkbox" name="chbox" value="readonly" readonly> readonly
  </label></p>
  <p><label>
    <input type="checkbox" name="chbox" value="disabled" disabled> disabled
  </label></p>
</fieldset>
<fieldset>
  <legend>Radio buttons</legend>
  <p><label>
    <input type="radio" name="radio" value="regular"> Regular
  </label></p>
  <p><label>
    <input type="radio" name="radio" value="readonly" readonly> readonly
  </label></p>
  <p><label>
    <input type="radio" name="radio" value="disabled" disabled> disabled
  </label></p>
</fieldset>
```

{{ EmbedLiveSample('Examples', 500, 200) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'readonly attribute' in that specification](https://html.spec.whatwg.org/multipage/forms.html#attr-input-readonly) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'readonly attribute' in that specification](https://www.w3.org/TR/html52/forms.html#attr-input-readonly) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 5.1** The definition of 'readonly attribute' in that specification](https://www.w3.org/TR/html51/sec-forms.html#the-readonly-attribute) | {{ Spec2('HTML5.1') }} |  |

## Browser compatibility

{{ Compat("html.elements.attributes.readonly") }}

## See also

-   {{ cssxref(':read-only') }} and {{ cssxref(':read-write') }}
-   [`input`](/html/element/input/)
-   [`select`](/html/element/select/)