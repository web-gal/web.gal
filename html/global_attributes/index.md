---
title: Global attributes
tags:
  - Attribute
  - HTML
  - Reference
  - Web
permalink: html/global_attributes
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes'
browserCompact: html.global_attributes
---
**Global attributes** are attributes common to all HTML elements; they can be used on all elements, though they may have no effect on some elements.

Global attributes may be specified on all [HTML elements](/html/element), _even those not specified in the standard_. That means that any non-standard elements must still permit these attributes, even though using those elements means that the document is no longer HTML5-compliant. For example, HTML5-compliant browsers hide content marked as `<foo hidden>...</foo>`, even though `<foo>` is not a valid HTML element.

In addition to the basic HTML global attributes, the following global attributes also exist:

-   {{ HTMLAttrDef("xml:lang") }} and {{ HTMLAttrDef("xml:base") }} — these are inherited from the XHTML specifications and deprecated, but kept for compatibility purposes.
-   The multiple **`[aria-*](/accessibility/aria)`** attributes, used for improving accessibility.
-   The [event handler](/guide/events/event_handlers) attributes: **`onabort`**, **`onautocomplete`**, **`onautocompleteerror`**, **`onblur`**, **`oncancel`**, **`oncanplay`**, **`oncanplaythrough`**, **`onchange`**, **`onclick`**, **`onclose`**, **`oncontextmenu`**, **`oncuechange`**, **`ondblclick`**, **`ondrag`**, **`ondragend`**, **`ondragenter`**, **`ondragexit`**, **`ondragleave`**, **`ondragover`**, **`ondragstart`**, **`ondrop`**, **`ondurationchange`**, **`onemptied`**, **`onended`**, **`onerror`**, **`onfocus`**, **`oninput`**, **`oninvalid`**, **`onkeydown`**, **`onkeypress`**, **`onkeyup`**, **`onload`**, **`onloadeddata`**, **`onloadedmetadata`**, **`onloadstart`**, **`onmousedown`**, **`onmouseenter`**, **`onmouseleave`**, **`onmousemove`**, **`onmouseout`**, **`onmouseover`**, **`onmouseup`**, **`onmousewheel`**, **`onpause`**, **`onplay`**, **`onplaying`**, **`onprogress`**, **`onratechange`**, **`onreset`**, **`onresize`**, **`onscroll`**, **`onseeked`**, **`onseeking`**, **`onselect`**, **`onshow`**, **`onsort`**, **`onstalled`**, **`onsubmit`**, **`onsuspend`**, **`ontimeupdate`**, **`ontoggle`**, **`onvolumechange`**, **`onwaiting`**.

## List of global attributes

[{{ HTMLAttrDef("accesskey") }}](/html/global_attributes/accesskey)
: Provides a hint for generating a keyboard shortcut for the current element. This attribute consists of a space-separated list of characters. The browser should use the first one that exists on the computer keyboard layout.

[{{ HTMLAttrDef("autocapitalize") }}](/html/global_attributes/autocapitalize)
: Controls whether and how text input is automatically capitalized as it is entered/edited by the user. It can have the following values:

-   `off` or `none`, no autocapitalization is applied (all letters default to lowercase)
-   `on` or `sentences`, the first letter of each sentence defaults to a capital letter; all other letters default to lowercase
-   `words`, the first letter of each word defaults to a capital letter; all other letters default to lowercase
-   `characters`, all letters should default to uppercase

[{{ HTMLAttrDef("class") }}](/html/global_attributes/class)
: A space-separated list of the classes of the element. Classes allows CSS and JavaScript to select and access specific elements via the [class selectors](/css/class_selectors) or functions like the method {{ DOMxRef("Document.getElementsByClassName()") }}.

[{{ HTMLAttrDef("contenteditable") }}](/html/global_attributes/contenteditable)
: An enumerated attribute indicating if the element should be editable by the user. If so, the browser modifies its widget to allow editing. The attribute must take one of the following values:

-   `true` or the _empty string_, which indicates that the element must be editable;
-   `false`, which indicates that the element must not be editable.

[{{ HTMLAttrDef("contextmenu") }}](/html/global_attributes/contextmenu) {{ Obsolete_Inline }}
: The `[**id**](#attr-id)` of a [`menu`](/html/element/menu/) to use as the contextual menu for this element.

[{{ HTMLAttrDef("data-*") }}](/html/global_attributes/data-*)
: Forms a class of attributes, called custom data attributes, that allow proprietary information to be exchanged between the [HTML](/html) and its [DOM](/glossary/dom/) representation that may be used by scripts. All such custom data are available via the {{ DOMxRef("HTMLElement") }} interface of the element the attribute is set on. The {{ DOMxRef("HTMLElement.dataset") }} property gives access to them.

[{{ HTMLAttrDef("dir") }}](/html/global_attributes/dir)
: An enumerated attribute indicating the directionality of the element's text. It can have the following values:

-   `ltr`, which means _left to right_ and is to be used for languages that are written from the left to the right (like English);
-   `rtl`, which means _right to left_ and is to be used for languages that are written from the right to the left (like Arabic);
-   `auto`, which lets the user agent decide. It uses a basic algorithm as it parses the characters inside the element until it finds a character with a strong directionality, then it applies that directionality to the whole element.

[{{ HTMLAttrDef("draggable") }}](/html/global_attributes/draggable)
: An enumerated attribute indicating whether the element can be dragged, using the [Drag and Drop API](/en-us/docs/DragDrop/Drag_and_Drop). It can have the following values:

-   `true`, which indicates that the element may be dragged
-   `false`, which indicates that the element may not be dragged.

[{{ HTMLAttrDef("dropzone") }}](/html/global_attributes/dropzone) {{ deprecated_inline }}
: An enumerated attribute indicating what types of content can be dropped on an element, using the [Drag and Drop API](/en-US/docs/DragDrop/Drag_and_Drop). It can have the following values:

-   `copy`, which indicates that dropping will create a copy of the element that was dragged
-   `move`, which indicates that the element that was dragged will be moved to this new location.
-   `link`, will create a link to the dragged data.

[{{ HTMLAttrDef("exportparts") }}](/html/global_attributes/exportparts) {{ Experimental_Inline }}
: Used to transitively export shadow parts from a nested shadow tree into a containing light tree.

[{{ HTMLAttrDef("hidden") }}](/html/global_attributes/hidden)
: A Boolean attribute indicates that the element is not yet, or is no longer, _relevant_. For example, it can be used to hide elements of the page that can't be used until the login process has been completed. The browser won't render such elements. This attribute must not be used to hide content that could legitimately be shown.

[{{ HTMLAttrDef("id") }}](/html/global_attributes/id)
: Defines a unique identifier (ID) which must be unique in the whole document. Its purpose is to identify the element when linking (using a fragment identifier), scripting, or styling (with CSS).

[{{ HTMLAttrDef("inputmode") }}](/html/global_attributes/inputmode)
: Provides a hint to browsers as to the type of virtual keyboard configuration to use when editing this element or its contents. Used primarily on [`input`](/html/element/input/) elements, but is usable on any element while in {{ HTMLAttrxRef("contenteditable") }} mode.

[{{ HTMLAttrDef("is") }}](/html/global_attributes/is)
: Allows you to specify that a standard HTML element should behave like a registered custom built-in element (see [Using custom elements](/web_components/using_custom_elements) for more details).

**Note:** The `item*` attributes are part of the [WHATWG HTML Microdata feature](https://html.spec.whatwg.org/multipage/microdata.html#microdata).

[{{ HTMLAttrDef("itemid") }}](/html/global_attributes/itemid)
: The unique, global identifier of an item.

[{{ HTMLAttrDef("itemprop") }}](/html/global_attributes/itemprop)
: Used to add properties to an item. Every HTML element may have an `itemprop` attribute specified, where an `itemprop` consists of a name and value pair.

[{{ HTMLAttrDef("itemref") }}](/html/global_attributes/itemref)
: Properties that are not descendants of an element with the `itemscope` attribute can be associated with the item using an `itemref`. It provides a list of element ids (not `itemid`s) with additional properties elsewhere in the document.

[{{ HTMLAttrDef("itemscope") }}](/html/global_attributes/itemscope)
: `itemscope` (usually) works along with {{ HTMLAttrxRef("itemtype") }} to specify that the HTML contained in a block is about a particular item. `itemscope` creates the Item and defines the scope of the `itemtype` associated with it. `itemtype` is a valid URL of a vocabulary (such as [schema.org](https://schema.org/)) that describes the item and its properties context.

[{{ HTMLAttrDef("itemtype") }}](/html/global_attributes/itemtype)
: Specifies the URL of the vocabulary that will be used to define `itemprop`s (item properties) in the data structure. {{ HTMLAttrxRef("itemscope") }} is used to set the scope of where in the data structure the vocabulary set by `itemtype` will be active.

[{{ HTMLAttrDef("lang") }}](/html/global_attributes/lang)
: Helps define the language of an element: the language that non-editable elements are in, or the language that editable elements should be written in by the user. The attribute contains one “language tag” (made of hyphen-separated “language subtags”) in the format defined in [_Tags for Identifying Languages (BCP47)_](https://www.ietf.org/rfc/bcp/bcp47.txt). [**xml:lang**](#attr-xml:lang) has priority over it.

[{{ HTMLAttrDef("part") }}](/html/global_attributes/part)
: A space-separated list of the part names of the element. Part names allows CSS to select and style specific elements in a shadow tree via the {{ CSSxRef("::part") }} pseudo-element.

[{{ HTMLAttrDef("slot") }}](/html/global_attributes/slot)
: Assigns a slot in a [shadow DOM](/web_components/shadow_dom) shadow tree to an element: An element with a `slot` attribute is assigned to the slot created by the [`slot`](/html/element/slot/) element whose {{ HTMLAttrxRef("name", "slot") }} attribute's value matches that `slot` attribute's value.

[{{ HTMLAttrDef("spellcheck") }}](/html/global_attributes/spellcheck)
: An enumerated attribute defines whether the element may be checked for spelling errors. It may have the following values:

-   `true`, which indicates that the element should be, if possible, checked for spelling errors;
-   `false`, which indicates that the element should not be checked for spelling errors.

[{{ HTMLAttrDef("style") }}](/html/global_attributes/style)
: Contains [CSS](/css) styling declarations to be applied to the element. Note that it is recommended for styles to be defined in a separate file or files. This attribute and the [`style`](/html/element/style/) element have mainly the purpose of allowing for quick styling, for example for testing purposes.

[{{ HTMLAttrDef("tabindex") }}](/html/global_attributes/tabindex)
: An integer attribute indicating if the element can take input focus (is _focusable_), if it should participate to sequential keyboard navigation, and if so, at what position. It can take several values:

-   a _negative value_ means that the element should be focusable, but should not be reachable via sequential keyboard navigation;
-   `0` means that the element should be focusable and reachable via sequential keyboard navigation, but its relative order is defined by the platform convention;
-   a _positive value_ means that the element should be focusable and reachable via sequential keyboard navigation; the order in which the elements are focused is the increasing value of the [**tabindex**](#attr-tabindex). If several elements share the same tabindex, their relative order follows their relative positions in the document.

[{{ HTMLAttrDef("title") }}](/html/global_attributes/title)
: Contains a text representing advisory information related to the element it belongs to. Such information can typically, but not necessarily, be presented to the user as a tooltip.

[{{ HTMLAttrDef("translate") }}](/html/global_attributes/translate) {{ Experimental_Inline }}
: An enumerated attribute that is used to specify whether an element's attribute values and the values of its {{ DOMxRef("Text") }} node children are to be translated when the page is localized, or whether to leave them unchanged. It can have the following values:

-   empty string and `yes`, which indicates that the element will be translated.
-   `no`, which indicates that the element will not be translated.

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'Global attributes' in that specification](https://html.spec.whatwg.org/multipage/dom.html#global-attributes) | {{ Spec2("HTML WHATWG") }} |  |
| [**Shadow Parts**](https://drafts.csswg.org/css-shadow-parts-1/#exposing) | {{ Spec2("CSS Shadow Parts") }} | Added the `part` and `exportparts` global attributes. |
| [**HTML 5.2** The definition of 'Global attributes' in that specification](https://www.w3.org/TR/html52/dom.html#global-attributes) | {{ Spec2("HTML5.2") }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/). From [**HTML 5.1**](https://www.w3.org/TR/html51/), `itemid`, `itemprop`, `itemref`, `itemscope`, and `itemtype` have been added. |
| [**HTML 5.1** The definition of 'Global attributes' in that specification](https://www.w3.org/TR/html51/dom.html#global-attributes) | {{ Spec2("HTML5.1") }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/). From [**HTML 5**](https://www.w3.org/TR/html52/), `contextmenu`, `draggable`, `dropzone`, and `spellcheck` have been added. |
| [**HTML 5** The definition of 'Global attributes' in that specification](https://www.w3.org/TR/html52/dom.html#global-attributes) | {{ Spec2("HTML5 W3C") }} | Snapshot of [**HTML Living Standard**](https://html.spec.whatwg.org/multipage/). From [**HTML 4.01 Specification**](https://www.w3.org/TR/html401/), the concept of global attributes is introduced and the `dir`, `lang`, `style`, `id`, `class`, `tabindex`, `accesskey`, and `title` are now true global attributes.  
`xml:lang` which was initially part of XHTML, is now also part of HTML.  
`hidden`, `data-*`, `contenteditable`, and `translate` have been added. |
| [**HTML 4.01 Specification**](https://www.w3.org/TR/html401/) | {{ Spec2("HTML4.01") }} | There are no global attributes defined. Several attributes that will become global attributes in subsequent specifications are defined on a subset of elements.  
`class` and `style` are supported on all elements but [`base`](/html/element/base/), [`basefont`](/html/element/basefont/), [`head`](/html/element/head/), [`html`](/html/element/html/), [`meta`](/html/element/meta/), [`param`](/html/element/param/), [`script`](/html/element/script/), [`style`](/html/element/style/), and [`title`](/html/element/title/).  
`dir` is supported on all elements but [`applet`](/html/element/applet/), [`base`](/html/element/base/), [`basefont`](/html/element/basefont/), [`bdo`](/html/element/bdo/), [`br`](/html/element/br/), [`frame`](/html/element/frame/), [`frameset`](/html/element/frameset/), [`iframe`](/html/element/iframe/), [`param`](/html/element/param/), and [`script`](/html/element/script/).  
`id` is supported on all elements but [`base`](/html/element/base/), [`head`](/html/element/head/), [`html`](/html/element/html/), [`meta`](/html/element/meta/), [`script`](/html/element/script/), [`style`](/html/element/style/), and [`title`](/html/element/title/).  
`lang` is supported on all elements but [`applet`](/html/element/applet/), [`base`](/html/element/base/), [`basefont`](/html/element/basefont/), [`br`](/html/element/br/), [`frame`](/html/element/frame/), [`frameset`](/html/element/frameset/), [`iframe`](/html/element/iframe/), [`param`](/html/element/param/), and [`script`](/html/element/script/).  
`tabindex` is only supported on [`a`](/html/element/a/), [`area`](/html/element/area/), [`button`](/html/element/button/), [`object`](/html/element/object/), [`select`](/html/element/select/), and [`textarea`](/html/element/textarea/).  
`accesskey` is only supported on [`a`](/html/element/a/), [`area`](/html/element/area/), [`button`](/html/element/button/), [`input`](/html/element/input/), [`label`](/html/element/label/), [`legend`](/html/element/legend/) and [`textarea`](/html/element/textarea/).  
`title` is supported on all elements but [`base`](/html/element/base/), [`basefont`](/html/element/basefont/), [`head`](/html/element/head/), [`html`](/html/element/html/), [`meta`](/html/element/meta/), [`param`](/html/element/param/), [`script`](/html/element/script/), and [`title`](/html/element/title/). |

## Browser compatibility

{{ Compat("html.global_attributes") }}

## See also

-   {{ DOMxRef("Element") }} and {{ DOMxRef("GlobalEventHandlers") }} interfaces that allow to query most global attributes.