---
title: inputmode
tags:
  - Attribute
  - Editing
  - Forms
  - Global attributes
  - HTML
  - Input
  - Reference
  - Text
  - Web
  - contenteditable
  - global
  - inputmode
  - text input
permalink: html/global_attributes/inputmode
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/inputmode'
browserCompact: html.global_attributes.inputmode
---
The **`inputmode`** [global attribute](/html/global_attributes) is an enumerated attribute that hints at the type of data that might be entered by the user while editing the element or its contents. It can have the following values:

`none`
: No virtual keyboard. For when the page implements its own keyboard input control.

`text` (default value)
: Standard input keyboard for the user's current locale.

`decimal`
: Fractional numeric input keyboard containing the digits and decimal separator for the user's locale (typically . or ,). Devices may or may not show a minus key (-).

`numeric`
: Numeric input keyboard, but only requires the digits 0–9. Devices may or may not show a minus key.

`tel`
: A telephone keypad input, including the digits 0–9, the asterisk (*), and the pound (#) key. Inputs that _require_ a telephone number should typically use `[`input/tel`](/html/element/input/tel/)`instead.

`search`
: A virtual keyboard optimized for search input. For instance, the [return/submit key](https://html.spec.whatwg.org/dev/interaction.html#input-modalities:-the-enterkeyhint-attribute) may be labeled “Search”, along with possible other optimizations. Inputs that _require_ a search query should typically use `[`input/search`](/html/element/input/search/)` instead.

`email`
: A virtual keyboard optimized for entering email addresses. Typically includes the @ character as well as other optimizations. Inputs that _require_ email addresses should typically use `[`input/email`](/html/element/input/email/)` instead.

`url`
: A keypad optimized for entering URLs. This may have the / key more prominent, for example. Enhanced features could include history access and so on. Inputs that _require_ a URL should typically use `[`input/url`](/html/element/input/url/)` instead.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'inputmode' in that specification](https://html.spec.whatwg.org/multipage/interaction.html#input-modalities:-the-inputmode-attribute) | {{ Spec2("HTML WHATWG") }} |  |

## Browser compatibility

{{ Compat("html.global_attributes.inputmode") }}

## See also

-   All [global attributes](/html/global_attributes).