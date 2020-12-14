---
title: 'HTML attribute: min'
tags:
  - Attribute
  - Attributes
  - Constraint validation
  - HTML
  - min
permalink: html/attributes/min
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/min'
browserCompact: html.elements.attributes.min
---
The **`min`** attribute defines the minimum value that is acceptable and valid for the input containing the attribute. If the `[value](/html/element/input#attr-value)` of the element is less than this, the element fails [constraint validation](/guide/html/html5/constraint_validation). This value must be less than or equal to the value of the `max` attribute. If a value is specified for `min` that isn't a valid number, the input has no minimum value.

Valid for the numeric input types, including the [`input/date`](/html/element/input/date/), [`input/month`](/html/element/input/month/), [`input/week`](/html/element/input/week/), [`input/time`](/html/element/input/time/), [`input/datetime-local`](/html/element/input/datetime-local/), [`input/number`](/html/element/input/number/) and [`input/range`](/html/element/input/range/) types, and the [`meter`](/html/element/meter/) element, the `min` attribute is a number that specifies the most negative value a form control to be considered valid.

### Syntax

Syntax for `min` values by input `type`
| Input type | Example | Example |
| --- | --- | --- |
| [`input/date`](/html/element/input/date/) | `yyyy-mm-dd` | `<input type="date" min="2019-12-25" step="1">` |
| [`input/month`](/html/element/input/month/) | `yyyy-mm` | `<input type="month" min="2019-12" step="12">` |
| [`input/week`](/html/element/input/week/) | `yyyy-W##` | `<input type="week" min="2019-W23" step="">` |
| [`input/time`](/html/element/input/time/) | `hh:mm` | `<input type="time" min="09:00" step="900">` |
| [`input/datetime-local`](/html/element/input/datetime-local/) | `yyyy-mm-ddThh:mm` | `<input type="datetime-local" min="2019-12-25T19:30">` |
| [`input/number`](/html/element/input/number/) | [<number>](/css/number) | `<input type="number" min="0" step="5" max="100">` |
| [`input/range`](/html/element/input/range/) | [<number>](/css/number) | `<input type="range" min="60" step="5" max="100">` |

**Note:** When the data entered by the user doesn't adhere to the min value set, the value is considered invalid in contraint validation and will match the {{ cssxref(':invalid') }} pseudoclass

See [Client-side validation](/guide/html/html5/constraint_validation) and {{ domxref("ValidityState.rangeUnderflow", "rangeUnderflow") }} for more information.

For the [`meter`](/html/element/meter/) element, the `min` attribute defines the lower numeric bound of the measured range. This must be less than the minimum value (`[max](/html/attributes/max)` attribute), if specified. In both cases, if omitted, the value defaults to 1.

Syntax for `min` values for other elements
| Input type | Syntax | Example |
| --- | --- | --- |
| [`meter`](/html/element/meter/) | [<number>](/css/number) | `<meter id="fuel" min="0" max="100" low="33" high="66" optimum="80" value="40"> at 40/100</meter>` |

### Impact on step

The value of `min` and `step` define what are valid values, even if the `step` attribute is not included, as `step` defaults to `0`.

We add a big red border around invalid inputs:

```css
input:invalid {
  border: solid red 3px;
}
```

Then define an input with a minimum value of 7.2, omitting the step attribute, wherein it defaults to 1.

```html
<input id="myNumber" name="myNumber" type="number" min="7.2" value="8">
```

Because `step` defaults to 1, valid values include `7.2`, `8.2`, `9.2`, and so on. The value 8 is not valid. As we included an invalid value, supporting browsers will show the value as invalid.

{{ EmbedLiveSample("Impact_on_step",200,55) }}

If not explicitly included, `step` defaults to 1 for `number` and `range`, and 1 unit type (second, week, month, day) for the date/time input types.

## Accessibility concerns

Provide instructions to help users understand how to complete the form and use individual form controls. Indicate any required and optional input, data formats, and other relevant information. When using the min attribute, ensure this minimum requirement is understood by the user. Providing instructions within the [`label`](/html/element/label/) may be sufficient. If providing instructions outside of labels, which allows more flexible positioning and design, consider using `[aria-labelledby](/accessibility/aria/aria_techniques/using_the_aria-labelledby_attribute)` or `[aria-describedby](/accessibility/aria/aria_techniques/using_the_aria-describedby_attribute)`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'min attribute' in that specification](https://html.spec.whatwg.org/multipage/input.html#the-min-and-max-attributes) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'min attribute' in that specification](https://www.w3.org/TR/html52/input.html#the-min-and-max-attributes) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.attributes.min") }}

## See also

-   [step](/html/attributes/step)
-   [max](/html/attributes/max)
-   [constraint validation](/guide/html/html5/constraint_validation)
-   {{ domxref('Constraint_validation') }}
-   {{ domxref('validityState.rangeUnderflow') }}
-   {{ cssxref(':out-of-range') }}
-   [`input`](/html/element/input/)
-   [`input/date`](/html/element/input/date/), [`input/month`](/html/element/input/month/), [`input/week`](/html/element/input/week/), [`input/time`](/html/element/input/time/), [`input/datetime-local`](/html/element/input/datetime-local/), [`input/number`](/html/element/input/number/) and [`input/range`](/html/element/input/range/) types, and the [`meter`](/html/element/meter/)