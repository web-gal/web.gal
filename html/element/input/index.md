---
title: '<input>: The Input (Form Input) element'
tags:
  - Data entry
  - Element
  - Forms
  - HTML
  - HTML forms
  - HTML input tag
  - Input
  - MakeBrowserAgnostic
  - Reference
  - Web
permalink: html/element/input
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input'
browserCompact: html.elements.input
---
{{ HTMLRef }}

The **HTML `<input>` element** is used to create interactive controls for web-based forms in order to accept data from the user; a wide variety of types of input data and control widgets are available, depending on the device and [user agent](/glossary/user_agent/). The `<input>` element is one of the most powerful and complex in all of HTML due to the sheer number of combinations of input types and attributes.

{{ EmbedInteractiveExample("pages/tabbed/input-text.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

## <input> types

How an `<input>` works varies considerably depending on the value of its {{ htmlattrxref("type", "input") }} attribute, hence the different types are covered in their own separate reference pages. If this attribute is not specified, the default type adopted is `text`.

The available types are as follows:

  
| Type | Description | Basic Examples | Spec |
| --- | --- | --- | --- |
| [`input/button`](/html/element/input/button/) | A push button with no default behavior displaying the value of the {{ anch('htmlattrdefvalue', 'value') }} attribute, empty by default. | 
```html
<input  type="button" name="button" />
```
{{ EmbedLiveSample("examplebutton",200,55,"","", "nobutton") }} |  |
| [`input/checkbox`](/html/element/input/checkbox/) | A check box allowing single values to be selected/deselected. | 
```html
<input  type="checkbox" name="checkbox"/>
```
{{ EmbedLiveSample("examplecheckbox",200,55,"","", "nobutton") }} |  |
| [`input/color`](/html/element/input/color/) | A control for specifying a color; opening a color picker when active in supporting browsers. | 
```html
<input  type="color" name="color"/>
```
{{ EmbedLiveSample("examplecolor",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/date`](/html/element/input/date/) | A control for entering a date (year, month, and day, with no time). Opens a date picker or numeric wheels for year, month, day when active in supporting browsers. | 
```html
<input  type="date" name="date"/>
```
{{ EmbedLiveSample("exampledate",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/datetime-local`](/html/element/input/datetime-local/) | A control for entering a date and time, with no time zone. Opens a date picker or numeric wheels for date- and time-components when active in supporting browsers. | 
```html
<input  type="datetime-local" name="datetime-local"/>
```
{{ EmbedLiveSample("exampledtl",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/email`](/html/element/input/email/) | A field for editing an email address. Looks like a `text` input, but has validation parameters and relevant keyboard in supporting browsers and devices with dynamic keyboards. | 
```html
<input type="email" name="email"/>
```
{{ EmbedLiveSample("exampleemail",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/file`](/html/element/input/file/) | A control that lets the user select a file. Use the {{ anch('htmlattrdefaccept', 'accept') }} attribute to define the types of files that the control can select. | 
```html
<input type="file" accept="image/*, text/*" name="file"/>
```
{{ EmbedLiveSample("examplefile",'100%',55,"","", "nobutton") }} |  |
| [`input/hidden`](/html/element/input/hidden/) | A control that is not displayed but whose value is submitted to the server. There is an example in the next column, but it's hidden! |  |  |
| [`input/image`](/html/element/input/image/) | A graphical `submit` button. Displays an image defined by the `src` attribute. The {{ anch('htmlattrdefalt', 'alt') }} attribute displays if the image {{ anch('htmlattrdefsrc', 'src') }} is missing. | 
```html
<input type="image" name="image" src="" alt="image input"/>
```
{{ EmbedLiveSample("exampleimage",200,55,"","", "nobutton") }} |  |
| [`input/month`](/html/element/input/month/) | A control for entering a month and year, with no time zone. | 
```html
<input type="month" name="month"/>
```
{{ EmbedLiveSample("examplemonth",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/number`](/html/element/input/number/) | A control for entering a number. Displays a spinner and adds default validation when supported. Displays a numeric keypad in some devices with dynamic keypads. | 
```html
<input  type="number" name="number"/>
```
{{ EmbedLiveSample("examplenumber",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/password`](/html/element/input/password/) | A single-line text field whose value is obscured. Will alert user if site is not secure. | 
```html
<input  type="password" name="password"/>
```
{{ EmbedLiveSample("examplepassword",200,55,"","", "nobutton") }} |  |
| [`input/radio`](/html/element/input/radio/) | A radio button, allowing a single value to be selected out of multiple choices with the same {{ anch('htmlattrdefname', 'name') }} value. | 
```html
<input type="radio" name="radio"/>
```
{{ EmbedLiveSample("exampleradio",200,55,"","", "nobutton") }} |  |
| [`input/range`](/html/element/input/range/) | A control for entering a number whose exact value is not important. Displays as a range widget defaulting to the middle value. Used in conjunction {{ anch('htmlattrdefmin', 'min') }} and {{ anch('htmlattrdefmax', 'max') }} to define the range of acceptable values. | 
```html
<input type="range" name="range" min="0" max="25"/>
```
{{ EmbedLiveSample("examplerange",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/reset`](/html/element/input/reset/) | A button that resets the contents of the form to default values. Not recommended. | 
```html
<input  type="reset" name="reset"/>
```
{{ EmbedLiveSample("examplereset",200,55,"","", "nobutton") }} |  |
| [`input/search`](/html/element/input/search/) | A single-line text field for entering search strings. Line-breaks are automatically removed from the input value. May include a delete icon in supporting browsers that can be used to clear the field. Displays a search icon instead of enter key on some devices with dynamic keypads. | 
```html
<input  type="search" name="search"/>
```
{{ EmbedLiveSample("examplesearch",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/submit`](/html/element/input/submit/) | A button that submits the form. | 
```html
<input type="submit" name="submit"/>
```
{{ EmbedLiveSample("examplesubmit",200,55,"","", "nobutton") }} |  |
| [`input/tel`](/html/element/input/tel/) | A control for entering a telephone number. Displays a telephone keypad in some devices with dynamic keypads. | 
```html
<input  type="tel" name="tel"/>
```
{{ EmbedLiveSample("exampletel",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/text`](/html/element/input/text/) | The default value. A single-line text field. Line-breaks are automatically removed from the input value. | 
```html
<input type="text" name="text"/>
```
{{ EmbedLiveSample("exampletext",200,55,"","", "nobutton") }} |  |
| [`input/time`](/html/element/input/time/) | A control for entering a time value with no time zone. | 
```html
<input  type="time" name="time"/>
```
{{ EmbedLiveSample("exampletime",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/url`](/html/element/input/url/) | A field for entering a URL. Looks like a `text` input, but has validation parameters and relevant keyboard in supporting browsers and devices with dynamic keyboards. | 
```html
<input type="url" name="url"/>
```
{{ EmbedLiveSample("exampleurl",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| [`input/week`](/html/element/input/week/) | A control for entering a date consisting of a week-year number and a week number with no time zone. | 
```html
<input type="week" name="week"/>
```
{{ EmbedLiveSample("exampleweek",200,55,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |
| Obsolete values |
| [`input/datetime`](/html/element/input/datetime/) | {{ deprecated_inline }} {{ obsolete_inline }} A control for entering a date and time (hour, minute, second, and fraction of a second) based on UTC time zone. | 
```html
<input type="datetime" name="datetime"/>
```
{{ EmbedLiveSample("exampledatetime",200,75,"","", "nobutton") }} | {{ HTMLVersionInline("5") }} |

## Attributes

The `<input>` element is so powerful because of its attributes; the {{ htmlattrxref("type", "input") }} attribute, described with examples above, being the most important. Since every `<input>` element, regardless of type, is based on the {{ domxref("HTMLInputElement") }} interface, they technically share the exact same set of attributes. However, in reality, most attributes have an effect on only a specific subset of input types. In addition, the way some attributes impact an input depends on the input type, impacting different input types in different ways.

This section provides a table listing all the attributes with a brief description. This table is followed by a list describing each attribute in greater detail, along with which input types they are associated with.Those that are common to most or all input types are defined in greater detail below. Attributes that are unique to particular input types—or attributes which are common to all input types but have special behaviors when used on a given input type—are instead documented on those types' pages. This element includes the [global attributes](/html/global_attributes). Those with extra importance as it relates to `<input>` are highlighted.

Attributes for the [`input`](/html/element/input/) element include [global HTML attributes](/html/global_attributes) and:
| Attribute | Type or Types | Description |
| --- | --- | --- |
| {{ anch('htmlattrdefaccept', 'accept') }} | file | Hint for expected file type in file upload controls |
| {{ anch('htmlattrdefalt', 'alt') }} | image | alt attribute for the image type. Required for accessibility |
| {{ anch('htmlattrdefautocomplete', 'autocomplete') }} | all | Hint for form autofill feature |
| {{ anch('htmlattrdefautofocus', 'autofocus') }} | all | Automatically focus the form control when the page is loaded |
| {{ anch('htmlattrdefcapture', 'capture') }} | file | Media capture input method in file upload controls |
| {{ anch('htmlattrdefchecked', 'checked') }} | radio, checkbox | Whether the command or control is checked |
| {{ anch('htmlattrdefdirname', 'dirname') }} | text, search | Name of form field to use for sending the element's directionality in form submission |
| {{ anch('htmlattrdefdisabled', 'disabled') }} | all | Whether the form control is disabled |
| {{ anch('htmlattrdefform', 'form') }} | all | Associates the control with a form element |
| {{ anch('htmlattrdefformaction', 'formaction') }} | image, submit | URL to use for form submission |
| {{ anch('htmlattrdefformenctype', 'formenctype') }} | image, submit | Form data set encoding type to use for form submission |
| {{ anch('htmlattrdefformmethod', 'formmethod') }} | image, submit | HTTP method to use for form submission |
| {{ anch('htmlattrdefformnovalidate', 'formnovalidate') }} | image, submit | Bypass form control validation for form submission |
| {{ anch('htmlattrdefformtarget', 'formtarget') }} | image, submit | Browsing context for form submission |
| {{ anch('htmlattrdefheight', 'height') }} | image | Same as `height` attribute for [`img`](/html/element/img/); vertical dimension |
| {{ anch('htmlattrdeflist', 'list') }} | almost all | Value of the id attribute of the [`datalist`](/html/element/datalist/) of autocomplete options |
| {{ anch('htmlattrdefmax', 'max') }} | numeric types | Maximum value |
| {{ anch('htmlattrdefmaxlength', 'maxlength') }} | password, search, tel, text, url | Maximum length (number of characters) of `value` |
| {{ anch('htmlattrdefmin', 'min') }} | numeric types | Minimum value |
| {{ anch('htmlattrdefminlength', 'minlength') }} | password, search, tel, text, url | Minimum length (number of characters) of `value` |
| {{ anch('htmlattrdefmultiple', 'multiple') }} | email, file | Boolean. Whether to allow multiple values |
| {{ anch('htmlattrdefname', 'name') }} | all | Name of the form control. Submitted with the form as part of a name/value pair. |
| {{ anch('htmlattrdefpattern', 'pattern') }} | password, text, tel | Pattern the `value` must match to be valid |
| {{ anch('htmlattrdefplaceholder', 'placeholder') }} | password, search, tel, text, url | Text that appears in the form control when it has no value set |
| [readonly](/html/attributes/readonly) | almost all | Boolean. The value is not editable |
| [required](/html/attributes/required) | almost all | Boolean. A value is required or must be check for the form to be submittable |
| {{ anch('htmlattrdefsize', 'size') }} | email, password, tel, text | Size of the control |
| {{ anch('htmlattrdefsrc', 'src') }} | image | Same as `src` attribute for [`img`](/html/element/img/); address of image resource |
| {{ anch('htmlattrdefstep', 'step') }} | numeric types | Incremental values that are valid. |
| {{ anch('htmlattrdeftype', 'type') }} | all | Type of form control |
| {{ anch('htmlattrdefvalue', 'value') }} | all | At first, the initial value if specified explicitly in HTML. More generally, the current value of the form control. Submitted with the form as part of a name/value pair. |
| {{ anch('htmlattrdefwidth', 'width') }} | image | Same as `width` attribute for [`img`](/html/element/img/) |

A few additional non-standard attributes are listed following the descriptions of the standard attributes.

### Individual attributes

{{ htmlattrdef("accept") }}
: Valid for the `file` input type only, the `accept` attribute defines which file types are selectable in a `file` upload control. See the [`input/file`](/html/element/input/file/) input type.

{{ htmlattrdef("alt") }}
: Valid for the `image` button only, the `alt` attribute provides alternative text for the image, displaying the value of the attribute if the image [`src`](#htmlattrdefsrc) is missing or otherwise fails to load. See the [`input/image`](/html/element/input/image/) input type.

{{ htmlattrdef("autocomplete") }}
: (**Not** a Boolean attribute!) The `[autocomplete](/html/attributes/autocomplete)` attribute takes as its value a space-separated string that describes what, if any, type of autocomplete functionality the input should provide. A typical implementation of autocomplete simply recalls previous values entered in the same input field, but more complex forms of autocomplete can exist. For instance, a browser could integrate with a device's contacts list to autocomplete `email` addresses in an email input field. See {{ SectionOnPage("/en-US/docs/Web/HTML/Attributes/autocomplete", "Values") }} for permitted values.

The `autocomplete` attribute is valid on `hidden`, `text`, `search`, `url`, `tel`, `email`, `date`, `month`, `week`, `time`, `datetime-local`, `number`, `range`, `color`, and `password`. This attribute has no effect on input types that do not return numeric or text data, being valid for all input types except `checkbox`, `radio`, `file`, or any of the button types.

See [The HTML autocomplete attribute](/html/attributes/autocomplete) for additional information, including information on password security and how `autocomplete` is slightly different for `hidden` than for other input types.

{{ htmlattrdef("autofocus") }}
: A Boolean attribute which, if present, indicates that the input should automatically have focus when the page has finished loading (or when the [`dialog`](/html/element/dialog/) containing the element has been displayed).

**Note:** An element with the `autofocus` attribute may gain focus before the {{ domxref("DOMContentLoaded") }} event is fired.

No more than one element in the document may have the `autofocus` attribute. If put on more than one element, the first one with the attribute receives focus.

The `autofocus` attribute cannot be used on inputs of type `hidden`, since hidden inputs cannot be focused.

**Warning:** Automatically focusing a form control can confuse visually-impaired people using screen-reading technology and people with cognitive impairments. When `autofocus` is assigned, screen-readers "teleport" their user to the form control without warning them beforehand.

Use careful consideration for accessibility when applying the `autofocus` attribute. Automatically focusing on a control can cause the page to scroll on load. The focus can also cause dynamic keyboards to display on some touch devices. While a screen reader will announce the label of the form control receiving focus, the screen reader will not announce anything before the label, and the sighted user on a small device will equally miss the context created by the preceding content.

{{ htmlattrdef("capture") }}
: Introduced in the HTML Media Capture specification and valid for the `file` input type only, the `capture` attribute defines which media—microphone, video, or camera—should be used to capture a new file for upload with `file` upload control in supporting scenarios. See the [`input/file`](/html/element/input/file/) input type.

{{ htmlattrdef("checked") }}
: Valid for both `radio` and `checkbox` types, `checked` is a Boolean attribute. If present on a `radio` type, it indicates that that radio button is the currently selected one in the group of same-named radio buttons. If present on a `checkbox` type, it indicates that the checkbox is checked by default (when the page loads). It does _not_ indicate whether this checkbox is currently checked: if the checkbox’s state is changed, this content attribute does not reflect the change. (Only the [`HTMLInputElement`’s `checked` IDL attribute](/api/htmlinputelement) is updated.)

**Note:** Unlike other input controls, a checkboxes and radio buttons value are only included in the submitted data if they are currently `checked`. If they are, the name and the value(s) of the checked controls are submitted.

For example, if a checkbox whose `name` is `fruit` has a `value` of `cherry`, and the checkbox is checked, the form data submitted will include `fruit=cherry`. If the checkbox isn't active, it isn't listed in the form data at all. The default `value` for checkboxes and radio buttons is `on`.

{{ htmlattrdef("dirname") }}
: Valid for `text` and `search` input types only, the `dirname` attribute enables the submission of the directionality of the element. When included, the form control will submit with two name/value pairs: the first being the [`name`](#htmlattrdefname) and [`value`](#htmlattrdefvalue), the second being the value of the `dirname` as the name with the value of `ltr` or `rtl` being set by the browser.

```
<form action="page.html" method="post">
  <label>Fruit: <input type="text" name="fruit" dirname="fruit.dir" value="cherry"></label>
  <input type="submit"/>
</form>
<!-- page.html?fruit=cherry&fruit.dir=ltr -->

```

When the form above is submitted, the input cause both the `name` / `value` pair of `fruit=cherry` and the `dirname` / direction pair of `fruit.dir=ltr` to be sent.

{{ htmlattrdef("disabled") }}
: A Boolean attribute which, if present, indicates that the user should not be able to interact with the input. Disabled inputs are typically rendered with a dimmer color or using some other form of indication that the field is not available for use.

Specifically, disabled inputs do not receive the {{ domxref("Element/click_event", "click") }} event, and disabled inputs are not submitted with the form.

**Note:** Although not required by the specification, Firefox will by default [persist the dynamic disabled state](https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing) of an `<input>` across page loads. Use the {{ htmlattrxref("autocomplete","input") }} attribute to control this feature.

{{ htmlattrdef("form") }}
: A string specifying the [`form`](/html/element/form/) element with which the input is associated (that is, its **form owner**). This string's value, if present, must match the {{ htmlattrxref("id") }} of a `<form>` element in the same document. If this attribute isn't specified, the `<input>` element is associated with the nearest containing form, if any.

The `form` attribute lets you place an input anywhere in the document but have it included with a form elsewhere in the document.

**Note:** An input can only be associated with one form.

{{ htmlattrdef('formaction') }}
: Valid for the `image` and `submit` input types only. See the [`input/submit`](/html/element/input/submit/) input type for more information.

{{ htmlattrdef('formenctype') }}
: Valid for the `image` and `submit` input types only. See the [`input/submit`](/html/element/input/submit/) input type for more information.

{{ htmlattrdef('formmethod') }}
: Valid for the `image` and `submit` input types only. See the [`input/submit`](/html/element/input/submit/) input type for more information.

{{ htmlattrdef('formnovalidate') }}
: Valid for the `image` and `submit` input types only. See the [`input/submit`](/html/element/input/submit/) input type for more information.

{{ htmlattrdef('formtarget') }}
: Valid for the `image` and `submit` input types only. See the [`input/submit`](/html/element/input/submit/) input type for more information.

{{ htmlattrdef("height") }}
: Valid for the `image` input button only, the `height` is the height of the image file to display to represent the graphical submit button. See the [`input/image`](/html/element/input/image/) input type.

{{ htmlattrdef("id") }}
: Global attribute valid for all elements, including all the input types, it defines a unique identifier (ID) which must be unique in the whole document. Its purpose is to identify the element when linking. The value is used as the value of the [`label`](/html/element/label/)'s `for` attribute to link the label with the form control. See [`label`](/html/element/label/).

{{ htmlattrdef("inputmode") }}
: Global value valid for all elements, it provides a hint to browsers as to the type of virtual keyboard configuration to use when editing this element or its contents. Values include `none`, `text`, `tel`, `url`, `email`, `numeric`, `decimal`, and `search`.

{{ htmlattrdef("list") }}
: The value given to the `list` attribute should be the {{ domxref("Element.id", "id") }} of a [`datalist`](/html/element/datalist/) element located in the same document. The `<datalist>` provides a list of predefined values to suggest to the user for this input. Any values in the list that are not compatible with the {{ htmlattrxref("type", "input") }} are not included in the suggested options. The values provided are suggestions, not requirements: users can select from this predefined list or provide a different value.

```html
<datalist id="colorsxx">
  <option>#ff0000</option>
  <option>#ee0000</option>
  <option>#dd0000</option>
  <option>#cc0000</option>
  <option>#bb0000</option>
</datalist>
<datalist id="numbersxx">
  <option>0</option>
  <option>2</option>
  <option>4</option>
  <option>8</option>
  <option>16</option>
  <option>32</option>
  <option>64</option>
</datalist>
<datalist id="fruitsxx">
  <option>cherry</option>
  <option>banana</option>
  <option>mango</option>
  <option>orange</option>
  <option>blueberry</option>
</datalist>
<datalist id="urlsxx">
  <option>https://developer.mozilla.org</option>
  <option>https://caniuse.com/</option>
  <option>https://mozilla.com</option>
  <option>https://mdn.github.io</option>
  <option>https://www.youtube.com/user/firefoxchannel</option>
</datalist>

<p><label for="textx">Text</label> <input type="text" list="fruitsxx" id="textx"/></p>
<p><label for="colorx">Color</label> <input type="color" list="colorsxx" id="colorx"/></p>
<p><label for="rangex">Range</label> <input type="range" min="0" max="64" list="numbersxx" id="rangex"/></p>
<p><label for="numberx">Number</label> <input type="number" min="0" max="64" list="numbersxx" id="numberx"/></p>
<p><label for="urlx">URL</label> <input type="url" list="urlsxx" id="urlx"/></p>
```

{{ EmbedLiveSample("datalist",400,275,"","", "nobutton") }}

It is valid on `text`, `search`, `url`, `tel`, `email`, `date`, `month`, `week`, `time`, `datetime-local`, `number`, `range`, and `color`.

Per the specifications, the `list` attribute is not supported by the `hidden`, `password`, `checkbox`, `radio`, `file`, or any of the button types.

Depending on the browser, the user may see a custom color palette suggested, tic marks along a range, or even a input that opens like a [`select`](/html/element/select/) but allows for non-listed values. Check out the [browser compatibility table](/html/element/datalist#browser_compatibility) for the other input types.

See the [`datalist`](/html/element/datalist/) element.

[{{ htmlattrdef("max") }}](/html/attributes/max)
: Valid for `date`, `month`, `week`, `time`, `datetime-local`, `number`, and `range`, it defines the greatest value in the range of permitted values. If the {{ htmlattrxref("value", "input") }} entered into the element exceeds this, the element fails [constraint validation](/guide/html/html5/constraint_validation). If the value of the `max` attribute isn't a number, then the element has no maximum value.

There is a special case: if the data type is periodic (such as for dates or times), the value of `max` may be lower than the value of `min`, which indicates that the range may wrap around; for example, this allows you to specify a time range from 10 PM to 4 AM.

{{ htmlattrdef("maxlength") }}
: Valid for `text`, `search`, `url`, `tel`, `email`, and `password`, it defines the maximum number of characters (as UTF-16 code units) the user can enter into the field. This must be an integer value `0` or higher. If no `maxlength` is specified, or an invalid value is specified, the field has no maximum length. This value must also be greater than or equal to the value of `minlength`.

The input will fail [constraint validation](/guide/html/html5/constraint_validation) if the length of the text entered into the field is greater than `maxlength` UTF-16 code units long. By default, browsers prevent users from entering more characters than allowed by the `maxlength` attribute. See {{ anch("Client-side validation") }} for more information.

{{ htmlattrdef("min") }}
: Valid for `date`, `month`, `week`, `time`, `datetime-local`, `number`, and `range`, it defines the most negative value in the range of permitted values. If the {{ htmlattrxref("value", "input") }} entered into the element is less than this this, the element fails [constraint validation](/guide/html/html5/constraint_validation). If the value of the `min` attribute isn't a number, then the element has no minimum value.

This value must be less than or equal to the value of the `max` attribute. If the `min` attribute is present but is not specified or is invalid, no `min` value is applied. If the `min` attribute is valid and a non-empty value is less than the minimum allowed by the `min` attribute, constraint validation will prevent form submission. See {{ anch("Client-side validation") }} for more information.

There is a special case: if the data type is periodic (such as for dates or times), the value of `max` may be lower than the value of `min`, which indicates that the range may wrap around; for example, this allows you to specify a time range from 10 PM to 4 AM.

{{ htmlattrdef("minlength") }}
: Valid for `text`, `search`, `url`, `tel`, `email`, and `password`, it defines the minimum number of characters (as UTF-16 code units) the user can enter into the entry field. This must be an non-negative integer value smaller than or equal to the value specified by `maxlength`. If no `minlength` is specified, or an invalid value is specified, the input has no minimum length.

The input will fail [constraint validation](/guide/html/html5/constraint_validation) if the length of the text entered into the field is fewer than `minlength` UTF-16 code units long, preventing form submission. See {{ anch("Client-side validation") }} for more information.

{{ htmlattrdef("multiple") }}
: The Boolean `multiple` attribute, if set, means the user can enter comma separated email addresses in the email widget or can choose more than one file with the `file` input. See the [`input/email`](/html/element/input/email/) and [`input/file`](/html/element/input/file/) input type.

{{ htmlattrdef("name") }}
: A string specifying a name for the input control. This name is submitted along with the control's value when the form data is submitted.

##### What's in a name

Consider the `name` a required attribute (even though it's not). If an input has no `name` specified, or `name` is empty, the input's value is not submitted with the form! (Disabled controls, unchecked radio buttons, unchecked checkboxes, and reset buttons are also not sent.)

There are two special cases:

1.  `_charset_` : If used as the name of an `<input>` element of type [`input/hidden`](/html/element/input/hidden/), the input's `value` is automatically set by the [user agent](/glossary/user_agent/) to the character encoding being used to submit the form.
2.  `isindex`: For historical reasons, the name `[isindex](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-fe-name)` is not allowed.

##### name and radio buttons

The [`name`](#htmlattrdefname) attribute creates a unique behavior for radio buttons.

Only one radio button in a same-named group of radio buttons can be checked at a time. Selecting any radio button in that group automatically deselects any currently-selected radio button in the same group. The value of that one checked radio button is sent along with the name if the form is submitted,

When tabbing into a series of same-named group of radio buttons, if one is checked, that one will receive focus. If they aren't grouped together in source order, if one of the group is checked, tabbing into the group starts when the first one in the group is encountered, skipping all those that aren't checked. In other words, if one is checked, tabbing skips the unchecked radio buttons in the group. If none are checked, the radio button group receives focus when the first button in the same name group is reached.

Once one of the radio buttons in a group has focus, using the arrow keys will navigate through all the radio buttons of the same name, even if the radio buttons are not grouped together in the source order.

##### HTMLFormElement.elements

When an input element is given a `name`, that name becomes a property of the owning form element's {{ domxref("HTMLFormElement.elements") }} property. If you have an input whose `name` is set to `guest` and another whose `name` is `hat-size`, the following code can be used:

```js
let form = document.querySelector("form");

let guestName = form.elements.guest;
let hatSize = form.elements["hat-size"];

```

When this code has run, `guestName` will be the {{ domxref("HTMLInputElement") }} for the `guest` field, and `hatSize` the object for the `hat-size` field.

**Warning:** Avoid giving form elements a `name` that corresponds to a built-in property of the form, since you would then override the predefined property or method with this reference to the corresponding input.

{{ htmlattrdef("pattern") }}
: The `pattern` attribute, when specified, is a regular expression that the input's {{ htmlattrxref("value") }} must match in order for the value to pass [constraint validation](/guide/html/html5/constraint_validation). It must be a valid JavaScript regular expression, as used by the {{ jsxref("RegExp") }} type, and as documented in our [guide on regular expressions](/javascript/guide/regular_expressions); the `'u'` flag is specified when compiling the regular expression, so that the pattern is treated as a sequence of Unicode code points, instead of as ASCII. No forward slashes should be specified around the pattern text.

If the `pattern` attribute is present but is not specified or is invalid, no regular expression is applied and this attribute is ignored completely. If the pattern attribute is valid and a non-empty value does not match the pattern, constraint validation will prevent form submission.

**Tip:** If using the `pattern` attribute, inform the user about the expected format by including explanatory text nearby. You can also include a {{ htmlattrxref("title", "input") }} attribute to explain what the requirements are to match the pattern; most browsers will display this title as a tooltip. The visible explanation is required for accessibility. The tooltip is an enhancement.

See {{ anch("Client-side validation") }} for more information.

{{ htmlattrdef("placeholder") }}
: The `placeholder` attribute is a string that provides a brief hint to the user as to what kind of information is expected in the field. It should be a word or short phrase that provides a hint as to the expected type of data, rather than an explanation or prompt. The text _must not_ include carriage returns or line feeds. So for example if a field is expected to capture a user's first name, and its label is "First Name", a suitable placeholder might be "e.g. Mustafa".

**Note:** The `placeholder` attribute is not as semantically useful as other ways to explain your form, and can cause unexpected technical issues with your content. See {{ SectionOnPage("/en-US/docs/Web/HTML/Element/input", "Labels") }} for more information.

{{ htmlattrdef("readonly") }}
: A Boolean attribute which, if present, indicates that the user should not be able to edit the value of the input. The `readonly` attribute is supported `text`, `search`, `url`, `tel`, `email`, `date`, `month`, `week`, `time`, `datetime-local`, `number`, and `password` input types.

See the [HTML attribute: `readonly`](/html/attributes/readonly) for more information.

{{ htmlattrdef("required") }}
: `required` is a Boolean attribute which, if present, indicates that the user must specify a value for the input before the owning form can be submitted. The `required` attribute is supported `text`, `search`, `url`, `tel`, `email`, `date`, `month`, `week`, `time`, `datetime-local`, `number`, `password`, `checkbox`, `radio`, and `file`.

See {{ anch("Client-side validation") }} and the [HTML attribute: `required`](/html/attributes/required) for more information.

{{ htmlattrdef("size") }}
: Valid for `email`, `password`, `tel`, and `text` `input` types only. Specifies how much of the input is shown. Basically creates same result as setting CSS `width` property with a few specialities. The actual unit of the value depends on the input type. For `password` and `text`, it is a number of characters (or `em` units) with a default value of `20`, and for others, it is `pixel`s. CSS width takes precedence over size attribute.

{{ htmlattrdef("src") }}
: Valid for the `image` input button only, the `src` is string specifying the URL of the image file to display to represent the graphical submit button. See the [`input/image`](/html/element/input/image/) input type.

{{ htmlattrdef("step") }}
: Valid for the numeric input types, including `number`, date/time input types, and `range`, the `[step](/html/attributes/step)` attribute is a number that specifies the granularity that the value must adhere to.

If not explicitly included:

-   `step` defaults to 1 for `number` and `range`.
-   For the date/time input types, `step` is expressed in seconds, with the **default step being 60 seconds**. The step scale factor is 1000 (which converts the seconds to milliseconds, as used in other algorithms).

The value must be a positive number—integer or float—or the special value `any`, which means no stepping is implied, and any value is allowed (barring other constraints, such as `{{ anch("min") }}` and `{{ anch("max") }}`).

If `any` is not explicity set, valid values for the `number`, date/time input types, and `range` input types are equal to the basis for stepping — the `{{ anch("min") }}` value and increments of the step value, up to the `{{ anch("max") }}` value, if specified.

For example, if you have `<input type="number" min="10" step="2">`, then any even integer, `10` or greater, is valid. If omitted, `<input type="number">`, any integer is valid, but floats (like `4.2`) are not valid, because `step` defaults to `1`. For `4.2` to be valid, `step` would have had to be set to `any`, 0.1, 0.2, or any the `min` value would have had to be a number ending in `.2`, such as `<input type="number" min="-5.2">`

**Note:** When the data entered by the user doesn't adhere to the stepping configuration, the value is considered invalid in contraint validation and will match the `:invalid` pseudoclass.

See {{ anch("Client-side validation") }} for more information.

{{ htmlattrdef("tabindex") }}
: Global attribute valid for all elements, including all the input types, an integer attribute indicating if the element can take input focus (is focusable), if it should participate to sequential keyboard navigation. As all input types except for input of type hidden are focusable, this attribute should not be used on form controls, because doing so would require the management of the focus order for all elements within the document with the risk of harming usability and accessibility if done incorrectly.

{{ htmlattrdef('title') }}
: Global attribute valid for all elements, including all input types, containing a text representing advisory information related to the element it belongs to. Such information can typically, but not necessarily, be presented to the user as a tooltip. The title should NOT be used as the primary explanation of the purpose of the form control. Instead, use the [`label`](/html/element/label/) element with a `for` attribute set to the form control's {{ htmlattrdef('id') }} attribute. See {{ anch("Labels") }} below.

{{ htmlattrdef("type") }}
: A string specifying the type of control to render. For example, to create a checkbox, a value of `checkbox` is used. If omitted (or an unknown value is specified), the input type `text` is used, creating a plaintext input field.

Permitted values are listed in {{ anch("<input> types", "`<input>` types") }} above.

{{ htmlattrdef("value") }}
: The input control's value. When specified in the HTML, this is the initial value, and from then on it can be altered or retrieved at any time using JavaScript to access the respective {{ domxref("HTMLInputElement") }} object's `value` property. The `value` attribute is always optional, though should be considered mandatory for `checkbox`, `radio`, and `hidden`.

{{ htmlattrdef("width") }}
: Valid for the `image` input button only, the `width` is the width of the image file to display to represent the graphical submit button. See the [`input/image`](/html/element/input/image/) input type.

### Non-standard attributes

The following non-standard attributes are also available on some browsers. As a general rule, you should avoid using them unless it can't be helped.

| Attribute | Description |
| --- | --- |
| `{{ anch("autocorrect") }}` | A string indicating whether or not autocorrect is `on` or `off`. **Safari only.** |
| `{{ anch("incremental") }}` | Whether or not to send repeated {{ domxref("HTMLInputElement/search_event", "search") }} events to allow updating live search results while the user is still editing the value of the field. **WebKit and Blink only (Safari, Chrome, Opera, etc.).** |
| `{{ anch("mozactionhint") }}` | A string indicating the type of action that will be taken when the user presses the Enter or Return key while editing the field; this is used to determine an appropriate label for that key on a virtual keyboard. **Firefox for Android only**. |
| `{{ anch("orient") }}` | Sets the orientation of the range slider. **Firefox only**. |
| `{{ anch("results") }}` | The maximum number of items that should be displayed in the drop-down list of previous search queries. **Safari only.** |
| `{{ anch("webkitdirectory") }}` | A Boolean indicating whether or not to only allow the user to choose a directory (or directories, if `{{ anch("multiple") }}` is also present) |

{{ htmlattrdef("autocorrect") }} {{ non-standard_inline }}
: {{ page("/en-US/docs/Web/HTML/Element/input/text", "autocorrect-include") }}

{{ htmlattrdef("incremental") }} {{ non-standard_inline }}
: {{ page("/en-US/docs/Web/HTML/Element/input/search", "incremental-include") }}

{{ htmlattrdef("mozactionhint") }} {{ non-standard_inline }}
: {{ page("/en-US/docs/Web/HTML/Element/input/text", "mozactionhint-include") }}

{{ htmlattrdef("orient") }} {{ non-standard_inline }}
: {{ page("/en-US/docs/Web/HTML/Element/input/range", "orient-include") }}

{{ htmlattrdef("results") }} {{ non-standard_inline }}
: {{ page("/en-US/docs/Web/HTML/Element/input/search", "results-include") }}

{{ htmlattrdef("webkitdirectory") }} {{ non-standard_inline }}
: {{ page("/en-US/docs/Web/HTML/Element/input/file", "webkitdirectory-include") }}

## Methods

The following methods are provided by the {{ domxref("HTMLInputElement") }} interface which represents `<input>` elements in the DOM. Also available are those methods specified by the parent interfaces, {{ domxref("HTMLElement") }}, {{ domxref("Element") }}, {{ domxref("Node") }}, and {{ domxref("EventTarget") }}.

{{ domxref("HTMLInputElement.checkValidity", "checkValidity()") }}
: Immediately runs the validity check on the element, triggering the document to fire the {{ domxref("HTMLInputElement.invalid_event", "invalid") }} event at the element if the value isn't valid.

{{ domxref("HTMLFormElement.reportValidity", "reportValidity()") }}
: Returns `true` if the element's value passes validity checks; otherwise, returns `false`.

{{ domxref("HTMLInputElement.select", "select()") }}
: Selects the entire content of the `<input>` element, if the element's content is selectable. For elements with no selectable text content (such as a visual color picker or calendar date input), this method does nothing.

{{ domxref("HTMLInputElement.setCustomValidity", "setCustomValidity()") }}
: Sets a custom message to display if the input element's value isn't valid.

{{ domxref("HTMLInputElement.setRangeText", "setRangeText()") }}
: Sets the contents of the specified range of characters in the input element to a given string. A `selectMode` parameter is available to allow controlling how the existing content is affected.

{{ domxref("HTMLInputElement.setSelectionRange", "setSelectionRange()") }}
: Selects the specified range of characters within a textual input element. Does nothing for inputs which aren't presented as text input fields.

{{ domxref("HTMLInputElement.stepDown", "stepDown()") }}
: Decrements the value of a numeric input by one, by default, or by the specified number of units.

{{ domxref("HTMLInputElement.stepUp", "stepUp()") }}
: Increments the value of a numeric input by one or by the specified number of units.

## CSS

Inputs, being replaced elements, have a few features not applicable to non form elements. There are CSS selectors that can specification target form controls based on their UI features, also known as UI pseudo-classes. The input element can also be targeted by type with attribute selectors. There are some properties that are especially useful as well.

### UI pseudo-classes

Captions super relevant to the [`input`](/html/element/input/) element:
| Pseudo-class | Description |
| --- | --- |
| {{ Cssxref(":enabled") }} | Any currently enabled element that can be activated (selected, clicked on, typed into, etc.) or accept focus and also has a disabled state, in which it can't be activated or accept focus. |
| {{ Cssxref(":disabled") }} | Any currently disabled element that has an enabled state, meaing it otherwise could be activated (selected, clicked on, typed into, etc.) or accept focus were it not disabled. |
| {{ Cssxref(":read-only") }} | Element not editable by the user |
| {{ Cssxref(":read-write") }} | Element that is editable by the user. |
| {{ Cssxref(":placeholder-shown") }} | Element that is currently displaying [placeholder text](https://wiki.developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-placeholder), including [`input`](/html/element/input/) and [`textarea`](/html/element/textarea/) elements with the {{ anch('htmlattrdefplaceholder', 'placeholder') }} attribute present that has, as of yet, no value. |
| {{ Cssxref(":default") }} | Form elements that are the default in a group of related elements. Matches [`input/checkbox`](/html/element/input/checkbox/) and [`input/radio`](/html/element/input/radio/) input types that were checked on page load or render. |
| {{ Cssxref(":checked") }} | Matches [`input/checkbox`](/html/element/input/checkbox/) and [`input/radio`](/html/element/input/radio/) input types that are currently checked (and the ([`option`](/html/element/option/) in a [`select`](/html/element/select/) that is currently selected). |
| {{ Cssxref(":indeterminate") }} | [`input/checkbox`](/html/element/input/checkbox/) elements whose indeterminate property is set to true by JavaScript, [`input/radio`](/html/element/input/radio/) elements, when all radio buttons with the same name value in the form are unchecked, and [`progress`](/html/element/progress/) elements in an indeterminate state |
| {{ Cssxref(":valid") }} | Form controls that can have constraint validation applied and are currently valid. |
| {{ Cssxref(":invalid") }} | Form controls that have constraint validation applied and are currently not valid. Matches a form control whose value doesn't match the constraints set on it by it's attributes, such as {{ anch('htmlattrdefrequired', 'required') }}, {{ anch('htmlattrdefpattern', 'pattern') }} , {{ anch('htmlattrdefstep', 'step') }} and {{ anch('htmlattrdefmax', 'max') }}. |
| {{ Cssxref(":in-range") }} | A non-empty input whose current value is within the range limits specified by the {{ anch('htmlattrdefmin', 'min') }} and {{ anch('htmlattrdefmax', 'max') }} attributes and the {{ anch('htmlattrdefstep', 'step') }} . |
| {{ Cssxref(":out-of-range") }} | A non-empty input whose current value is NOT within the range limits specified by the {{ anch('htmlattrdefmin', 'min') }} and {{ anch('htmlattrdefmax', 'max') }} attributes or does not adher to the {{ anch('htmlattrdefstep', 'step') }} constraint. |
| {{ Cssxref(":required") }} | [`input`](/html/element/input/), [`select`](/html/element/select/), or [`textarea`](/html/element/textarea/) element that has the {{ htmlattrxref("required", "input") }} attribute set on it. Only matches elements that can be required. The attribute included on a non-requirable element will not make for a match. |
| {{ Cssxref(":optional") }} | [`input`](/html/element/input/), [`select`](/html/element/select/), or [`textarea`](/html/element/textarea/) element that does NOT have the {{ htmlattrxref("required", "input") }} attribute set on it. Does not match elements that can't be required. |
| {{ Cssxref(":blank") }} | [`input`](/html/element/input/) and [`textarea`](/html/element/textarea/) elements that currently have no value. |
| {{ Cssxref(":user-invalid") }} | Similar to `:invalid`, but is activated on blur. Matches invalid input but only after the user interaction, such as by focusing on the control, leaving the control, or attempting to submit the form containing the invalid control. |

#### Examples

We can style a checkbox label based on whether the checkbox is checked or not. In this example, we are styling the {{ cssxref('color') }} and {{ cssxref('font-weight') }} of the [`label`](/html/element/label/) that comes immediately after a checked input. We haven't applied any styles if the `input` is not checked.

```html
<input id="checkboxInput" type="checkbox">
<label for="checkboxInput">Toggle the checkbox on and off</label>

```
```css
input:checked + label {
  color: red;
  font-weight: bold;
}

```

{{ EmbedLiveSample('checkbox_label', 500, 80) }}

### Attribute selectors

It is possible to target different types of form controls based on their {{ anch('htmlattrdeftype', 'type') }} using [attribute selectors](/en-US/docs/Learn/CSS/Building_blocks/Selectors/Attribute_selectors). CSS attribute selectors match elements based on either just the presence of a attribute or the value of a given attribute.

```css
/* matches a password input */
input[type="password"] {}

/* matches a form control whose valid values are limited to a range of values*/
input[min][max] {}

/* matches a form control with with a pattern attribute */
 input[pattern] {}
```

### ::placeholder

By default, the appearance of placeholder text is a translucent or light gray. The {{ cssxref('::placeholder') }} pseudo-element is the input's [placeholder text](/html/forms_in_html#the_placeholder_attribute). It can be styled with a limited subset of CSS properties.

```css
::placeholder {
  color: blue;
}
```

Only the subset of CSS properties that apply to the {{ cssxref("::first-line") }} pseudo-element can be used in a rule using `::placeholder` in its selector.

### appearance

The {{ cssxref("appearance") }} property enables the displaying of (almost) any element as a platform-native style based on the operating system's theme as well as the removal of any platform-native styling with the `none` value.

You could make a `<div>` look like a radio button with `div {appearance: radio;}` or a radio look like a checkbox with `[type="checkbox] {appearance: checkbox;}`, but don't.

Setting `appearance: none` removes platform native borders, but not functionality.

### caret-color

A property specific to text entry-related elements is the CSS {{ cssxref("caret-color") }} property, which lets you set the color used to draw the text input caret:

#### HTML

```html
<label for="textInput">Note the red caret:</label>
<input id="textInput" class="custom" size="32">

```

#### CSS

```css
input.custom {
  caret-color: red;
  font: 16px "Helvetica", "Arial", "sans-serif"
}

```

#### Result

{{ EmbedLiveSample('caret-color', 500, 80) }}

### object-position and object-fit

In certain cases (typically involving non-textual inputs and specialized interfaces), the `<input>` element is a [replaced element](/css/replaced_element). When it is, the position and size of the element's size and positioning within its frame can be adjusted using the CSS {{ cssxref("object-position") }} and {{ cssxref("object-fit") }} properties

### Styling

For more information about adding color to elements in HTML, see:

-   [Applying color to HTML elements using CSS](/html/applying_color).

Also see:

-   [Styling HTML forms,](/en-US/docs/Learn/HTML/Forms/Styling_HTML_forms) [advanced styling for HTML forms](/en-US/docs/Learn/HTML/Forms/Advanced_styling_for_HTML_forms), and
-   the [compatibility table of CSS properties](/en-US/docs/Learn/HTML/Forms/Property_compatibility_table_for_form_widgets).

## Additional features

### Labels

Labels are needed to associate assistive text with an `<input>`. The [`label`](/html/element/label/) element provides explanatory information about a form field that is _always_ appropriate (aside from any layout concerns you have). It's never a bad idea to use a `<label>` to explain what should be entered into an `<input>` or [`textarea`](/html/element/textarea/).

#### Associated labels

The semantic pairing of `<input>` and `<label>` elements is useful for assistive technologies such as screen readers. By pairing them using the `<label>`'s {{ htmlattrxref("for", "label") }} attribute, you bond the label to the input in a way that lets screen readers describe inputs to users more precisely.

It does not suffice to have plain text adjacent to the `<input>` element,. Rather, usability and accessibility requires the inclusion of either implicit or explicit [`label`](/html/element/label/):

```html
<!-- inaccessible -->
<p>Enter your name: <input id="name" type="text" size="30"></p>

<!-- implicit label -->
<p><label>Enter your name: <input id="name" type="text" size="30"></label></p>

<!-- explicit label -->
<p><label for="name">Enter your name: </label><input id="name" type="text" size="30"></p>
```

The first example is inaccessible: no relationship exists between the prompt and the `<input>` element.

In addition to an accessible name, the label provides a larger 'hit' area for mouse and touch screen users to click on or touch. By pairing a `<label>` with an `<input>`, clicking on either one will focus the `<input>`. If you use plain text to "label" your input, this won't happen. Having the prompt part of the activation area for the input is helpful for people with motor control conditions.

As web developers, it's important that we never assume that people will know all the things that we know. The diversity of people using the web—and by extension your web site—practically guarantees that some of your site's visitors will have some variation in thought processes and/or circumstances that leads them to interpret your forms very differently from you without clear and properly-presented labels.

#### Placeholders are not accessible

The {{ htmlattrxref("placeholder", "input") }} attribute lets you specify text that appears within the `<input>` element's content area itself when it is empty. The placeholder should never be required in order to understand your forms. It is not a label, and should not be used as a substitute, because it isn't. The placeholder is used to provide a hint as to what an inputted value should look like, not an explanation or prompt.

Not only is the placeholder not accessible to screen readers, but once the user enters any text into the form control, or if the form control already has a value, the placeholder disappears. Browsers with automatic page translation features may skip over attributes when translating, meaning the `placeholder` may not get translated.

Don't use the {{ htmlattrxref("placeholder", "input") }} attribute if you can avoid it. If you need to label an `<input>` element, use the [`label`](/html/element/label/) element.

### Client-side validation

**Warning:** Client-side validation is useful, but it does _not_ guarantee that the server will receive valid data. If the data must be in a specific format, _always_ verify it also on the server-side, and return a [`400` HTTP response](/http/status/400) if the format is invalid.

In addition to using CSS to style inputs based on the {{ cssxref(":valid") }} or {{ cssxref(":invalid") }} UI states based on the current state of each input, as noted in the {{ anch('UI pseudo-classes') }} section above, the browser provides for client-side validation on (attempted) form submission. On form submission, if there is a form control that fails constraint validation, supporting browsers will display an error message on the first invalid form control; displaying a default message based on the error type, or a message set by you.

Some input types and other attributes place limits on what values are valid for a given input. For example, `<input type="number" min="2" max="10" step="2">` means only the number 2, 4, 6, 8, or 10 are valid. Several errors could occur, including a `rangeUnderflow` error if the value is less than 2, `rangeOverflow` if greater than 10, `stepMismatch` if the value is a number between 2 and 10, but not an even integer (does not match the requirements of the `step` attribute), or `typeMismatch` if the value is not a number.

For the input types whose domain of possible values is periodic (that is, at the highest possible value, the values wrap back around to the beginning rather than ending), it's possible for the values of the {{ htmlattrxref("max") }} and {{ htmlattrxref("min") }} properties to be reversed, which indicates that the range of permitted values starts at `min`, wraps around to the lowest possible value, then continues on until `max` is reached. This is particularly useful for dates and times, such as when you want to allow the range to be from 8 PM to 8 AM:

```html
<input type="time" min="20:00" max="08:00" name="overnight">
```

Specific attributes and their values can lead to a specific error {{ domxref('ValidityState') }}:

Validity object errors depend on the [`input`](/html/element/input/) attributes and their values:
| Attribute | Relevant property | Description |
| --- | --- | --- |
| {{ anch('htmlattrdefmax', 'max') }} | {{ domxref('validityState.rangeOverflow') }} | Occurs when the value is greater than the maximum value as defined by the `max` attribute |
| {{ anch('htmlattrdefmaxlength', 'maxlength') }} | {{ domxref('validityState.tooLong') }} | Occurs when the number of characters is greater than the number allowed by the `maxlength` property |
| {{ anch('htmlattrdefmin', 'min') }} | {{ domxref('validityState.rangeUnderflow') }} | Occurs when the value is less than the minimum value as defined by the `min` attribute |
| {{ anch('htmlattrdefminlength', 'minlength') }} | {{ domxref('validityState.tooShort') }} | Occurs when the number of characters is less than the number required by the `minlength` property |
| {{ anch('htmlattrdefpattern', 'pattern') }} | {{ domxref('validityState.patternMismatch') }} | Occurs when a pattern attribute is included with a valid regular expression and the `value` does not match it. |
| {{ anch('htmlattrdefrequired', 'required') }} | {{ domxref('validityState.valueMissing') }} | Occurs when the `required` attribute is present but the value is `null` or radio or checkbox is not checked. |
| {{ anch('htmlattrdefstep', 'step') }} | {{ domxref('validityState.stepMismatch') }} | The value doesn't match the step increment. Increment default is `1`, so only integers are valid on `type="number"` is step is not included. `step="any"` will never throw this error. |
| {{ anch('htmlattrdeftyoe', 'type') }} | {{ domxref('validityState.typeMismatch') }} | Occurs when the value is not of the correct type, for example a email does not contain an `@` or a url doesn't contain a protocol. |

If a form control doesn't have the `required` attribute, no value, or an empty string, is not invalid. Even if the above attributes are present, with the exception of `required`, and empty string will not lead to an error.

We can set limits on what values we accept, and supporting browsers will natively validate these form values and alert the user if there is a mistake when the form is submitted.

In addition to the errors described in the table above, the `validityState` interface contains the `badInput`, `valid`, and `customError` boolean readonly properties. The validity object includes:

-   {{ domxref('validityState.valueMissing') }}
-   {{ domxref('validityState.typeMismatch') }}
-   {{ domxref('validityState.patternMismatch') }}
-   {{ domxref('validityState.tooLong') }}
-   {{ domxref('validityState.tooShort') }}
-   {{ domxref('validityState.rangeUnderflow') }}
-   {{ domxref('validityState.rangeOverflow') }}
-   {{ domxref('validityState.stepMismatch') }}
-   {{ domxref('validityState.badInput') }}
-   {{ domxref('validityState.valid') }}
-   {{ domxref('validityState.customError') }}

For each of these Boolean properties, a value of `true` indicates that the specified reason validation may have failed is true, with the exception of the `valid` property, which is `true` if the element's value obeys all constraints.

If there is an error, supporting browsers will both alert the user and prevent the form from being submitted. A word of caution: if a custom error is set to a truthy value (anything other than the empty string or `null`), the form will be be prevented from being submitted. If there is no custom error message, and none of the other properties return true, `valid` will be true, and the form can be submitted.

```js
function validate(input) {
  let validityState_object = input.validity;
  if(validityState_object.valueMissing) {
     input.setCustomValidity('A value is required');
  } else if (input.rangeUnderflow) {
    input.setCustomValidity('Your value is too low');
  } else if (input.rangeOverflow) {
    input.setCustomValidity('Your value is too high');
  } else {
    input.setCustomValidity('');
  }
}
```

The last line, setting the custom validity message to the error string is vital. If the user makes an error, and the validity is set, it will fail to submit, even if all of the values are valid, until the message is `null`.

#### Example

If you want to present a custom error message when a field fails to validate, you need to use the [Constraint validation features](/api/constraint_validation#constraint_validation_interfaces) available on `<input>` (and related) elements. Take the following form:

```html
<form>
  <label for="name">Enter username (upper and lowercase letters): </label>
  <input type="text" name="name" id="name" required pattern="[A-Za-z]+">
  <button>Submit</button>
</form>
```

The basic HTML form validation features will cause this to produce a default error message if you try to submit the form with either no valid filled in, or a value that does not match the `pattern`.

If you wanted to instead display custom error messages, you could use JavaScript like the following:

```js
const nameInput = document.querySelector('input');
const form = document.querySelector('form');

nameInput.addEventListener('input', () => {
  nameInput.setCustomValidity('');
  nameInput.checkValidity();
});

nameInput.addEventListener('invalid', () => {
  if(nameInput.value === '') {
    nameInput.setCustomValidity('Enter your username!');
  } else {
    nameInput.setCustomValidity('Usernames can only contain upper and lowercase letters. Try again!');
  }
});
```

The example renders like so:

{{ EmbedLiveSample('Client-side_validation') }}

In brief:

-   We check the valid state of the input element every time its value is changed by running the `checkValidity()` method via the `input` event handler.
-   If the value is invalid, an `invalid` event is raised, and the `invalid` event handler function is run. Inside this function we work out whether the value is invalid because it is empty, or because it doesn't match the pattern, using an `if()` block, and set a custom validity error message.
-   As a result, if the input value is invalid when the submit button is pressed, one of the custom error messages will be shown.
-   If it is valid, it will submit as you'd expect. For this to happen, the custom validity has to be cancelled, by invoking `setCustomValidity()` with an empty string value. We therefore do this every time the `input` event is raised. If you don't do this, and a custom validity was previously set, the input will register as invalid, even if it current contains a valid value on submission.

**Note:** Always validate input constraints both client side and server side. Constraint validation doesn't remove the need for validation on the _server side_. Invalid values can still be sent by older browsers or by bad actors.

**Note**: Firefox supported a proprietary error attribute — `x-moz-errormessage` — for many versions, which allowed you set custom error messages in a similar way. This has been removed as of version 66 (see [bug 1513890](https://bugzilla.mozilla.org/show_bug.cgi?id=1513890)).

### Localization

The allowed inputs for certain `<input>` types depend on the locale. In some locales, 1,000.00 is a valid number, while in other locales the valid way to enter this number is 1.000,00.

Firefox uses the following heuristics to determine the locale to validate the user's input (at least for `type="number"`):

-   Try the language specified by a `lang`/`xml:lang` attribute on the element or any of its parents.
-   Try the language specified by any `Content-Language` HTTP header. Or,
-   If none specified, use the browser's locale.

### Technical summary

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), listed, submittable, resettable, form-associated element, [phrasing content](/html/content_categories#phrasing_content). If the {{ htmlattrxref("type", "input") }} is not `hidden`, then labelable element, palpable content. |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | Must have a start tag and must not have an end tag. |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | 
-   `type=button`: `[button](/accessibility/aria/roles/button_role)`
-   `type=checkbox`: `[checkbox](/accessibility/aria/roles/checkbox_role)`
-   `type=email`
    -   with no `list` attribute: `[textbox](/accessibility/aria/roles/textbox_role)`
    -   with `list` attribute: [`combobox`](https://w3c.github.io/aria/#combobox)
-   `type=image`: `[button](/accessibility/aria/roles/button_role)`
-   `type=number`: [`spinbutton`](https://w3c.github.io/aria/#spinbutton)
-   `type=radio`: [`radio`](https://w3c.github.io/aria/#radio)
-   `type=range`: [`slider`](https://w3c.github.io/aria/#slider)
-   `type=reset`: `[button](/accessibility/aria/roles/button_role)`
-   `type=search`
    -   with no `list` attribute: [`searchbox`](https://w3c.github.io/aria/#searchbox)
    -   with `list` attribute: [`combobox`](https://w3c.github.io/aria/#combobox)
-   `type=submit`: `[button](/accessibility/aria/roles/button_role)`
-   `type=tel`
    -   with no `list` attribute: `[textbox](/accessibility/aria/roles/textbox_role)`
    -   with `list` attribute: [`combobox`](https://w3c.github.io/aria/#combobox)
-   `type=text`
    -   with no `list` attribute: `[textbox](/accessibility/aria/roles/textbox_role)`
    -   with `list` attribute: [`combobox`](https://w3c.github.io/aria/#combobox)
-   `type=url`
    -   with no `list` attribute: `[textbox](/accessibility/aria/roles/textbox_role)`
    -   with `list` attribute: [`combobox`](https://w3c.github.io/aria/#combobox)
-   `type=color|date|datetime-local|file|hidden|month|password|time|week`: [no corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role)

 |
| Permitted ARIA roles | 

-   `type=button`: [`link`](https://w3c.github.io/aria/#link), [`menuitem`](https://w3c.github.io/aria/#menuitem), [`menuitemcheckbox`](https://w3c.github.io/aria/#menuitemcheckbox), [`menuitemradio`](https://w3c.github.io/aria/#menuitemradio), [`option`](https://w3c.github.io/aria/#option), [`radio`](https://w3c.github.io/aria/#radio), [`switch`](https://w3c.github.io/aria/#switch), [`tab`](https://w3c.github.io/aria/#tab)
-   `type=checkbox`: [`button`](https://w3c.github.io/aria/#button) when used with `aria-pressed`, [`menuitemcheckbox`](https://w3c.github.io/aria/#menuitemcheckbox), [`option`](https://w3c.github.io/aria/#option), [`switch`](https://w3c.github.io/aria/#switch)
-   `type=image`: [`link`](https://w3c.github.io/aria/#link), [`menuitem`](https://w3c.github.io/aria/#menuitem), [`menuitemcheckbox`](https://w3c.github.io/aria/#menuitemcheckbox), [`menuitemradio`](https://w3c.github.io/aria/#menuitemradio), [`radio`](https://w3c.github.io/aria/#radio), [`switch`](https://w3c.github.io/aria/#switch)
-   `type=radio`: [`menuitemradio`](https://w3c.github.io/aria/#menuitemradio)
-   `type=text` with no `list` attribute: [`combobox`](https://w3c.github.io/aria/#combobox), [`searchbox`](https://w3c.github.io/aria/#searchbox), [`spinbutton`](https://w3c.github.io/aria/#spinbutton)
-   `type=color|date|datetime|datetime-local|email|file|hidden|month|number|password|range|reset|search|submit|tel|url|week` or `text` with `list` attribute: no `role` permitted

 |
| DOM interface | {{ domxref("HTMLInputElement") }} |

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<input>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-input-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML Media Capture** The definition of 'capture attribute' in that specification](https://w3c.github.io/html-media-capture/#the-capture-attribute) | {{ Spec2('HTML Media Capture') }} | Adds the `capture` attribute |
| [**HTML 5** The definition of '<input>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-input-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<form>' in that specification](https://www.w3.org/TR/html401/interact/forms.html#h-17.4) | {{ Spec2('HTML4.01') }} |  |

## Accessibility concerns

### Labels

When including inputs, it is an accessibilty requirement to add labels along side. This is needed so those who use assistive technologies can tell what the input is for. Also, clicking or touching a label gives focus to the label's associated form control. This improves the accessibility and usability for sighted users, increases the area a user can click or touch to activate the form control. This is especially useful (and even needed) for radio buttons and checkboxes, which are tiny. For more information about labels in general see {{ anch("Labels") }} .

The following is an example of how to associate the `<label>` with an `<input>` element in the above style. You need to give the `<input>` an `id` attribute. The `<label>` then needs a `for` attribute whose value is the same as the input's `id`.

```
<label for="peas">Do you like peas?</label>
<input type="checkbox" name="peas" id="peas">

```

### Size

Interactive elements such as form input should provide an area large enough that it is easy to activate them. This helps a variety of people, including people with motor control issues and people using non-precise forms of input such as a stylus or fingers. A minimum interactive size of 44×44 [CSS pixels](https://www.w3.org/TR/WCAG21/#dfn-css-pixels) is recommended.

-   [Understanding Success Criterion 2.5.5: Target Size | W3C Understanding WCAG 2.1](https://www.w3.org/WAI/WCAG21/Understanding/target-size.html)
-   [Target Size and 2.5.5 | Adrian Roselli](http://adrianroselli.com/2019/06/target-size-and-2-5-5.html)
-   [Quick test: Large touch targets - The A11Y Project](https://a11yproject.com/posts/large-touch-targets/)

## Browser compatibility

{{ Compat("html.elements.input") }}

## See also

-   [Form constraint validation](/guide/html/html5/constraint_validation)
-   [Your first HTML form](/en-US/docs/Learn/HTML/Forms/Your_first_HTML_form)
-   [How to structure an HTML form](/en-US/docs/Learn/HTML/Forms/How_to_structure_an_HTML_form)
-   [The native form widgets](/en-US/docs/Learn/HTML/Forms/The_native_form_widgets)
-   [Sending form data](/en-US/docs/Learn/HTML/Forms/Sending_and_retrieving_form_data)
-   [Form data validation](/en-US/docs/Learn/HTML/Forms/Form_validation)
-   [How to build custom form widgets](/en-US/docs/Learn/HTML/Forms/How_to_build_custom_form_widgets)
-   [HTML forms in legacy browsers](/en-US/docs/Learn/HTML/Forms/HTML_forms_in_legacy_browsers)
-   [Styling HTML forms](/en-US/docs/Learn/HTML/Forms/Styling_HTML_forms)
-   [Advanced styling for HTML forms](/en-US/docs/Learn/HTML/Forms/Advanced_styling_for_HTML_forms)
-   [CSS property compatibility table](/en-US/docs/Learn/HTML/Forms/Property_compatibility_table_for_form_widgets)