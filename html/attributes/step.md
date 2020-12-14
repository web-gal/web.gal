---
title: 'HTML attribute: step'
tags:
  - Attribute
  - Attributes
  - constrain validation
  - step
permalink: html/attributes/step
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/step'
draft: true
---
The **`step`** attribute is a number that specifies the granularity that the value must adhere to or the keyword `any`. It is valid for the numeric input types, including the [`input/date`](/html/element/input/date/), [`input/month`](/html/element/input/month/), [`input/week`](/html/element/input/week/), [`input/time`](/html/element/input/time/), [`input/datetime-local`](/html/element/input/datetime-local/), [`input/number`](/html/element/input/number/) and [`input/range`](/html/element/input/range/) types.

The `step` sets the _stepping interval_ when clicking up and down spinner buttons, moving a slider left and right on a range, and validating the different date types. If not explicitly included, `step` defaults to 1 for `number` and `range`, and 1 unit type (minute, week, month, day) for the date/time input types. The value can must be a positive number - integer or float -- or the special value `any`, which means no stepping is implied, and any value is allowed (barring other constraints, such as `[min](/html/attributes/min)` and `[max](/html/attributes/max)`).

The default stepping value for `number` inputs is 1, allowing only integers to be entered, _unless_ the stepping base is not an integer. The default stepping value for `time` is 1 second, with 900 being equal to 15 minutes.

Default values for step
| Input type | Value | Example |
| --- | --- | --- |
| [`input/date`](/html/element/input/date/) | 1 (day) | `<input type="date" min="2019-12-25" step="1">` |
| [`input/month`](/html/element/input/month/) | 1 (month) | `<input type="month" min="2019-12" step="12">` |
| [`input/week`](/html/element/input/week/) | 1 (week) | `<input type="week" min="2019-W23" step="2">` |
| [`input/time`](/html/element/input/time/) | 60 (seconds) | `<input type="time" min="09:00" step="900">` |
| [`input/datetime-local`](/html/element/input/datetime-local/) | 1 (day) | 
`<input type="datetime-local" min="019-12-25T19:30" step="7">`

 |
| [`input/number`](/html/element/input/number/) | 1 | `<input type="number" min="0" step="0.1" max="10">` |
| [`input/range`](/html/element/input/range/) | 1 | `<input type="range" min="0" step="2" max="10">` |

If `any` is not explicity set, valid values for the `number`, date/time input types, and `range` input types are equal to the basis for stepping - the `[min](/html/attributes/min)` value and increments of the step value, up to the `[max](/html/attributes/max)` value, if specified. For example, if we have `<input type="number" min="10" step="2">` any even integer, 10 or great, is valid. If omitted, `<input type="number">`, any integer is valid, but floats, like 4.2, are not valid, as `step` defaults to 1. For 4.2 to be valid, `step` would have had to be set to `any`, 0.1, 0.2, or any the min value would have had to be a number ending in .2, such as `<input type="number" min="-5.2">`

### min impact on step

The value of `min` and `step` define what are valid values, even if the `step` attribute is not included, as `step` defaults to `0`.

We add a big red border around invalid inputs:

```css
input:invalid {
  border: solid red 3px;
}
```

Then define an input with a minimum value of 7.2, omitting the step attribute, wherein it defaults to 1.

```html
<input id="myNumber" name="myNumber" type="number" step="2" min="1.2">
```

Valid values include `1.2`, `3.2`, `5.2`, `7.2`, `9.2`, `11.2`, and so on. Integers and even numbers follwed by .2 are not valid. As we included an invalid value, supporting browsers will show the value as invalid. The number spinner, if present, will only show valid float values of `1.2` and greater

{{ EmbedLiveSample("min_impact_on_step",200,55) }}

**Note:** When the data entered by the user doesn't adhere to the stepping configuration, the value is considered invalid in constraint validation and will match the {{ cssxref(":invalid") }} and {{ cssxref(":out-of-range") }} pseudoclasses

See [Client-side validation](/guide/html/html5/constraint_validation) and {{ domxref("ValidityState.stepMismatch", "stepMismatch") }} for more information.

## Accessibility concerns

Provide instructions to help users understand how to complete the form and use individual form controls. Indicate any required and optional input, data formats, and other relevant information. When using the min attribute, ensure this minimum requirement is understood by the user. Providing instructions within the [`label`](/html/element/label/) may be sufficient. If providing instructions outside of labels, which allows more flexible positioning and design, consider using  `[aria-labelledby](/accessibility/aria/aria_techniques/using_the_aria-labelledby_attribute)` or `[aria-describedby](/accessibility/aria/aria_techniques/using_the_aria-describedby_attribute)`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'step attribute' in that specification](https://html.spec.whatwg.org/multipage/input.html#the-step-attribute) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'step attribute' in that specification](https://www.w3.org/TR/html52/input.html#the-step-attribute) | {{ Spec2('HTML5 W3C') }} |  |

## See also

-   `[min](/html/attributes/min)`
-   [constraint validation](/guide/html/html5/constraint_validation)
-   {{ domxref('Constraint validation', "", 1) }} API
-   {{ domxref('validityState.stepMismatch') }}
-   {{ cssxref(':out-of-range') }}
-   [`input`](/html/element/input/)