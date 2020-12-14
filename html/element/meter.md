---
title: '<meter>: The HTML Meter element'
tags:
  - Element
  - HTML
  - HTML forms
  - HTML5
  - Reference
  - Web
permalink: html/element/meter
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meter'
browserCompact: html.elements.meter
---
{{ HTMLRef }}

The **HTML `<meter>` element** represents either a scalar value within a known range or a fractional value.

{{ EmbedInteractiveExample("pages/tabbed/meter.html", "tabbed-shorter") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), labelable content, palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content), but there must be no `<meter>` element among its descendants. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLMeterElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("value") }}
: The current numeric value. This must be between the minimum and maximum values (`min` attribute and `max` attribute) if they are specified. If unspecified or malformed, the value is `0`. If specified, but not within the range given by the `min` attribute and `max` attribute, the value is equal to the nearest end of the range.

**Note:** Unless the `value` attribute is between `0` and `1` (inclusive), the `min` and `max` attributes should define the range so that the `value` attribute's value is within it.

{{ htmlattrdef("min") }}
: The lower numeric bound of the measured range. This must be less than the maximum value (`max` attribute), if specified. If unspecified, the minimum value is `0`.

{{ htmlattrdef("max") }}
: The upper numeric bound of the measured range. This must be greater than the minimum value (`min` attribute), if specified. If unspecified, the maximum value is `1`.

{{ htmlattrdef("low") }}
: The upper numeric bound of the low end of the measured range. This must be greater than the minimum value (`min` attribute), and it also must be less than the high value and maximum value (`high` attribute and `max` attribute, respectively), if any are specified. If unspecified, or if less than the minimum value, the `low` value is equal to the minimum value.

{{ htmlattrdef("high") }}
: The lower numeric bound of the high end of the measured range. This must be less than the maximum value (`max` attribute), and it also must be greater than the low value and minimum value (`low` attribute and `min` attribute, respectively), if any are specified. If unspecified, or if greater than the maximum value, the `high` value is equal to the maximum value.

{{ htmlattrdef("optimum") }}
: This attribute indicates the optimal numeric value. It must be within the range (as defined by the `min` attribute and `max` attribute). When used with the `low` attribute and `high` attribute, it gives an indication where along the range is considered preferable. For example, if it is between the `min` attribute and the `low` attribute, then the lower range is considered preferred. The browser may color the meter's bar differently depending on whether the value is less than or equal to the optimum value.

{{ htmlattrdef("form") }}
: The [`form`](/html/element/form/) element to associate the `<meter>` element with (its _form owner_). The value of this attribute must be the {{ htmlattrxref("id") }} of a `<form>` in the same document. If this attribute is not set, the `<meter>` is associated with its ancestor `<form>` element, if any. This attribute is only used if the `<meter>` element is being used as a form-associated element, such as one displaying a range corresponding to an [`<input type="number">`](/html/element/input/number).

## Examples

### Simple example

#### HTML

```html
<p>Heat the oven to <meter min="200" max="500"
  value="350">350 degrees</meter>.</p>

```

#### Result

{{ EmbedLiveSample("Simple_example", 300, 60) }}

On Google Chrome, the resulting meter looks like this:

![current look of <meter> in google chrome](https://mdn.mozillademos.org/files/17399/Screen_Shot_2020-10-12_at_10.10.53_PM.png)

### High and Low range example

Note that in this example the {{ htmlattrxref("min", "meter") }} attribute is omitted. This is allowed, as it will default to `0`.

#### HTML

```html
<p>He got a <meter low="69" high="80" max="100"
  value="84">B</meter> on the exam.</p>

```

#### Result

{{ EmbedLiveSample("High_and_Low_range_example", 300, 60) }}

On Google Chrome, the resulting meter looks like this:

![red meter in google chrome](https://mdn.mozillademos.org/files/17400/Screen_Shot_2020-10-12_at_10.11.52_PM.png)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<meter>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-meter-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<meter>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-meter-element) | {{ Spec2('HTML5 W3C') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.meter") }}

## See also

-   [`progress`](/html/element/progress/)