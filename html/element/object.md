---
title: <object>
tags:
  - Element
  - HTML
  - HTML embedded content
  - Reference
  - Web
permalink: html/element/object
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/object'
browserCompact: html.elements.object
---
{{ HTMLRef }}

The **HTML `<object>` element** represents an external resource, which can be treated as an image, a nested browsing context, or a resource to be handled by a plugin.

{{ EmbedInteractiveExample("pages/tabbed/object.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content); [phrasing content](/html/content_categories#phrasing_content); [embedded content](/html/content_categories#embedded_content), palpable content; if the element has a {{ htmlattrxref("usemap","object") }} attribute, [interactive content](/html/content_categories#interactive_content); [listed](/html/content_categories#form_listed), [submittable](/html/content_categories#form_submittable) [form-associated](/html/content_categories#form-associated_content) element. |
| Permitted content | zero or more [`param`](/html/element/param/) elements, then [transparent](/html/content_categories#transparent_content_model). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [embedded content](/html/content_categories#embedded_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | [`application`](https://w3c.github.io/aria/#application), [`document`](https://w3c.github.io/aria/#document), [`image`](https://w3c.github.io/aria/#image) |
| DOM interface | {{ domxref("HTMLObjectElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ HTMLAttrDef("archive") }}{{ HTMLVersionInline(4) }} only{{ Obsolete_Inline("HTML5") }}
: A space-separated list of URIs for archives of resources for the object.

{{ HTMLAttrDef("border") }}{{ Deprecated_Inline("HTML4.01") }}{{ Obsolete_Inline("HTML5") }}
: The width of a border around the control, in pixels.

{{ HTMLAttrDef("classid") }}{{ HTMLVersionInline(4) }} only{{ Obsolete_Inline("HTML5") }}
: The URI of the object's implementation. It can be used together with, or in place of, the **data** attribute.

{{ HTMLAttrDef("codebase") }}{{ HTMLVersionInline(4) }} only{{ Obsolete_Inline("HTML5") }}
: The base path used to resolve relative URIs specified by **classid**, **data**, or **archive**. If not specified, the default is the base URI of the current document.

{{ HTMLAttrDef("codetype") }}{{ HTMLVersionInline(4) }} only{{ Obsolete_Inline("HTML5") }}
: The content type of the data specified by **classid**.

{{ HTMLAttrDef("data") }}
: The address of the resource as a valid URL. At least one of **data** and **type** must be defined.

{{ HTMLAttrDef("declare") }}{{ HTMLVersionInline(4) }} only{{ Obsolete_Inline("HTML5") }}
: The presence of this Boolean attribute makes this element a declaration only. The object must be instantiated by a subsequent `<object>` element. In HTML5, repeat the <object> element completely each that that the resource is reused.

{{ HTMLAttrDef("form") }}{{ HTMLVersionInline(5) }}
: The form element, if any, that the object element is associated with (its _form owner_). The value of the attribute must be an ID of a [`form`](/html/element/form/) element in the same document.

{{ HTMLAttrDef("height") }}
: The height of the displayed resource, in [CSS pixels](https://drafts.csswg.org/css-values/#px). -- (Absolute values only. [NO percentages](https://html.spec.whatwg.org/multipage/embedded-content.html#dimension-attributes))

{{ HTMLAttrDef("name") }}
: The name of valid browsing context (HTML5), or the name of the control (HTML 4).

{{ HTMLAttrDef("standby") }}{{ HTMLVersionInline(4) }} only{{ Obsolete_Inline("HTML5") }}
: A message that the browser can show while loading the object's implementation and data.

{{ HTMLAttrDef("tabindex") }}{{ HTMLVersionInline(4) }} only{{ Obsolete_Inline("HTML5") }}
: The position of the element in the tabbing navigation order for the current document.

{{ HTMLAttrDef("type") }}
: The [content type](/en-US/docs/Glossary/Content_type) of the resource specified by **data**. At least one of **data** and **type** must be defined.

{{ HTMLAttrDef("typemustmatch") }}{{ HTMLVersionInline(5) }}
: This Boolean attribute indicates if the **type** attribute and the actual [content type](/en-US/docs/Glossary/Content_type) of the resource must match to be used.

{{ HTMLAttrDef("usemap") }}
: A hash-name reference to a [`map`](/html/element/map/) element; that is a '#' followed by the value of a {{ htmlattrxref("name", "map") }} of a map element.

{{ HTMLAttrDef("width") }}
: The width of the display resource, in [CSS pixels](https://drafts.csswg.org/css-values/#px). -- (Absolute values only. [NO percentages](https://html.spec.whatwg.org/multipage/embedded-content.html#dimension-attributes))

## Examples

### Embed a flash movie

```html
<!-- Embed a flash movie -->
<object data="movie.swf"
  type="application/x-shockwave-flash"></object>

<!-- Embed a flash movie with parameters -->
<object data="movie.swf" type="application/x-shockwave-flash">
  <param name="foo" value="bar">
</object>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<object>' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#the-object-element) | {{ Spec2("HTML WHATWG") }} |  |
| [**HTML 5** The definition of '<object>' in that specification](https://www.w3.org/TR/html52/semantics-embedded-content.html#the-object-element) | {{ Spec2("HTML5 W3C") }} |  |
| [**HTML 4.01 Specification** The definition of '<object>' in that specification](https://www.w3.org/TR/html401/struct/objects.html#h-13.3) | {{ Spec2("HTML4.01") }} |  |

## Browser compatibility

Note: Google Chrome doesn't support search for text (accessed via ctrl + F shortcut) inside `<object></object>` tags.

{{ Compat("html.elements.object") }}

## See also

-   [`applet`](/html/element/applet/) {{ Obsolete_Inline }}
-   [`embed`](/html/element/embed/)
-   [`param`](/html/element/param/)