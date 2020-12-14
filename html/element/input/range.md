---
title: <input type="range">
tags:
  - Element
  - Forms
  - HTML
  - HTML forms
  - HTML input tag
  - Input
  - Range
  - Reference
  - Web
  - slider
permalink: html/element/input/range
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range'
browserCompact: html.elements.input.input-range
---
{{ HTMLRef("Input_types") }}

[`input`](/html/element/input/) elements of type **`range`** let the user specify a numeric value which must be no less than a given value, and no more than another given value. The precise value, however, is not considered important. This is typically represented using a slider or dial control rather than a text entry box like the [`input/number`](/html/element/input/number/) input type. Because this kind of widget is imprecise, it shouldn't typically be used unless the control's exact value isn't important.

{{ EmbedInteractiveExample("pages/tabbed/input-range.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

If the user's browser doesn't support type `range`, it will fall back and treat it as a `[`input/text`](/html/element/input/text/)` input.

| Property | Value |
| --- | --- |
| **{{ anch("Value") }}** | A {{ domxref("DOMString") }} containing the string representation of the selected numeric value; use {{ domxref("HTMLInputElement.valueAsNumber", "valueAsNumber") }} to get the value as a {{ jsxref("Number") }}. |
| **Events** | {{ event("change") }} and {{ event("input") }} |
| **Supported common attributes** | {{ htmlattrxref("autocomplete", "input") }}, {{ htmlattrxref("list", "input") }}, {{ htmlattrxref("max", "input") }}, {{ htmlattrxref("min", "input") }}, and {{ htmlattrxref("step", "input") }} |
| **IDL attributes** | `list`, `value`, and `valueAsNumber` |
| **Methods** | {{ domxref("HTMLInputElement.stepDown", "stepDown()") }} and {{ domxref("HTMLInputElement.stepUp", "stepUp()") }} |

### Validation

There is no pattern validation available; however, the following forms of automatic validation are performed:

-   If the {{ htmlattrxref("value", "input") }} is set to something which can't be converted into a valid floating-point number, validation fails because the input is suffering from a bad input.
-   The value won't be less than {{ htmlattrxref("min", "input") }}. The default is 0.
-   The value won't be greater than {{ htmlattrxref("max", "input") }}. The default is 100.
-   The value will be a multiple of {{ htmlattrxref("step", "input") }}. The default is 1.

### Value

The {{ htmlattrxref("value", "input") }} attribute contains a {{ domxref("DOMString") }} which contains a string representation of the selected number. The value is never an empty string (`""`). The default value is halfway between the specified minimum and maximum—unless the maximum is actually less than the minimum, in which case the default is set to the value of the `min` attribute. The algorithm for determining the default value is:

```js
defaultValue = (rangeElem.max < rangeElem.min) ? rangeElem.min
               : rangeElem.min + (rangeElem.max - rangeElem.min)/2;
```

If an attempt is made to set the value lower than the minimum, it is set to the minimum. Similarly, an attempt to set the value higher than the maximum results in it being set to the maximum.

## Additional attributes

In addition to the attributes shared by all [`input`](/html/element/input/) elements, range inputs offer the following attributes:

| Attribute | Description |
| --- | --- |
| `{{ anch("list") }}` | The id of the <datalist> element that contains optional pre-defined options |
| `{{ anch("max") }}` | The maximum permitted value |
| `{{ anch("min") }}` | The minimum permitted value |
| `{{ anch("step") }}` | The stepping interval, used both for user interface and validation purposes |

{{ page("/en-US/docs/Web/HTML/Element/input/text", "list", 0, 1, 2) }}

See the [range control with hash marks](#A_range_control_with_hash_marks) below for an example of how the options on a range are denoted in supported browsers

### {{ htmlattrdef("max") }}

The greatest value in the range of permitted values. If the {{ htmlattrxref("value", "input") }} entered into the element exceeds this, the element fails [constraint validation](/guide/html/html5/constraint_validation). If the value of the `[max](/html/attributes/max)` attribute isn't a number, then the element has no maximum value.

This value must be greater than or equal to the value of the `[min](/html/attributes/min)` attribute. See the HTML [`max`](/html/attributes/max) attribute.

### {{ htmlattrdef("min") }}

The lowest value in the range of permitted values. If the {{ htmlattrxref("value", "input") }} of the element is less than this, the element fails [constraint validation](/guide/html/html5/constraint_validation). If a value is specified for `min` that isn't a valid number, the input has no minimum value.

This value must be less than or equal to the value of the `[max](/html/attributes/max)` attribute. See the [HTML `min` attribute.](/html/attributes/min)

### {{ htmlattrdef("step") }}

{{ page("/en-US/docs/Web/HTML/Element/input/number", "step-include") }}

The default stepping value for `range` inputs is 1, allowing only integers to be entered, _unless_ the stepping base is not an integer; for example, if you set `min` to -10 and `value` to 1.5, then a `step` of 1 will allow only values such as 1.5, 2.5, 3.5,... in the positive direction and -0.5, -1.5, -2.5,... in the negative direction. See the [HTML `step` attribute](/html/attributes/step).

### Non Standard Attributes

| Attribute | Description |
| --- | --- |
| `{{ anch("orient") }}` | Sets the orientation of the range slider. **Firefox only.** |

{{ htmlattrdef("orient") }} {{ non-standard_inline }}
: Similar to the -moz-orient non-standard CSS property impacting the [`progress`](/html/element/progress/) and [`meter`](/html/element/meter/) elements, the `orient` attribute defines the orientation of the range slider. Values include `horizontal`, meaning the range is rendered horizontally, and `vertical`, where the range is rendered vertically.

Note: The following input attributes do not apply to the input range: `accept`, `alt`, `checked`, `dirname`, `formaction`, `formenctype`, `formmethod`, `formnovalidate`, `formtarget`, `height`, `maxlength`, `minlength`, `multiple`, `pattern`, `placeholder`, `readonly`, `required`, `size`, `src`, and `width`. Any of these attributes, if included, will be ignored.

## Examples

While the `number` type lets users enter a number with optional constraints forcing their value to be between a minimum and a maximum value, it does require that they enter a specific value. The `range` input type lets you ask the user for a value in cases where the user may not even care—or know—what the specific numeric value selected is.

A few examples of situations in which range inputs are commonly used:

-   Audio controls such as volume and balance, or filter controls.
-   Color configuration controls such as color channels, transparency, brightness, etc.
-   Game configuration controls such as difficulty, visibility distance, world size, and so forth.
-   Password length for a password manager's generated passwords.

As a rule, if the user is more likely to be interested in the percentage of the distance between minimum and maximum values than the actual number itself, a range input is a great candidate. For example, in the case of a home stereo volume control, users typically think "set volume at halfway to maximum" instead of "set volume to 0.5".

### Specifying the minimum and maximum

By default, the minimum is 0 and the maximum is 100. If that's not what you want, you can easily specify different bounds by changing the values of the {{ htmlattrxref("min", "input") }} and/or {{ htmlattrxref("max", "input") }} attributes. These can be any floating-point value.

For example, to ask the user for a value between -10 and 10, you can use:

```html
<input type="range" min="-10" max="10">
```

{{ EmbedLiveSample("Specifying_the_minimum_and_maximum", 600, 40) }}

### Setting the value's granularity

By default, the granularity, is 1, meaning that the value is always an integer. You can change the {{ htmlattrxref("step") }} attribute to control the granularity. For example, If you need a value between 5 and 10, accurate to two decimal places, you should set the value of `step` to 0.01:

```html
<input type="range" min="5" max="10" step="0.01">
```

{{ EmbedLiveSample("Granularity_sample1", 600, 40) }}

If you want to accept any value regardless of how many decimal places it extends to, you can specify a value of `any` for the {{ htmlattrxref("step", "input") }} attribute:

```html
<input type="range" min="0" max="3.14" step="any">
```

{{ EmbedLiveSample("Granularity_sample2", 600, 40) }}

This example lets the user select any value between 0 and π without any restriction on the fractional part of the value selected.

### Adding hash marks and labels

The HTML specification gives browsers some flexibility on how to present the range control. Nowhere is this flexibility more apparent than in the area of hash marks and, to a lesser degree, labels. The specification describes how to add custom points to the range control using the {{ htmlattrxref("list", "input") }} attribute and a [`datalist`](/html/element/datalist/) element, but does not have any requirements or even recommendations for standardized hash or tick marks along the length of the control.

#### Range control mockups

Since browsers have this flexibility, and to date none support all of the features HTML defines for range controls, here are some mockups to show you what you might get on macOS in a browser which supports them.

##### An unadorned range control

This is what you get if you don't specify a {{ htmlattrxref("list", "input") }} attribute, or if the browser doesn't support it.

| HTML | Examples |
| --- | --- |
| 
```html
<input type="range">
```
 | Screenshot |
| ![Screenshot of a plain slider control on macOS](https://mdn.mozillademos.org/files/14989/macslider-plain.png) |
| Live |
| {{ EmbedLiveSample("An_unadorned_range_control",200,55,"","", "nobutton") }} |

##### A range control with hash marks

This range control is using a `list` attribute specifying the ID of a [`datalist`](/html/element/datalist/) which defines a series of hash marks on the control. There are eleven of them, so that there's one at 0% as well as at each 10% mark. Each point is represented using an [`option`](/html/element/option/) element with its {{ htmlattrxref("value", "option") }} set to the range's value at which a mark should be drawn.

| HTML | Examples |
| --- | --- |
| 
```html
<input type="range" list="tickmarks">
<datalist id="tickmarks">
  <option value="0"></option>
  <option value="10"></option>
  <option value="20"></option>
  <option value="30"></option>
  <option value="40"></option>
  <option value="50"></option>
  <option value="60"></option>
  <option value="70"></option>
  <option value="80"></option>
  <option value="90"></option>
  <option value="100"></option>
</datalist>

```
 | Screenshot |
| ![Screenshot of a plain slider control on macOS](https://mdn.mozillademos.org/files/14991/macslider-ticks.png) |
| Live |
| {{ EmbedLiveSample("A_range_control_with_hash_marks_and_labels",200,55,"","", "nobutton") }} |

##### A range control with hash marks and labels

You can add labels to your range control by adding the {{ htmlattrxref("label", "option") }} attribute to the [`option`](/html/element/option/) elements corresponding to the tick marks you wish to have labels for.

| HTML | Examples |
| --- | --- |
| 
```html
<input type="range" list="tickmarks">
<datalist id="tickmarks">
  <option value="0" label="0%"></option>
  <option value="10"></option>
  <option value="20"></option>
  <option value="30"></option>
  <option value="40"></option>
  <option value="50" label="50%"></option>
  <option value="60"></option>
  <option value="70"></option>
  <option value="80"></option>
  <option value="90"></option>
  <option value="100" label="100%"></option>
</datalist>

```
 | Screenshot |
| ![Screenshot of a plain slider control on macOS](https://mdn.mozillademos.org/files/14993/macslider-labels.png) |
| Live |
| {{ EmbedLiveSample("A_range_control_with_hash_marks_and_labels",200,55,"","", "nobutton") }} |

**Note**: Currently, no browser fully supports these features. Firefox doesn't support hash marks and labels at all, for example, while Chrome supports hash marks but doesn't support labels. Version 66 (66.0.3359.181) of Chrome supports labels but the [`datalist`](/html/element/datalist/) tag has to be styled with CSS as its {{ cssxref("display") }} property is set to `none` by default, hiding the labels.

### Change the orientation

By default, if a browser renders a range input as a slider, it will render it so that the knob slides left and right. When supported, we will be able to make the range vertical, to slide up and down with CSS by declaring a height value greater than the width value. This is not actually implemented yet by any of the major browsers. (See Firefox [bug 981916](https://bugzilla.mozilla.org/show_bug.cgi?id=981916), [Chrome bug 341071](https://bugs.chromium.org/p/chromium/issues/detail?id=341071)). It also, perhaps, may still be [under discussion](https://github.com/whatwg/html/issues/4177).

In the meantime, we can make the range vertical by rotating it using using CSS transforms, or, by targeting each browser engine with their own method, which includes setting the {{ cssxref('appearance') }} to `slider-vertical`, by using a non-standard `orient` attribute in Firefox, or by changing the text direction for Internet Explorer and Edge.

Consider this range control:

```html
<input type="range" id="volume" min="0" max="11" value="7" step="1">
```

{{ EmbedLiveSample("Orientation_sample1", 200, 200, "https://mdn.mozillademos.org/files/14983/Orientation_sample1.png") }}

This control is horizontal (at least on most if not all major browers; others might vary).

### Standards

According to the specification, making it vertical requires adding CSS to change the dimensions of the control so that it's taller than it is wide, like this:

#### CSS

```css
#volume {
  height: 150px;
  width: 50px;
}
```

#### HTML

```html
<input type="range" id="volume" min="0" max="11" value="7" step="1">
```

#### Result

{{ EmbedLiveSample("Orientation_sample2", 200, 200, "https://mdn.mozillademos.org/files/14985/Orientation_sample2.png") }}

Unfortunately, no major browsers currently support vertical range controls directly.

### transform: rotate(-90deg)

You can, however, create a vertical range control by drawing a horizontal range control on its side. The easiest way is to use CSS: by applying a {{ cssxref("transform") }} to rotate the element, you can make it vertical. Let's take a look.

#### HTML

The HTML needs to be updated to wrap the [`input`](/html/element/input/) in a [`div`](/html/element/div/) to let us correct the layout after the transform is performed (since transforms don't automatically affect the layout of the page):

```html
<div class="slider-wrapper">
  <input type="range" min="0" max="11" value="7" step="1">
</div>
```

#### CSS

Now we need some CSS. First is the CSS for the wrapper itself; this specifies the display mode and size we want so that the page lays out correctly; in essence, it's reserving an area of the page for the slider so that the rotated slider fits into the reserved space without making a mess of things.

```css
.slider-wrapper {
  display: inline-block;
  width: 20px;
  height: 150px;
  padding: 0;
}

```

Then comes the style information for the `<input>` element within the reserved space:

```css
.slider-wrapper input {
  width: 150px;
  height: 20px;
  margin: 0;
  transform-origin: 75px 75px;
  transform: rotate(-90deg);
}
```

The size of the control is set to be 150 pixels long by 20 pixels tall. The margins are set to 0 and the {{ cssxref("transform-origin") }} is shifted to the middle of the space the slider rotates through; since the slider is configured to be 150 pixels wide, it rotates through a box which is 150 pixels on each side. Offsetting the origin by 75px on each axis means we will rotate around the center of that space. Finally, we rotate counter-clockwise by 90°. The result: a range input which is rotated so the maximum value is at the top and the minimum value is at the bottom.

{{ EmbedLiveSample("transform_rotate-90deg", 200, 200, "https://mdn.mozillademos.org/files/14987/Orientation_sample3.png") }}

### appearance property

The {{ cssxref('appearance') }} property has a non-standard value of `slider-vertical` that, well, makes sliders vertical.

#### HTML

We use the same HTML as in the previous examples:

```html
<input type="range" min="0" max="11" value="7" step="1">

```

#### CSS

We target just the inputs with a type of range:

```css
input[type="range"] {
  -webkit-appearance: slider-vertical;
}
```

{{ EmbedLiveSample("appearance_property", 200, 200) }}

### orient attribute

In Firefox only, there is a non-standard `orient` property.

#### HTML

Use similar HTML as in the previous examples, we add the attribute with a value of `vertical`:

```html
<input type="range" min="0" max="11" value="7" step="1" orient="vertical">

```

{{ EmbedLiveSample("orient_attribute", 200, 200) }}

### writing-mode: bt-lr;

The {{ cssxref('writing-mode') }} property should generally not be used to alter text direction for internationalization or localization purposes, but can be used for special effects. 

#### HTML

We use the same HTML as in the previous examples:

```html
<input type="range" min="0" max="11" value="7" step="1">

```

#### CSS

We target just the inputs with a type of range, changing the writing mode from the default to `bt-lr`, or bottom-to-top and left-to-right:

```css
input[type="range"] {
  writing-mode: bt-lr;
}
```

{{ EmbedLiveSample("writing-mode_bt-lr", 200, 200) }}

### Putting it all together

As each of the above examples works in different browsers, you can put all of them in a single example to make it work cross browser:

#### HTML

We keep the `orient` attribute with a value of `vertical` for Firefox:

```html
<input type="range" min="0" max="11" value="7" step="1" orient="vertical">

```

#### CSS

We target just the inputs with a type of range, changing the writing mode from the default to `bt-lr`, or bottom-to-top and left-to-right, for Edge and Internet Explorer, and add `-webkit-appearance: slider-vertical` for all -webkit-based browsers:

```css
input[type="range"] {
  writing-mode: bt-lr;
  -webkit-appearance: slider-vertical;
}
```

{{ EmbedLiveSample("Putting_it_all_together", 200, 200) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/forms.html#range-state-(type=range) | {{ Spec2('HTML WHATWG') }} | Initial definition |
| [**HTML 5.1** The definition of '<input type="range">' in that specification](https://www.w3.org/TR/html51/sec-forms.html#range-state-typerange) | {{ Spec2('HTML5.1') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.input.input-range") }}

## See also

-   [HTML Forms](/en-US/docs/Learn/HTML/Forms)
-   [`input`](/html/element/input/) and the {{ domxref("HTMLInputElement") }} interface it's based upon
-   `[<input type="number">](/html/element/input/number)`
-   {{ domxref('validityState.rangeOverflow') }} and {{ domxref('validityState.rangeUnderflow') }}
-   [Controlling multiple parameters with ConstantSourceNode](/api/web_audio_api/controlling_multiple_parameters_with_constantsourcenode)
-   [Styling the range element](https://css-tricks.com/sliding-nightmare-understanding-range-input)
-   [Compatibility of CSS properties](/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)