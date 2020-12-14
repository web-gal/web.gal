---
title: 'HTML attribute: max'
tags:
  - Attribute
  - Attributes
  - Constraint validation
  - HTML
  - Reference
permalink: html/attributes/max
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/max'
browserCompact: html.elements.attributes.max
---
The **`max`** attribute defines the maximum value that is acceptable and valid for the input containing the attribute. If the `[value](/html/element/input#attr-value)` of the element is greater than this, the element fails [constraint validation](/guide/html/html5/constraint_validation). This value must be greater than or equal to the value of the [`min`](min) attribute. If the `max` attribute is present by is not specified or is invalid, no `max` value is applied. If the `max` attribute is valid and a non-empty value is greater than the maximum allowed by the `max` attribute, constraint validation will prevent form submission.

Valid for the numeric input types, including the [`input/date`](/html/element/input/date/), [`input/month`](/html/element/input/month/), [`input/week`](/html/element/input/week/), [`input/time`](/html/element/input/time/), [`input/datetime-local`](/html/element/input/datetime-local/), [`input/number`](/html/element/input/number/) and [`input/range`](/html/element/input/range/) types, and both the [`progress`](/html/element/progress/) and [`meter`](/html/element/meter/) elements, the `max` attribute is a number that specifies the most positive value a form control to be considered valid.

If the value exceeds the max value allowed, the {{ domxref('validityState.rangeOverflow') }} will be true, and the the control will be matched by the {{ cssxref(':out-of-range') }} and {{ cssxref(':invalid') }} pseudo-classes.

### Syntax

Syntax for `max` values by input `type`
| Input type | Syntax | Example |
| --- | --- | --- |
| [`input/date`](/html/element/input/date/) | `yyyy-mm-dd` | `<input type="date" max="2019-12-25" step="1">` |
| [`input/month`](/html/element/input/month/) | `yyyy-mm` | `<input type="month" max="2019-12" step="12">` |
| [`input/week`](/html/element/input/week/) | `yyyy-W##` | `<input type="week" max="2019-W23" step="">` |
| [`input/time`](/html/element/input/time/) | `hh:mm` | `<input type="time" max="17:00" step="900">` |
| [`input/datetime-local`](/html/element/input/datetime-local/) | `yyyy-mm-ddThh:mm` | `<input type="datetime-local" min="2019-12-25T23:59">` |
| [`input/number`](/html/element/input/number/) | [<number>](/css/number) | `<input type="number" min="0" step="5" max="100">` |
| [`input/range`](/html/element/input/range/) | [<number>](/css/number) | `<input type="range" min="60" step="5" max="100">` |

**Note:** When the data entered by the user doesn't adhere to the maximum value set, the value is considered invalid in contraint validation and will match the {{ cssxref(':invalid') }} and {{ cssxref(':out-of-range') }} pseudo-classes.

See [Client-side validation](/guide/html/html5/constraint_validation) and {{ domxref("ValidityState.rangeOverflow", "rangeOverflow") }} for more information.

For the [`progress`](/html/element/progress/) element, the `max` attribute describes how much work the task indicated by the `progress` element requires. If present, must have a value greater than zero and be a valid floating point number. For the [`meter`](/html/element/meter/) element, the `max` attribute defines the upper numeric bound of the measured range. This must be greater than the minimum value (`[min](/html/attributes/min)` attribute), if specified. In both cases, if omitted, the value defaults to 1.

Syntax for `max` values for other elements
| Input type | Syntax | Example |
| --- | --- | --- |
| [`progress`](/html/element/progress/) | [<number>](/css/number) | `<progress id="file" max="100" value="70"> 70% </progress>` |
| [`meter`](/html/element/meter/) | [<number>](/css/number) | `<meter id="fuel" min="0" max="100" low="33" high="66" optimum="80" value="40"> at 40/100</meter>` |

## Accessibility concerns

Provide instructions to help users understand how to complete the form and use individual form controls. Indicate any required and optional input, data formats, and other relevant information. When using the `max` attribute, ensure this maximum requirement is understood by the user. Providing instructions within the [`label`](/html/element/label/) may be sufficient. If providing instructions outside of labels, which allows more flexible positioning and design, consider using `[aria-labelledby](/accessibility/aria/aria_techniques/using_the_aria-labelledby_attribute)` or `[aria-describedby](/accessibility/aria/aria_techniques/using_the_aria-describedby_attribute)`.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'max attribute' in that specification](https://html.spec.whatwg.org/multipage/input.html#the-min-and-max-attributes) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'max attribute' in that specification](https://www.w3.org/TR/html52/input.html#the-min-and-max-attributes) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML Living Standard** The definition of 'progress element' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-progress-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'progress element' in that specification](https://www.w3.org/TR/html52/forms.html#the-progress-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML Living Standard** The definition of 'meter element' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-meter-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'meter element' in that specification](https://www.w3.org/TR/html52/forms.html#the-meter-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.attributes.max") }}

## See also

-   [`step`](/html/attributes/step)
-   [`min`](/html/attributes/min)
-   other meter attributes: [`low`](/html/attributes/low), [`high`](/html/attributes/high), [`optimum`](/html/attributes/optimum)
-   [Constraint validation](/guide/html/html5/constraint_validation)
-   [Constraint validation API](/api/constraint_validation)
-   {{ domxref('validityState.rangeOverflow') }}
-   {{ cssxref(':out-of-range') }}
-   [`input`](/html/element/input/)