---
title: '<datalist>: The HTML Data List element'
tags:
  - Element
  - HTML
  - HTML forms
  - HTML5
  - Reference
  - Web
permalink: html/element/datalist
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist'
browserCompact: html.elements.datalist
---
{{ HTMLRef }}

The **HTML `<datalist>` element** contains a set of [`option`](/html/element/option/) elements that represent the permissible or recommended options available to choose from within other controls.

{{ EmbedInteractiveExample("pages/tabbed/datalist.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content). |
| Permitted content | Either [phrasing content](/html/content_categories#phrasing_content) or zero or more [`option`](/html/element/option/) elements. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [listbox](/accessibility/aria/roles/listbox_role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLDataListElement") }} |

## Attributes

This element has no other attributes than the [global attributes](/en-US/docs/HTML/Global_attributes), common to all elements.

## Examples

### Basic datalist

```html
<label for="myBrowser">Choose a browser from this list:</label>
<input list="browsers" id="myBrowser" name="myBrowser" />
<datalist id="browsers">
  <option value="Chrome">
  <option value="Firefox">
  <option value="Internet Explorer">
  <option value="Opera">
  <option value="Safari">
  <option value="Microsoft Edge">
</datalist>

```

#### Result

{{ EmbedLiveSample("Basic_datalist", '100%', 100) }}

### Customizing datalist styles

The style of the list produced by a `<datalist>` element is platform-dependent, so if you want to customize the display of the options, you have to implement your own custom solution that overrides the default behavior. The below example provides a simple solution for this. Note how we haven't specified the `<datalist>` `id` inside the `[<input>](/html/element/input)` `list` attribute in this case, as that stops the browser-specific display of the data list items from kicking in. Instead, we are setting the selected `<datalist>` value in the `<input>` via JavaScript.

**Note**: Since `[::after](/css/::after)` is not permitted on `<input>` elements, if you want to reproduce the arrow-down icon you will have to wrap the `<input>` element in another element that you can hang the styling on (or some other suitable solution).

#### HTML

```html
<input
  list=""
  name="option"
  id="input"
  autocomplete="off"
>

<datalist id="datalist">
  <option>Carrots</option>
  <option>Peas</option>
  <option>Beans</option>
</datalist>
```

#### CSS

```css
datalist {
  position: absolute;
  background-color: lightgrey;
  font-family: sans-serif;
  font-size: 0.8rem;
}

option {
  background-color: #bbb;
  padding: 4px;
  margin-bottom: 1px;
  cursor: pointer;
}

```

#### JavaScript

```js
input.onfocus = function () {
  datalist.style.display = 'block';
}

for (let option of datalist.options) {
  option.onclick = function () {
    input.value = this.value;
    datalist.style.display = 'none';
  }
}

datalist.style.width = input.offsetWidth + 'px';
datalist.style.left = input.offsetLeft + 'px';
datalist.style.top = input.offsetTop + input.offsetHeight + 'px';
```

#### Result

{{ EmbedLiveSample('Customizing_datalist_styles', '100%', 200) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<datalist>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-datalist-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<datalist>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-datalist-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.datalist") }}

## Polyfill

Include this polyfill to provide support for older and currently incompatible browsers:  
[datalist-polyfill](https://github.com/mfranzke/datalist-polyfill)

## See also

-   The [`input`](/html/element/input/) element, and more specifically its {{ htmlattrxref("list", "input") }} attribute;
-   The [`option`](/html/element/option/) element.