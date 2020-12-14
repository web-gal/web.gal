---
title: <map>
tags:
  - Element
  - HTML
  - HTML embedded content
  - Multimedia
  - Reference
  - Web
permalink: html/element/map
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/map'
browserCompact: html.elements.map
---
{{ HTMLRef }}

The **HTML `<map>` element** is used with [`area`](/html/element/area/) elements to define an image map (a clickable link area).

{{ EmbedInteractiveExample("pages/tabbed/map.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | Any [transparent](/html/content_categories#transparent_content_model) element. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLMapElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("name") }}
: The `name` attribute gives the map a name so that it can be referenced. The attribute must be present and must have a non-empty value with no space characters. The value of the `name` attribute must not be a compatibility-caseless match for the value of the `name` attribute of another `<map>` element in the same document. If the {{ htmlattrxref("id") }} attribute is also specified, both attributes must have the same value.

## Examples

```html
<map name="primary">
  <area shape="circle" coords="75,75,75" href="left.html">
  <area shape="circle" coords="275,75,75" href="right.html">
</map>
<img usemap="#primary" src="https://placehold.it/350x150" alt="350 x 150 pic">

```

### Result

{{ EmbedLiveSample('Examples', '350', '166', '', 'Web/HTML/Element/map')  }}

### Expected live example output

The live example above should appear similar to the following images (when using your keyboard tab key):

_For the `left.html` link:_  
![](https://mdn.mozillademos.org/files/14595/Screen%20Shot%202017-02-02%20at%2010.48.40%20PM.png)

_For the `right.html` link_  
![](https://mdn.mozillademos.org/files/14597/Screen%20Shot%202017-02-02%20at%2010.49.04%20PM.png)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<map>' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#the-map-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<map>' in that specification](https://www.w3.org/TR/html52/semantics-embedded-content.html#the-map-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<map>' in that specification](https://www.w3.org/TR/html401/struct/objects.html#h-13.6.1) | {{ Spec2('HTML4.01') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.map") }}

## See also

-   [`a`](/html/element/a/)
-   [`area`](/html/element/area/)