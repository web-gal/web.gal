---
title: data-*
tags:
  - Global attributes
  - HTML
  - Reference
permalink: html/global_attributes/data-*
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/data-*'
browserCompact: html.global_attributes.data_attributes
---
The **`data-*`** [global attributes](/html/global_attributes) form a class of attributes called **custom data attributes**, that allow proprietary information to be exchanged between the [HTML](/html "en/HTML") and its [DOM](/api/document_object_model "en/DOM") representation by scripts.

{{ EmbedInteractiveExample("pages/tabbed/attribute-data.html","tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

All such custom data are available via the {{ domxref("HTMLElement") }} interface of the element the attribute is set on. The {{ domxref("HTMLElement.dataset") }} property gives access to them.  
The `*` may be replaced by any name following [the production rule of XML names](http://www.w3.org/TR/REC-xml/#NT-Name "http://www.w3.org/TR/REC-xml/#NT-Name") with the following restrictions:

-   the name must not start with `xml`, whatever case is used for these letters;
-   the name must not contain any semicolon (`U+003A`);
-   the name must not contain capital letters.

Note that the {{ domxref("HTMLElement.dataset") }} property is a {{ domxref("DOMStringMap") }}, and the name of the custom data attribute _data-test-value_ will be accessible via `HTMLElement.dataset.testValue` (or by `HTMLElement.dataset["_testValue_"]`) as any dash (`U+002D`) is replaced by the capitalization of the next letter, converting the name to camelcase.

### Usage

By adding `data-*` attributes, even ordinary HTML elements can become rather complex and powerful program-objects. For example, a space-ship "[sprite](https://en.wikipedia.org/wiki/Sprite_(computer_graphics))_"_ in a game could be a simple [`img`](/html/element/img/) element with a [`class`](/html/global_attributes/class) attribute and several `data-*` attributes:

```html
<img class="spaceship cruiserX3" src="shipX3.png"
  data-ship-id="324" data-weapons="laserI laserII" data-shields="72%"
  data-x="414354" data-y="85160" data-z="31940"
  onclick="spaceships[this.dataset.shipId].blasted()">

```

For a more in-depth tutorial about using HTML data attributes, see [Using data attributes](/en-US/docs/Learn/HTML/Howto/Use_data_attributes).

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'data-*' in that specification](https://html.spec.whatwg.org/multipage/dom.html#embedding-custom-non-visible-data-with-the-data-*-attributes) | {{ Spec2('HTML WHATWG') }} | No change from latest snapshot, [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of 'data-*' in that specification](https://www.w3.org/TR/html51/dom.html#element-attrdef-global-data) | {{ Spec2('HTML5.1') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), no change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of 'data-*' in that specification](https://www.w3.org/TR/html52/dom.html#element-attrdef-global-data) | {{ Spec2('HTML5 W3C') }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/), initial definition. |

## Browser compatibility

The compatibility table on this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.global_attributes.data_attributes") }}

## See also

-   All [global attributes](/html/global_attributes).
-   The {{ domxref("HTMLElement.dataset") }} property that allows to access and modify these values.
-   [Using data attributes](/en-US/docs/Learn/HTML/Howto/Use_data_attributes)