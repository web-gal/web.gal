---
title: '<applet>: The Embed Java Applet element'
tags:
  - Element
  - HTML
  - Java
  - Obsolete
  - Reference
  - Web
  - applet
permalink: html/element/applet
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/applet'
obsolete: true
browserCompact: html.elements.applet
---
{{ HTMLRef }}

The `<applet>` element was removed in [Gecko 56](https://bugzilla.mozilla.org/show_bug.cgi?id=1279218) and [Chrome 47](https://bugs.chromium.org/p/chromium/issues/detail?id=470301).

Removal is being considered in [WebKit](https://bugs.webkit.org/show_bug.cgi?id=157926) and [Edge](https://developer.microsoft.com/en-us/microsoft-edge/platform/issues/11946645/).

The obsolete **HTML Applet Element** (**`<applet>`**) embeds a Java applet into the document; this element has been deprecated in favor of [`object`](/html/element/object/).

Use of Java applets on the Web is deprecated; most browsers no longer support use of plug-ins, including the Java plug-in.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), [embedded content](/html/content_categories#embedded_content), interactive content, palpable content. |
| Permitted content | Zero or more [`param`](/html/element/param/) elements, then [transparent](/html/content_categories#transparent_content_model). |
| Tag omission | None, both the starting and ending tag are mandatory. |
| Permitted parents | Any element that accepts [embedded content](/html/content_categories#embedded_content). |
| DOM interface | {{ DOMxRef("HTMLAppletElement") }} |

## Attributes

{{ HTMLAttrDef("align") }}
: This attribute is used to position the applet on the page relative to content that might flow around it. The HTML 4.01 specification defines values of `bottom`, `left`, `middle`, `right`, and `top`, whereas Microsoft and Netscape also might support `absbottom`, `absmiddle`, `baseline`, `center`, and `texttop`.

{{ HTMLAttrDef("alt") }}
: This attribute causes a descriptive text alternate to be displayed on browsers that do not support Java. Page designers should also remember that content enclosed within the `<applet>` element may also be rendered as alternative text.

{{ HTMLAttrDef("archive") }}
: This attribute refers to an archived or compressed version of the applet and its associated class files, which might help reduce download time.

{{ HTMLAttrDef("code") }}
: This attribute specifies the URL of the applet's class file to be loaded and executed. Applet filenames are identified by a .class filename extension. The URL specified by code might be relative to the `codebase` attribute.

{{ HTMLAttrDef("codebase") }}
: This attribute gives the absolute or relative URL of the directory where applets' .class files referenced by the code attribute are stored.

{{ HTMLAttrDef("datafld") }}
: This attribute, supported by Internet Explorer 4 and higher, specifies the column name from the data source object that supplies the bound data. This attribute might be used to specify the various [`param`](/html/element/param/) elements passed to the Java applet.

{{ HTMLAttrDef("datasrc") }}
: Like `datafld`, this attribute is used for data binding under Internet Explorer 4. It indicates the id of the data source object that supplies the data that is bound to the [`param`](/html/element/param/) elements associated with the applet.

{{ HTMLAttrDef("height") }}
: This attribute specifies the height, in pixels, that the applet needs.

{{ HTMLAttrDef("hspace") }}
: This attribute specifies additional horizontal space, in pixels, to be reserved on either side of the applet.

{{ HTMLAttrDef("mayscript") }}
: In the Netscape implementation, this attribute allows access to an applet by programs in a scripting language embedded in the document.

{{ HTMLAttrDef("name") }}
: This attribute assigns a name to the applet so that it can be identified by other resources; particularly scripts.

{{ HTMLAttrDef("object") }}
: This attribute specifies the URL of a serialized representation of an applet.

{{ HTMLAttrDef("src") }}
: As defined for Internet Explorer 4 and higher, this attribute specifies a URL for an associated file for the applet. The meaning and use is unclear and not part of the HTML standard.

{{ HTMLAttrDef("vspace") }}
: This attribute specifies additional vertical space, in pixels, to be reserved above and below the applet.

{{ HTMLAttrDef("width") }}
: This attribute specifies in pixels the width that the applet needs.

## Example

### HTML

```html
<applet code="game.class" align="left" archive="game.zip" height="250" width="350">
  <param name="difficulty" value="easy">
  <b>Sorry, you need Java to play this game.</b>
</applet>

```

{{ EmbedLiveSample("Example", "100%", 300) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML 5.2** The definition of '<applet>' in that specification](https://www.w3.org/TR/html52/obsolete.html#the-applet-element) | {{ Spec2("HTML5.2") }} |  |
| [**HTML 5.1** The definition of '<applet>' in that specification](https://www.w3.org/TR/html51/obsolete.html#the-applet-element) | {{ Spec2("HTML5.1") }} |  |
| [**HTML 5** The definition of '<applet>' in that specification](https://www.w3.org/TR/html52/obsolete.html#the-applet-element) | {{ Spec2("HTML5 W3C") }} | Made obsolete |
| [**HTML 4.01 Specification** The definition of '<applet>' in that specification](https://www.w3.org/TR/html401/struct/objects.html#h-13.4) | {{ Spec2("HTML4.01") }} | Deprecated in favor of [`object`](/html/element/object/) |

## Browser compatibility

{{ Compat("html.elements.applet") }}

## Notes

The W3C specification does not encourage the use of `<applet>` and prefers the use of the [`object`](/html/element/object/) element. Under the strict definition of HTML 4.01, this element is deprecated and entirely obsolete in HTML5.