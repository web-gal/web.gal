---
title: <input type="month">
tags:
  - Date picker
  - Element
  - Form input
  - Forms
  - HTML
  - HTML forms
  - HTML input
  - Input
  - Input Element
  - Input Type
  - Number
  - Reference
  - month
permalink: html/element/input/month
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/month'
browserCompact: html.elements.input.input-month
---
{{ HTMLRef("Input_types") }}

[`input`](/html/element/input/) elements of type **`month`** create input fields that let the user enter a month and year allowing a month and year to be easily entered. The value is a string whose value is in the format "`YYYY-MM`", where `YYYY` is the four-digit year and `MM` is the month number.

{{ EmbedInteractiveExample("pages/tabbed/input-month.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

The control's UI varies in general from browser to browser; at the moment support is patchy, with only Chrome/Opera and Edge on desktop — and most modern mobile browser versions — having usable implementations. In browsers that don't support `month` inputs, the control degrades gracefully to a simple `[<input type="text">](/html/element/input/text)`, although there may be automatic validation of the entered text to ensure it's formatted as expected.

For those of you using a browser that doesn't support `month`, the screenshot below shows what it looks like in Chrome and Opera. Clicking the down arrow on the right hand side brings up a date picker that lets you select the month and year.

![](https://mdn.mozillademos.org/files/15391/month-control-chrome.png)

The Microsoft Edge `month` control looks like this:

![](https://mdn.mozillademos.org/files/15393/month-control-edge.png)

| Property | Value |
| --- | --- |
| **{{ anch("Value") }}** | A {{ domxref("DOMString") }} representing a month and year, or empty. |
| **Events** | {{ domxref("HTMLElement/change_event", "change") }} and {{ domxref("HTMLElement/input_event", "input") }} |
| **Supported common attributes** | {{ htmlattrxref("autocomplete", "input") }}, {{ htmlattrxref("list", "input") }}, {{ htmlattrxref("readonly", "input") }}, and {{ htmlattrxref("step", "input") }}. |
| **IDL attributes** | `value` |
| **Methods** | {{ domxref("HTMLInputElement.select", "select()") }}, {{ domxref("HTMLInputElement.stepDown", "stepDown()") }}, {{ domxref("HTMLInputElement.stepUp", "stepUp()") }}. |

## Value

A {{ domxref("DOMString") }} representing the value of the month and year entered into the input, in the form YYYY-MM (four or more digit year, then a hyphen ("`-`"), followed by the two-digit month). The format of the month string used by this input type is described in {{ SectionOnPage("/en-US/docs/Web/HTML/Date_and_time_formats", "Format of a valid local month string") }}.

You can set a default value for the input control by including a month and year inside the {{ htmlattrxref("value", "input") }} attribute, like so:

```html
<label for="bday-month">What month were you born in?</label>
<input id="bday-month" type="month" name="bday-month" value="2017-06">
```

{{ EmbedLiveSample('value-example-1', 600, 60) }}

One thing to note is that the displayed date format differs from the actual `value`; most [user agents](/glossary/user_agent/) display the month and year in a locale-appropriate form, based on the set locale of the user's operating system, whereas the date `value` is always formatted `yyyy-MM`.

When the above value is submitted to the server, for example, it will look like `bday-month=1978-06`.

You can also get and set the date value in JavaScript using the {{ domxref("HTMLInputElement.value") }} property, for example:

```html
<label for="bday-month">What month were you born in?</label>
<input id="bday-month" type="month" name="bday-month" value="2017-06">
```

```js
var monthControl = document.querySelector('input[type="month"]');
monthControl.value = '1978-06';
```

{{ EmbedLiveSample("value-example-2", 600, 60) }}

## Additional attributes

In addition to the attributes common to [`input`](/html/element/input/) elements, month inputs offer the following attributes:

| Attribute | Description |
| --- | --- |
| `{{ anch("list") }}` | The id of the <datalist> element that contains the optional pre-defined autocomplete options |
| `{{ anch("max") }}` | The latest year and month to accept as a valid input |
| `{{ anch("min") }}` | The earliest year and month to accept as a valid input |
| `{{ anch("readonly") }}` | A Boolean which, if present, indicates that the input's value can't be edited |
| `{{ anch("step") }}` | A stepping interval to use when incrementing and decrementing the value of the input field |

{{ page("/en-US/docs/Web/HTML/Element/input/text", "list", 0, 1, 2) }}

### {{ htmlattrdef("max") }}

The latest year and month, in the string format discussed in the {{ anch("Value") }} section above, to accept. If the {{ htmlattrxref("value", "input") }} entered into the element exceeds this, the element fails [constraint validation](/guide/html/html5/constraint_validation). If the value of the `max` attribute isn't a valid string in "`yyyy-MM`" format, then the element has no maximum value.

This value must specify a year-month pairing later than or equal to the one specified by the `min` attribute.

### {{ htmlattrdef("min") }}

The latest year and month to accept, in the same "`yyyy-MM`" format described above. If the {{ htmlattrxref("value", "input") }} of the element is less than this, the element fails [constraint validation](/guide/html/html5/constraint_validation). If a value is specified for `min` that isn't a valid year and month string, the input has no minimum value.

This value must be a year-month pairing which is earlier than or equal to the one specified by the `max` attribute.

### {{ htmlattrdef("readonly") }}

A Boolean attribute which, if present, means this field cannot be edited by the user. Its `value` can, however, still be changed from JavaScript code that directly sets the value of the {{ domxref("HTMLInputElement.value") }} property.

**Note:** Because a read-only field cannot have a value, `required` does not have any effect on inputs with the `readonly` attribute also specified.

### {{ htmlattrdef("step") }}

{{ page("/en-US/docs/Web/HTML/Element/input/number", "step-include") }}

For `month` inputs, the value of `step` is given in months, with a scaling factor of 1 (since the underlying numeric value is also in months). The default value of `step` is 1 month.

## Using month inputs

Date-related inputs (including `month`) sound convenient at first glance; they promise an easy UI for choosing dates, and they normalize the data format sent to the server, regardless of the user's locale. However, there are issues with `<input type="month">` because at this time, many major browsers don't yet support it.

We'll look at basic and more complex uses of `<input type="month">`, then offer advice on mitigating the browser support issue in the section {{ anch("Handling browser support") }}).

### Basic uses of month

The simplest use of `<input type="month">` involves a basic [`input`](/html/element/input/) and [`label`](/html/element/label/) element combination, as seen below:

```html
<form>
  <label for="bday-month">What month were you born in?</label>
  <input id="bday-month" type="month" name="bday-month">
</form>
```

{{ EmbedLiveSample('Basic_uses_of_month', 600, 40) }}

### Setting maximum and minimum dates

You can use the {{ htmlattrxref("min", "input") }} and {{ htmlattrxref("max", "input") }} attributes to restrict the range of dates that the user can choose. In the following example we specify a minimum month of `1900-01` and a maximum month of `1999-12`:

```html
<form>
  <label for="bday-month">What month were you born in?</label>
  <input id="bday-month" type="month" name="bday-month"
         min="1900-01" max="1999-12">
</form>
```

{{ EmbedLiveSample('Setting_maximum_and_minimum_dates', 600, 40) }}

The result here is that:

-   Only months between in January 1900 and December 1999 can be selected; months outside that range can't be scrolled to in the control.
-   Depending on what browser you are using, you might find that months outside the specified range might not be selectable in the month picker (e.g. Edge), or invalid (see {{ anch("Validation") }}) but still available (e.g. Chrome).

### Controlling input size

`<input type="month">` doesn't support form sizing attributes such as {{ htmlattrxref("size", "input") }}. You'll have to resort to [CSS](/css) for sizing needs.

## Validation

By default, `<input type="month">` does not apply any validation to entered values. The UI implementations generally don't let you enter anything that isn't a date — which is helpful — but you can still submit the form with the `month` input empty, or enter an invalid date (e.g. the 32nd of April).

To help avoid this, you can use {{ htmlattrxref("min", "input") }} and {{ htmlattrxref("max", "input") }} to restrict the available dates (see {{ anch("Setting maximum and minimum dates") }}), and in addition use the {{ htmlattrxref("required", "input") }} attribute to make filling in the date mandatory. As a result, supporting browsers will display an error if you try to submit a date that is outside the set bounds, or an empty date field.

Let's look at an example; here we've set minimum and maximum dates, and also made the field required:

```html
<form>
  <div>
    <label for="month">What month would you like to visit us (Summer months only, please)?</label>
    <input id="month" type="month" name="month"
           min="2017-06" max="2017-09" required>
    <span class="validity"></span>
  </div>
  <div>
      <input type="submit" value="Submit form">
  </div>
</form>
```

If you try to submit the form without both the month and year specified (or with a date outside the set bounds), the browser displays an error. Try playing with the example now:

{{ EmbedLiveSample('Validation', 600, 120)  }}

Here's a screenshot for those of you who aren't using a supporting browser:

![](https://mdn.mozillademos.org/files/15395/month-required.png)

Here's the CSS used in the above example. Here we make use of the {{ cssxref(":valid") }} and {{ cssxref(":invalid") }} CSS properties to style the input based on whether or not the current value is valid. We had to put the icons on a [`span`](/html/element/span/) next to the input, not on the input itself, because in Chrome the generated content is placed inside the form control, and can't be styled or shown effectively.

```css
div {
  margin-bottom: 10px;
  position: relative;
}

input[type="number"] {
  width: 100px;
}

input + span {
  padding-right: 30px;
}

input:invalid+span:after {
  position: absolute;
  content: '✖';
  padding-left: 5px;
}

input:valid+span:after {
  position: absolute;
  content: '✓';
  padding-left: 5px;
}
```

**Important**: HTML form validation is _not_ a substitute for scripts that ensure that the entered data is in the proper format. It's far too easy for someone to make adjustments to the HTML that allow them to bypass the validation, or to remove it entirely. It's also possible for someone to simply bypass your HTML entirely and submit the data directly to your server. If your server-side code fails to validate the data it receives, disaster could strike when improperly-formatted data is submitted (or data which is too large, of the wrong type, and so forth).

## Handling browser support

As mentioned above, the major problem with using date inputs at the time of writing is that many major browsers don't yet implement them all; only Chrome/Opera and Edge support it on desktop, and most modern browsers on mobile. As an example, the `month` picker on Chrome for Android looks like this:

![](https://mdn.mozillademos.org/files/15397/month-android.png)

Non-supporting browsers gracefully degrade to a text input, but this creates problems both in terms of consistency of user interface (the presented control will be different), and data handling.

The second problem is the more serious of the two. As mentioned earlier, with a `month` input the actual value is always normalized to the format `yyyy-mm`. On the other hand, in its default configuration, a `text` input has no idea what format the date should be in, and this is an issue because of the number of different ways in which people write dates. For example:

-   `mmyyyy` (072018)
-   `mm/yyyy` (07/2018)
-   `mm-yyyy` (07-2018)
-   `yyyy-mm` (2018-07)
-   `Month yyyy` (July 2018)
-   ... and so forth.

One way around this is to put a {{ htmlattrxref("pattern", "input") }} attribute on your `month` input. Even though the `month` input doesn't use it, if the browser falls back to treating it like a `text` input, the pattern will be used. For example, try viewing the following demo in a browser that doesn't support `month` inputs:

```html
<form>
  <div>
    <label for="month">What month would you like to visit us? (Summer months only, yyyy-mm)</label>
    <input id="month" type="month" name="month"
           min="2017-06" max="2017-09" required
           pattern="[0-9]{4}-[0-9]{2}">
    <span class="validity"></span>
  </div>
  <div>
      <input type="submit" value="Submit form">
  </div>
</form>
```

{{ EmbedLiveSample('Handling_browser_support', 600, 100)  }}

If you try submitting it, you'll see that the browser now displays an error message (and highlights the input as invalid) if your entry doesn't match the pattern `nnnn-nn`, where `n` is a number from 0 to 9. Of course, this doesn't stop people from entering invalid dates (such as `0000-42`), or incorrectly formatted dates that follow the pattern.

There's also the problem that the user won't necessarily know which of the many date formats is expected. We have work left to do.

```css
div {
  margin-bottom: 10px;
  position: relative;
}

input[type="number"] {
  width: 100px;
}

input + span {
  padding-right: 30px;
}

input:invalid+span:after {
  position: absolute;
  content: '✖';
  padding-left: 5px;
}

input:valid+span:after {
  position: absolute;
  content: '✓';
  padding-left: 5px;
}
```

The best way to deal with dates in forms in a cross-browser way (until all of the major browsers have supported them for a while) is to get the user to enter the month and year in separate controls ([`select`](/html/element/select/) elements being popular; see below for an implementation), or use JavaScript libraries such as the [jQuery date picker](https://jqueryui.com/datepicker/) plugin.

## Examples

In this example, we create two sets of UI elements, each designed to let the user select a month and year. The first is a native `month` input, and the other is a pair of [`select`](/html/element/select/) elements that allow choosing a month and year independently, for compatibility with browsers that don't yet support `<input type="month">`.

{{ EmbedLiveSample('Examples', 600, 140) }}

### HTML

The form that requests the month and year looks like this:

```html
<form>
  <div class="nativeDatePicker">
    <label for="month-visit">What month would you like to visit us?</label>
    <input type="month" id="month-visit" name="month-visit">
    <span class="validity"></span>
  </div>
  <p class="fallbackLabel">What month would you like to visit us?</p>
  <div class="fallbackDatePicker">
    <div>
      <span>
        <label for="month">Month:</label>
        <select id="month" name="month">
          <option selected>January</option>
          <option>February</option>
          <option>March</option>
          <option>April</option>
          <option>May</option>
          <option>June</option>
          <option>July</option>
          <option>August</option>
          <option>September</option>
          <option>October</option>
          <option>November</option>
          <option>December</option>
        </select>
      </span>
      <span>
        <label for="year">Year:</label>
        <select id="year" name="year">
        </select>
      </span>
    </div>
  </div>
</form>
```

The [`div`](/html/element/div/) with the ID `nativeDatePicker` uses the `month` input type to request the month and year, while the `<div>` with the ID `fallbackDatePicker` instead uses a pair of `<select>` elements. The first requests the month, and the second the year.

The `<select>` for choosing the month is hardcoded with the names of the months, as they don't change (leaving localization out of things). The list of available year values is dynamically generated depending on the current year (see the code comments below for detailed explanations of how these functions work).

```css
div {
  margin-bottom: 10px;
  position: relative;
}

input[type="number"] {
  width: 100px;
}

input + span {
  padding-right: 30px;
}

input:invalid+span:after {
  position: absolute;
  content: '✖';
  padding-left: 5px;
}

input:valid+span:after {
  position: absolute;
  content: '✓';
  padding-left: 5px;
}
```

### JavaScript

The JavaScript code that handles selecting which approach to use and to set up the list of years to include in the non-native year `<select>` follows.

The part of the example that may be of most interest is the feature detection code. In order to detect whether the browser supports `<input type="month">`, we create a new [`input`](/html/element/input/) element, try setting its `type` to `month`, then immediately check what its type is set to. Browsers that don't support type `month` will return `text`, since that's What month falls back to when not supported. If `<input type="month">` is not supported, we hide the native picker and show the fallback picker UI instead.

```js
// define variables
var nativePicker = document.querySelector('.nativeDatePicker');
var fallbackPicker = document.querySelector('.fallbackDatePicker');
var fallbackLabel = document.querySelector('.fallbackLabel');

var yearSelect = document.querySelector('#year');
var monthSelect = document.querySelector('#month');

// hide fallback initially
fallbackPicker.style.display = 'none';
fallbackLabel.style.display = 'none';

// test whether a new date input falls back to a text input or not
var test = document.createElement('input');

try {
  test.type = 'month';
} catch (e) {
  console.log(e.description);
}

// if it does, run the code inside the if() {} block
if(test.type === 'text') {
  // hide the native picker and show the fallback
  nativePicker.style.display = 'none';
  fallbackPicker.style.display = 'block';
  fallbackLabel.style.display = 'block';

  // populate the years dynamically
  // (the months are always the same, therefore hardcoded)
  populateYears();
}

function populateYears() {
  // get the current year as a number
  var date = new Date();
  var year = date.getFullYear();

  // Make this year, and the 100 years before it available in the year <select>
  for(var i = 0; i <= 100; i++) {
    var option = document.createElement('option');
    option.textContent = year-i;
    yearSelect.appendChild(option);
  }
}
```

**Note**: Remember that some years have 53 weeks in them (see [Weeks per year](https://en.wikipedia.org/wiki/ISO_week_date#Weeks_per_year))! You'll need to take this into consideration when developing production apps.

## Specifications

| Specification | Status | Comments |
| --- | --- | --- |
| [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/forms.html#month-state-(type=month) | {{ Spec2('HTML WHATWG') }} |  |

## Browser compatibility

{{ Compat("html.elements.input.input-month") }}

## See also

-   The generic [`input`](/html/element/input/) element and the interface used to manipulate it, {{ domxref("HTMLInputElement") }}
-   [Date and time formats used in HTML](/html/date_and_time_formats)
-   [Date and Time picker tutorial](/guide/html/forms/the_native_form_widgets#date_and_time_picker)
-   `[<input type="datetime-local">](/html/element/input/datetime-local)`, `[<input type="date">](/html/element/input/date)`, `[<input type="time">](/html/element/input/time)`, and `[<input type="week">](/html/element/input/week)`
-   [Compatibility of CSS properties](/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls)