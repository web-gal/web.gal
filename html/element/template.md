---
title: '<template>: The Content Template element'
tags:
  - Element
  - HTML
  - HTML Web Components
  - 'HTML:Flow content'
  - 'HTML:Metadata content'
  - 'HTML:Phrasing content'
  - 'HTML:Script-supporting element'
  - Reference
  - Template
  - Web
  - Web Components
permalink: html/element/template
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/template'
browserCompact: html.elements.template
---
{{ HTMLRef }}

The **HTML Content Template (`<template>`) element** is a mechanism for holding [HTML](/glossary/html/) that is not to be rendered immediately when a page is loaded but may be instantiated subsequently during runtime using JavaScript.

Think of a template as a content fragment that is being stored for subsequent use in the document. While the parser does process the contents of the **`<template>`** element while loading the page, it does so only to ensure that those contents are valid; the element's contents are not rendered, however.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Metadata content](/html/content_categories#metadata_content), [flow content](/html/content_categories#flow_content), [phrasing content](/guide/html/content_categories#phrasing_content), [script-supporting element](/guide/html/content_categories#script-supporting_elements) |
| Permitted content | No restrictions |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [metadata content](/guide/html/content_categories#metadata_content), [phrasing content](/guide/html/content_categories#phrasing_content), or [script-supporting elements](/guide/html/content_categories#script-supporting_elements). Also allowed as a child of a [`colgroup`](/html/element/colgroup/) element that does _not_ have a {{ htmlattrxref("span", "colgroup") }} attribute. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLTemplateElement") }} |

## Attributes

This element only includes the [global attributes](/html/global_attributes).

However, the {{ domxref("HTMLTemplateElement") }} has a {{ domxref("HTMLTemplateElement.content", "content") }} property, which is a read-only {{ domxref("DocumentFragment") }} containing the DOM subtree which the template represents. Note that directly using the value of the {{ domxref("HTMLTemplateElement.content", "content") }} could lead to unexpected behavior, see [Avoiding DocumentFragment pitfall](#Avoiding_DocumentFragment_pitfall) section below.

## Examples

First we start with the HTML portion of the example.

```html
<table id="producttable">
  <thead>
    <tr>
      <td>UPC_Code</td>
      <td>Product_Name</td>
    </tr>
  </thead>
  <tbody>
    <!-- existing data could optionally be included here -->
  </tbody>
</table>

<template id="productrow">
  <tr>
    <td class="record"></td>
    <td></td>
  </tr>
</template>

```

First, we have a table into which we will later insert content using JavaScript code. Then comes the template, which describes the structure of an HTML fragment representing a single table row.

Now that the table has been created and the template defined, we use JavaScript to insert rows into the table, with each row being constructed using the template as its basis.

```js
// Test to see if the browser supports the HTML template element by checking
// for the presence of the template element's content attribute.
if ('content' in document.createElement('template')) {

    // Instantiate the table with the existing HTML tbody
    // and the row with the template
    var tbody = document.querySelector("tbody");
    var template = document.querySelector('#productrow');

    // Clone the new row and insert it into the table
    var clone = template.content.cloneNode(true);
    var td = clone.querySelectorAll("td");
    td[0].textContent = "1235646565";
    td[1].textContent = "Stuff";

    tbody.appendChild(clone);

    // Clone the new row and insert it into the table
    var clone2 = template.content.cloneNode(true);
    td = clone2.querySelectorAll("td");
    td[0].textContent = "0384928528";
    td[1].textContent = "Acme Kidney Beans 2";

    tbody.appendChild(clone2);

} else {
  // Find another way to add the rows to the table because
  // the HTML template element is not supported.
}

```

The result is the original HTML table, with two new rows appended to it via JavaScript:

```css
table {
  background: #000;
}
table td {
  background: #fff;
}
```

{{ EmbedLiveSample("Examples", 500, 120) }}

## Avoiding DocumentFragment pitfall

A {{ domxref("DocumentFragment") }} is not a valid target for various events, as such it is often preferable to clone or refer to the elements within it.

Consider the following HTML and JavaScript:

### HTML

```html
<div id="container"></div>

<template id="template">
  <div>Click me</div>
</template>
```

### JavaScript

```js
const container = document.getElementById("container");
const template = document.getElementById("template");

function clickHandler(event) {
  alert("Clicked a div");
}

const firstClone = template.content.cloneNode(true);
firstClone.addEventListener("click", clickHandler);
container.appendChild(firstClone);

const secondClone = template.content.firstElementChild.cloneNode(true);
secondClone.addEventListener("click", clickHandler);
container.appendChild(secondClone);
```

### Result

`firstClone` is a DocumentFragment instance, so while it gets appended inside the container as expected, clicking on it does not trigger the click event. `secondClone` is an [HTMLDivElement](/api/htmldivelement) instance, clicking on it works as one would expect.

{{ EmbedLiveSample('Avoiding_DocumentFragment_pitfall') }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'template element' in that specification](https://html.spec.whatwg.org/multipage/scripting.html#the-template-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'template element' in that specification](https://www.w3.org/TR/html52/semantics-scripting.html#the-template-element) | {{ Spec2('HTML5 W3C') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.template") }}

## See also

-   Web components: [`slot`](/html/element/slot/) (and historical: [`shadow`](/html/element/shadow/))
-   [Using templates and slots](/web_components/using_templates_and_slots)