---
title: 'HTML attribute: required'
tags:
  - Attribute
  - Attributes
  - Constraint validation
  - Forms
  - required
permalink: html/attributes/required
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/required'
browserCompact: html.elements.attributes.required
---
The Boolean `**required**` attribute which, if present, indicates that the user must specify a value for the input before the owning form can be submitted. The `required` attribute is supported by `[`input/text`](/html/element/input/text/)`, `[`input/search`](/html/element/input/search/)`, `[`input/url`](/html/element/input/url/)`, `[`input/tel`](/html/element/input/tel/)`, `[`input/email`](/html/element/input/email/)`, `[`input/password`](/html/element/input/password/)`, `[`input/date`](/html/element/input/date/)`, `[`input/month`](/html/element/input/month/)`, `[`input/week`](/html/element/input/week/)`, `[`input/time`](/html/element/input/time/)`, `[`input/datetime-local`](/html/element/input/datetime-local/)`, `[`input/number`](/html/element/input/number/)`, `[`input/checkbox`](/html/element/input/checkbox/)`, `[`input/radio`](/html/element/input/radio/)`, `[`input/file`](/html/element/input/file/)`, [`input`](/html/element/input/) types along with the [`select`](/html/element/select/) and [`textarea`](/html/element/textarea/) form control elements. If present on any of these input types and elements, the {{ cssxref(':required') }} pseudo class will match. If the attribute is not included, the {{ cssxref(':optional') }} pseudo class will match.

The attribute is not supported or relevant to [`input/range`](/html/element/input/range/) and [`input/color`](/html/element/input/color/), as both have default values. It is also not supported on [`input/hidden`](/html/element/input/hidden/) as it can not be expected that a user to fill out a form that is hidden. Nor is it supported on any of the button types, including `image`.

Note `color` and `range` don't support `required`, but type `color` defaults to `#000000`, and `range` defaults to the midpoint between `min` and `max` -- with `min` and `max` defaulting to 0 and 100 respectively in most browsers if not declared -- so always has a value.

When an input has the `required` attribute, the {{ cssxref(":required") }} pseudo-class also applies to it. Conversely, inputs that support the `required` attribute but don't have the attribute set match the {{ cssxref(":optional") }} pseudo-class.

In the case of a same named group of [`input/radio`](/html/element/input/radio/) buttons, if a single radio button in the group has the `required` attribute, a radio button in that group must be checked, although it doesn't have to be the one with the attribute is applied. So to improve code maintenance, it is recommended to either include the `required` attribute in every same-named radio button in the group, or else in none.

In the case of a same named group of [`input/checkbox`](/html/element/input/checkbox/) input types, only the checkboxes with the `required` attribute are required.

Note: Setting `[aria-required](/accessibility/aria/aria_techniques/using_the_aria-required_attribute)="true"` tells a screen reader that an element (any element) is required, but has no bearing on the optionality of the element.

### Attribute interactions

Because a read-only field cannot have a value, `required` does not have any effect on inputs with the `[readonly](/html/attributes/readonly)` attribute also specified.

### Usability

When including the `required` attribute, provide a visible indication near the control informing the user that the [`input`](/html/element/input/), [`select`](/html/element/select/) or [`textarea`](/html/element/textarea/) is required. In addition, target required form controls with the {{ cssxref(':required') }} pseudo-class, styling them in a way to indicate they are required. This improves usability for sighted users. Assistive technology should inform the user that the form control in mandatory based on the required attribute, but adding `[aria-required](/accessibility/aria/aria_techniques/using_the_aria-required_attribute)="true"` doesn't hurt, in case the browser / screen reader combination does not support `required` yet.

### Constraint validation

If the element is required and the element's value is the empty string, then the element is suffering from {{ domxref('ValidityState.valueMissing','valueMissing') }} and the element will match the {{ cssxref(':invalid') }} pseudo class.

## Accessibility concerns

Provide an indication to users informing them the form control is required. Ensure the messaging is multi-faceted, such as thru text, color, markings, and attribute, so that all users understand the requirements whether they have color blindness, cognitive differences, or are using a screen reader.

## Example

### HTML

```html
<form>
  <div class="group">
    <input type="text">
    <label>Normal</label>
  </div>
  <div class="group">
    <input type="text" required="required">
    <label>Required</label>
  </div>
  <input type="submit">
</form>

```

### Result

{{ EmbedLiveSample('Example') }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'required attribute' in that specification](https://html.spec.whatwg.org/multipage/forms.html#attr-input-required) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'required attribute' in that specification](https://www.w3.org/TR/html52/forms.html#attr-input-required) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 5.1** The definition of 'required attribute' in that specification](https://www.w3.org/TR/html51/sec-forms.html#the-required-attribute) | {{ Spec2('HTML5.1') }} |  |

## Browser compatibility

{{ Compat("html.elements.attributes.required") }}

## See also

-   {{ cssxref('validityState.valueMissing') }}
-   {{ cssxref(':required') }} and {{ cssxref(':optional') }}
-   [`input`](/html/element/input/)
-   [`select`](/html/element/select/)