---
title: HTML attribute reference
tags:
  - Attribute
  - Attributes
  - Beginner
  - Configuring
  - Element Attributes
  - Elements
  - HTML
  - Reference
  - Settings
  - Web
permalink: html/attributes
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes'
---
Elements in HTML have **attributes**; these are additional values that configure the elements or adjust their behavior in various ways to meet the criteria the users want.

## Attribute list

| Attribute Name | Elements | Description |
| --- | --- | --- |
| `[accept](/html/attributes/accept)` | [`form`](/html/element/form/), [`input`](/html/element/input/) | List of types the server accepts, typically a file type. |
| `[accept-charset](/html/attributes/accept-charset)` | [`form`](/html/element/form/) | List of supported charsets. |
| `[accesskey](/html/global_attributes/accesskey)` | [Global attribute](/html/global_attributes) | Keyboard shortcut to activate or add focus to the element. |
| `[action](/html/attributes/action)` | [`form`](/html/element/form/) | The URI of a program that processes the information submitted via the form. |
| `[align](/html/attributes/align)` | [`applet`](/html/element/applet/), [`caption`](/html/element/caption/), [`col`](/html/element/col/), [`colgroup`](/html/element/colgroup/), [`hr`](/html/element/hr/), [`iframe`](/html/element/iframe/), [`img`](/html/element/img/), [`table`](/html/element/table/), [`tbody`](/html/element/tbody/), [`td`](/html/element/td/), [`tfoot`](/html/element/tfoot/) , [`th`](/html/element/th/), [`thead`](/html/element/thead/), [`tr`](/html/element/tr/) | Specifies the horizontal alignment of the element. |
| `[allow](/html/attributes/allow)` | [`iframe`](/html/element/iframe/) | Specifies a feature-policy for the iframe. |
| `[alt](/html/attributes/alt)` | [`applet`](/html/element/applet/), [`area`](/html/element/area/), [`img`](/html/element/img/), [`input`](/html/element/input/) | Alternative text in case an image can't be displayed. |
| `[async](/html/attributes/async)` | [`script`](/html/element/script/) | Executes the script asynchronously. |
| `[autocapitalize](/html/global_attributes/autocapitalize)` | [Global attribute](/html/global_attributes) | Sets whether input is automatically capitalized when entered by user |
| `[autocomplete](/html/attributes/autocomplete)` | [`form`](/html/element/form/), [`input`](/html/element/input/), [`select`](/html/element/select/), [`textarea`](/html/element/textarea/) | Indicates whether controls in this form can by default have their values automatically completed by the browser. |
| `[autofocus](/html/attributes/autofocus)` | [`button`](/html/element/button/), [`input`](/html/element/input/), [`keygen`](/html/element/keygen/), [`select`](/html/element/select/), [`textarea`](/html/element/textarea/) | The element should be automatically focused after the page loaded. |
| `[autoplay](/html/attributes/autoplay)` | [`audio`](/html/element/audio/), [`video`](/html/element/video/) | The audio or video should play as soon as possible. |
| `background` | [`body`](/html/element/body/), [`table`](/html/element/table/), [`td`](/html/element/td/), [`th`](/html/element/th/) | Specifies the URL of an image file.
**Note:** Although browsers and email clients may still support this attribute, it is obsolete. Use CSS {{ Cssxref("background-image")  }} instead.

 |
| `bgcolor` | [`body`](/html/element/body/), [`col`](/html/element/col/), [`colgroup`](/html/element/colgroup/), [`marquee`](/html/element/marquee/), [`table`](/html/element/table/), [`tbody`](/html/element/tbody/), [`tfoot`](/html/element/tfoot/), [`td`](/html/element/td/), [`th`](/html/element/th/), [`tr`](/html/element/tr/) | 

Background color of the element.

**Note:** This is a legacy attribute. Please use the CSS {{ Cssxref("background-color")  }} property instead.



 |
| `border` | [`img`](/html/element/img/), [`object`](/html/element/object/), [`table`](/html/element/table/) | 

The border width.

**Note:** This is a legacy attribute. Please use the CSS {{ Cssxref("border")  }} property instead.



 |
| `[buffered](/html/attributes/buffered)` | [`audio`](/html/element/audio/), [`video`](/html/element/video/) | Contains the time range of already buffered media. |
| `[capture](/html/attributes/capture)` | [`input`](/html/element/input/) | From the [**HTML Media Capture** The definition of 'media capture' in that specification](https://w3c.github.io/html-media-capture/#the-capture-attribute)spec, specifies a new file can be captured. |
| `challenge` | [`keygen`](/html/element/keygen/) | A challenge string that is submitted along with the public key. |
| `[charset](/html/attributes/charset)` | [`meta`](/html/element/meta/), [`script`](/html/element/script/) | Declares the character encoding of the page or script. |
| `[checked](/html/attributes/checked)` | [`command`](/html/element/command/), [`input`](/html/element/input/) | Indicates whether the element should be checked on page load. |
| `[cite](/html/attributes/cite)` | [`blockquote`](/html/element/blockquote/), [`del`](/html/element/del/), [`ins`](/html/element/ins/), [`q`](/html/element/q/) | Contains a URI which points to the source of the quote or change. |
| `[class](/html/global_attributes/class)` | [Global attribute](/html/global_attributes) | Often used with CSS to style elements with common properties. |
| `[code](/html/attributes/code)` | [`applet`](/html/element/applet/) | Specifies the URL of the applet's class file to be loaded and executed. |
| `[codebase](/html/attributes/codebase)` | [`applet`](/html/element/applet/) | This attribute gives the absolute or relative URL of the directory where applets' .class files referenced by the code attribute are stored. |
| `color` | [`basefont`](/html/element/basefont/), [`font`](/html/element/font/), [`hr`](/html/element/hr/) | 

This attribute sets the text color using either a named color or a color specified in the hexadecimal #RRGGBB format.

**Note:** This is a legacy attribute. Please use the CSS {{ Cssxref("color")  }} property instead.



 |
| `[cols](/html/attributes/cols)` | [`textarea`](/html/element/textarea/) | Defines the number of columns in a textarea. |
| `[colspan](/html/attributes/colspan)` | [`td`](/html/element/td/), [`th`](/html/element/th/) | The colspan attribute defines the number of columns a cell should span. |
| `[content](/html/attributes/content)` | [`meta`](/html/element/meta/) | A value associated with `http-equiv` or `name` depending on the context. |
| `[contenteditable](/html/global_attributes/contenteditable)` | [Global attribute](/html/global_attributes) | Indicates whether the element's content is editable. |
| `[contextmenu](/html/attributes/contextmenu)` | [Global attribute](/html/global_attributes) | Defines the ID of a [`menu`](/html/element/menu/) element which will serve as the element's context menu. |
| `[controls](/html/attributes/controls)` | [`audio`](/html/element/audio/), [`video`](/html/element/video/) | Indicates whether the browser should show playback controls to the user. |
| `[coords](/html/attributes/coords)` | [`area`](/html/element/area/) | A set of values specifying the coordinates of the hot-spot region. |
| `[crossorigin](/docs/Web/HTML/CORS_settings_attributes)` | [`audio`](/html/element/audio/), [`img`](/html/element/img/), [`link`](/html/element/link/), [`script`](/html/element/script/), [`video`](/html/element/video/) | How the element handles cross-origin requests |
| `[csp](/docs/Web/API/HTMLiframeElement/csp)` {{ experimental_inline }} | [`iframe`](/html/element/iframe/) | Specifies the Content Security Policy that an embedded document must agree to enforce upon itself. |
| `[data](/html/attributes/data)` | [`object`](/html/element/object/) | Specifies the URL of the resource. |
| `[data-*](/html/global_attributes/data-*)` | [Global attribute](/html/global_attributes) | Lets you attach custom attributes to an HTML element. |
| `[datetime](/html/attributes/datetime)` | [`del`](/html/element/del/), [`ins`](/html/element/ins/), [`time`](/html/element/time/) | Indicates the date and time associated with the element. |
| `[decoding](/html/attributes/decoding)` | [`img`](/html/element/img/) | Indicates the preferred method to decode the image. |
| `[default](/html/attributes/default)` | [`track`](/html/element/track/) | Indicates that the track should be enabled unless the user's preferences indicate something different. |
| `[defer](/html/attributes/defer)` | [`script`](/html/element/script/) | Indicates that the script should be executed after the page has been parsed. |
| `[dir](/html/global_attributes/dir)` | [Global attribute](/html/global_attributes) | Defines the text direction. Allowed values are ltr (Left-To-Right) or rtl (Right-To-Left) |
| `[dirname](/html/attributes/dirname)` | [`input`](/html/element/input/), [`textarea`](/html/element/textarea/) |  |
| `[disabled](/html/attributes/disabled)` | [`button`](/html/element/button/), [`command`](/html/element/command/), [`fieldset`](/html/element/fieldset/), [`input`](/html/element/input/), [`keygen`](/html/element/keygen/), [`optgroup`](/html/element/optgroup/), [`option`](/html/element/option/), [`select`](/html/element/select/), [`textarea`](/html/element/textarea/) | Indicates whether the user can interact with the element. |
| `[download](/html/attributes/download)` | [`a`](/html/element/a/), [`area`](/html/element/area/) | Indicates that the hyperlink is to be used for downloading a resource. |
| `[draggable](/html/global_attributes/draggable)` | [Global attribute](/html/global_attributes) | Defines whether the element can be dragged. |
| `[dropzone](/html/global_attributes/dropzone)` | [Global attribute](/html/global_attributes) | Indicates that the element accepts the dropping of content onto it. |
| `[enctype](/html/attributes/enctype)` | [`form`](/html/element/form/) | Defines the content type of the form data when the `method` is POST. |
| `[enterkeyhint](/html/attributes/enterkeyhint)` {{ experimental_inline }} | [`textarea`](/html/element/textarea/), [`contenteditable`](/html/global_attributes/contenteditable) | The [`enterkeyhint`](https://html.spec.whatwg.org/dev/interaction.html#input-modalities:-the-enterkeyhint-attribute) specifies what action label (or icon) to present for the enter key on virtual keyboards. The attribute can be used with form controls (such as the value of `textarea` elements), or in elements in an editing host (e.g., using `contenteditable` attribute). |
| `[for](/html/attributes/for)` | [`label`](/html/element/label/), [`output`](/html/element/output/) | Describes elements which belongs to this one. |
| `[form](/html/attributes/form)` | [`button`](/html/element/button/), [`fieldset`](/html/element/fieldset/), [`input`](/html/element/input/), [`keygen`](/html/element/keygen/), [`label`](/html/element/label/), [`meter`](/html/element/meter/), [`object`](/html/element/object/), [`output`](/html/element/output/), [`progress`](/html/element/progress/), [`select`](/html/element/select/), [`textarea`](/html/element/textarea/) | Indicates the form that is the owner of the element. |
| `[formaction](/html/attributes/formaction)` | [`input`](/html/element/input/), [`button`](/html/element/button/) | Indicates the action of the element, overriding the action defined in the [`form`](/html/element/form/). |
| `[formenctype](/html/attributes/formenctype)` | [`button`](/html/element/button/), [`input`](/html/element/input/) | If the button/input is a submit button (`type="submit"`), this attribute sets the encoding type to use during form submission. If this attribute is specified, it overrides the `enctype` attribute of the button's [form](/html/element/form) owner. |
| `[formmethod](/html/attributes/formmethod)` | [`button`](/html/element/button/), [`input`](/html/element/input/) | If the button/input is a submit button (`type="submit"`), this attribute sets the submission method to use during form submission (`GET`, `POST`, etc.). If this attribute is specified, it overrides the `method` attribute of the button's [form](/html/element/form) owner. |
| `[formnovalidate](/html/attributes/formnovalidate)` | [`button`](/html/element/button/), [`input`](/html/element/input/) | If the button/input is a submit button (`type="submit"`), this boolean attribute specifies that the form is not to be validated when it is submitted. If this attribute is specified, it overrides the `novalidate` attribute of the button's [form](/html/element/form) owner. |
| `[formtarget](/html/attributes/formtarget)` | [`button`](/html/element/button/), [`input`](/html/element/input/) | If the button/input is a submit button (`type="submit"`), this attribute specifies the browsing context (for example, tab, window, or inline frame) in which to display the response that is received after submitting the form. If this attribute is specified, it overrides the `target` attribute of the button's [form](/html/element/form) owner. |
| `[headers](/html/attributes/headers)` | [`td`](/html/element/td/), [`th`](/html/element/th/) | IDs of the `<th>` elements which applies to this element. |
| `height` | [`canvas`](/html/element/canvas/), [`embed`](/html/element/embed/), [`iframe`](/html/element/iframe/), [`img`](/html/element/img/), [`input`](/html/element/input/), [`object`](/html/element/object/), [`video`](/html/element/video/) | 

Specifies the height of elements listed here. For all other elements, use the CSS {{ cssxref("height") }} property.

**Note:** In some instances, such as [`div`](/html/element/div/), this is a legacy attribute, in which case the CSS {{ Cssxref("height")  }} property should be used instead.



 |
| `[hidden](/html/global_attributes/hidden)` | [Global attribute](/html/global_attributes) | Prevents rendering of given element, while keeping child elements, e.g. script elements, active. |
| `[high](/html/attributes/high)` | [`meter`](/html/element/meter/) | Indicates the lower bound of the upper range. |
| `[href](/html/attributes/href)` | [`a`](/html/element/a/), [`area`](/html/element/area/), [`base`](/html/element/base/), [`link`](/html/element/link/) | The URL of a linked resource. |
| `[hreflang](/html/attributes/hreflang)` | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | Specifies the language of the linked resource. |
| `[http-equiv](/html/attributes/http-equiv)` | [`meta`](/html/element/meta/) | Defines a pragma directive. |
| `[icon](/html/attributes/icon)` | [`command`](/html/element/command/) | Specifies a picture which represents the command. |
| `[id](/html/global_attributes/id)` | [Global attribute](/html/global_attributes) | Often used with CSS to style a specific element. The value of this attribute must be unique. |
| `[importance](/html/attributes/importance)` {{ experimental_inline }} | [`iframe`](/html/element/iframe/), [`img`](/html/element/img/), [`link`](/html/element/link/), [`script`](/html/element/script/) | Indicates the relative fetch priority for the resource. |
| `[integrity](/security/subresource_integrity)` | [`link`](/html/element/link/), [`script`](/html/element/script/) | 

Specifies a [Subresource Integrity](/security/subresource_integrity) value that allows browsers to verify what they fetch.

 |
| [`intrinsicsize`](/html/element/img#attr-intrinsicsize) {{ deprecated_inline }} | [`img`](/html/element/img/) | This attribute tells the browser to ignore the actual intrinsic size of the image and pretend it’s the size specified in the attribute. |
| [`inputmode`](/html/global_attributes/inputmode) | [`textarea`](/html/element/textarea/), [`contenteditable`](/html/global_attributes/contenteditable) | Provides a hint as to the type of data that might be entered by the user while editing the element or its contents. The attribute can be used with form controls (such as the value of `textarea` elements), or in elements in an editing host (e.g., using `contenteditable` attribute). |
| `ismap` | [`img`](/html/element/img/) | Indicates that the image is part of a server-side image map. |
| `[itemprop](/html/global_attributes/itemprop)` | [Global attribute](/html/global_attributes) |  |
| `keytype` | [`keygen`](/html/element/keygen/) | Specifies the type of key generated. |
| `[kind](/html/attributes/kind)` | [`track`](/html/element/track/) | Specifies the kind of text track. |
| `[label](/html/attributes/label)` | [`optgroup`](/html/element/optgroup/), [`option`](/html/element/option/), [`track`](/html/element/track/) | Specifies a user-readable title of the element. |
| `[lang](/html/global_attributes/lang)` | [Global attribute](/html/global_attributes) | Defines the language used in the element. |
| `[language](/html/attributes/language)` | [`script`](/html/element/script/) | Defines the script language used in the element. |
| `loading` {{ experimental_inline }} | [`img`](/html/element/img/), [`iframe`](/html/element/iframe/) | Indicates if the element should be loaded lazily (`loading="lazy"`) or loaded immediately (`loading="eager"`).

**WIP:** [WHATWG PR #3752](https://github.com/whatwg/html/pull/3752)

 |
| `[list](/html/attributes/list)` | [`input`](/html/element/input/) | Identifies a list of pre-defined options to suggest to the user. |
| `[loop](/html/attributes/loop)` | [`audio`](/html/element/audio/), [`bgsound`](/html/element/bgsound/), [`marquee`](/html/element/marquee/), [`video`](/html/element/video/) | Indicates whether the media should start playing from the start when it's finished. |
| `[low](/html/attributes/low)` | [`meter`](/html/element/meter/) | Indicates the upper bound of the lower range. |
| `manifest` | [`html`](/html/element/html/) | Specifies the URL of the document's cache manifest.

**Note:** This attribute is obsolete, use [`<link rel="manifest">`](/manifest) instead.

 |
| `[max](/html/attributes/max)` | [`input`](/html/element/input/), [`meter`](/html/element/meter/), [`progress`](/html/element/progress/) | Indicates the maximum value allowed. |
| `[maxlength](/html/attributes/maxlength)` | [`input`](/html/element/input/), [`textarea`](/html/element/textarea/) | Defines the maximum number of characters allowed in the element. |
| `[minlength](/html/attributes/minlength)` | [`input`](/html/element/input/), [`textarea`](/html/element/textarea/) | Defines the minimum number of characters allowed in the element. |
| `[media](/html/attributes/media)` | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/), [`source`](/html/element/source/), [`style`](/html/element/style/) | Specifies a hint of the media for which the linked resource was designed. |
| [method](/html/attributes/method) | [`form`](/html/element/form/) | Defines which [HTTP](/http) method to use when submitting the form. Can be `GET` (default) or `POST`. |
| `[min](/html/attributes/min)` | [`input`](/html/element/input/), [`meter`](/html/element/meter/) | Indicates the minimum value allowed. |
| `[multiple](/html/attributes/multiple)` | [`input`](/html/element/input/), [`select`](/html/element/select/) | Indicates whether multiple values can be entered in an input of the type `email` or `file`. |
| `[muted](/html/attributes/muted)` | [`audio`](/html/element/audio/), [`video`](/html/element/video/) | Indicates whether the audio will be initially silenced on page load. |
| `[name](/html/attributes/name)` | [`button`](/html/element/button/), [`form`](/html/element/form/), [`fieldset`](/html/element/fieldset/), [`iframe`](/html/element/iframe/), [`input`](/html/element/input/), [`keygen`](/html/element/keygen/), [`object`](/html/element/object/), [`output`](/html/element/output/), [`select`](/html/element/select/), [`textarea`](/html/element/textarea/), [`map`](/html/element/map/), [`meta`](/html/element/meta/), [`param`](/html/element/param/) | Name of the element. For example used by the server to identify the fields in form submits. |
| `[novalidate](/html/attributes/novalidate)` | [`form`](/html/element/form/) | This attribute indicates that the form shouldn't be validated when submitted. |
| `[open](/html/attributes/open)` | [`details`](/html/element/details/) | Indicates whether the details will be shown on page load. |
| `[optimum](/html/attributes/optimum)` | [`meter`](/html/element/meter/) | Indicates the optimal numeric value. |
| `[pattern](/html/attributes/pattern)` | [`input`](/html/element/input/) | Defines a regular expression which the element's value will be validated against. |
| `[ping](/html/element/a#attr-ping)` | [`a`](/html/element/a/), [`area`](/html/element/area/) | The `ping` attribute specifies a space-separated list of URLs to be notified if a user follows the hyperlink. |
| `[placeholder](/html/attributes/placeholder)` | [`input`](/html/element/input/), [`textarea`](/html/element/textarea/) | Provides a hint to the user of what can be entered in the field. |
| `[poster](/html/attributes/poster)` | [`video`](/html/element/video/) | A URL indicating a poster frame to show until the user plays or seeks. |
| `[preload](/html/attributes/preload)` | [`audio`](/html/element/audio/), [`video`](/html/element/video/) | Indicates whether the whole resource, parts of it or nothing should be preloaded. |
| `radiogroup` | [`command`](/html/element/command/) |  |
| `[readonly](/html/attributes/readonly)` | [`input`](/html/element/input/), [`textarea`](/html/element/textarea/) | Indicates whether the element can be edited. |
| `[referrerpolicy](/html/attributes/referralpolicy)` | [`a`](/html/element/a/), [`area`](/html/element/area/), [`iframe`](/html/element/iframe/), [`img`](/html/element/img/), [`link`](/html/element/link/), [`script`](/html/element/script/) | Specifies which referrer is sent when fetching the resource. |
| `[rel](/html/attributes/rel)` | [`a`](/html/element/a/), [`area`](/html/element/area/), [`link`](/html/element/link/) | Specifies the relationship of the target object to the link object. |
| `[required](/html/attributes/required)` | [`input`](/html/element/input/), [`select`](/html/element/select/), [`textarea`](/html/element/textarea/) | Indicates whether this element is required to fill out or not. |
| `[reversed](/html/attributes/reversed)` | [`ol`](/html/element/ol/) | Indicates whether the list should be displayed in a descending order instead of a ascending. |
| `[rows](/html/attributes/rows)` | [`textarea`](/html/element/textarea/) | Defines the number of rows in a text area. |
| `[rowspan](/html/attributes/rowspan)` | [`td`](/html/element/td/), [`th`](/html/element/th/) | Defines the number of rows a table cell should span over. |
| `[sandbox](/html/element/iframe#attr-sandbox)` | [`iframe`](/html/element/iframe/) | Stops a document loaded in an iframe from using certain features (such as submitting forms or opening new windows). |
| `[scope](/html/attributes/scope)` | [`th`](/html/element/th/) | Defines the cells that the header test (defined in the `th` element) relates to. |
| `[scoped](/html/attributes/scoped)` | [`style`](/html/element/style/) |  |
| `[selected](/html/attributes/selected)` | [`option`](/html/element/option/) | Defines a value which will be selected on page load. |
| `[shape](/html/attributes/shape)` | [`a`](/html/element/a/), [`area`](/html/element/area/) |  |
| `[size](/html/attributes/size)` | [`input`](/html/element/input/), [`select`](/html/element/select/) | Defines the width of the element (in pixels). If the element's `type` attribute is `text` or `password` then it's the number of characters. |
| `[sizes](/html/attributes/sizes)` | [`link`](/html/element/link/), [`img`](/html/element/img/), [`source`](/html/element/source/) |  |
| `[slot](/html/attributes/slot)` | [Global attribute](/html/global_attributes) | Assigns a slot in a shadow DOM shadow tree to an element. |
| `[span](/html/attributes/span)` | [`col`](/html/element/col/), [`colgroup`](/html/element/colgroup/) |  |
| `[spellcheck](/html/global_attributes/spellcheck)` | [Global attribute](/html/global_attributes) | Indicates whether spell checking is allowed for the element. |
| `[src](/html/attributes/src)` | [`audio`](/html/element/audio/), [`embed`](/html/element/embed/), [`iframe`](/html/element/iframe/), [`img`](/html/element/img/), [`input`](/html/element/input/), [`script`](/html/element/script/), [`source`](/html/element/source/), [`track`](/html/element/track/), [`video`](/html/element/video/) | The URL of the embeddable content. |
| `[srcdoc](/html/attributes/srcdoc)` | [`iframe`](/html/element/iframe/) |  |
| `[srclang](/html/attributes/srclang)` | [`track`](/html/element/track/) |  |
| `[srcset](/html/attributes/srcset)` | [`img`](/html/element/img/), [`source`](/html/element/source/) | One or more responsive image candidates. |
| `[start](/html/attributes/start)` | [`ol`](/html/element/ol/) | Defines the first number if other than 1. |
| `[step](/html/attributes/step)` | [`input`](/html/element/input/) |  |
| `[style](/html/global_attributes/style)` | [Global attribute](/html/global_attributes) | Defines CSS styles which will override styles previously set. |
| `[summary](/html/attributes/summary)` | [`table`](/html/element/table/) |  |
| `[tabindex](/html/global_attributes/tabindex)` | [Global attribute](/html/global_attributes) | Overrides the browser's default tab order and follows the one specified instead. |
| `[target](/html/attributes/target)` | [`a`](/html/element/a/), [`area`](/html/element/area/), [`base`](/html/element/base/), [`form`](/html/element/form/) | Specifies where to open the linked document (in the case of an `<a>` element) or where to display the response recieved (in the case of a `<form>` element) |
| `[title](/html/global_attributes/title)` | [Global attribute](/html/global_attributes) | Text to be displayed in a tooltip when hovering over the element. |
| `[translate](/html/global_attributes/translate)` | [Global attribute](/html/global_attributes) | Specify whether an element’s attribute values and the values of its `[Text](https://dom.spec.whatwg.org/#text)` node children are to be translated when the page is localized, or whether to leave them unchanged. |
| `[type](/html/attributes/type)` | [`button`](/html/element/button/), [`input`](/html/element/input/), [`command`](/html/element/command/), [`embed`](/html/element/embed/), [`object`](/html/element/object/), [`script`](/html/element/script/), [`source`](/html/element/source/), [`style`](/html/element/style/), [`menu`](/html/element/menu/) | Defines the type of the element. |
| `[usemap](/html/attributes/usemap)` | [`img`](/html/element/img/), [`input`](/html/element/input/), [`object`](/html/element/object/) |  |
| `[value](/html/attributes/value)` | [`button`](/html/element/button/), [`data`](/html/element/data/), [`input`](/html/element/input/), [`li`](/html/element/li/), [`meter`](/html/element/meter/), [`option`](/html/element/option/), [`progress`](/html/element/progress/), [`param`](/html/element/param/) | Defines a default value which will be displayed in the element on page load. |
| `[width](/html/attributes/width)` | [`canvas`](/html/element/canvas/), [`embed`](/html/element/embed/), [`iframe`](/html/element/iframe/), [`img`](/html/element/img/), [`input`](/html/element/input/), [`object`](/html/element/object/), [`video`](/html/element/video/) | 

For the elements listed here, this establishes the element's width.

**Note:** For all other instances, such as [`div`](/html/element/div/), this is a legacy attribute, in which case the CSS {{ Cssxref("width")  }} property should be used instead.



 |
| `[wrap](/html/attributes/wrap)` | [`textarea`](/html/element/textarea/) | Indicates whether the text should be wrapped. |

## Content versus IDL attributes

In HTML, most attributes have two faces: the **content attribute** and the **IDL (Interface Definition Language) attribute**.

The content attribute is the attribute as you set it from the content (the HTML code) and you can set it or get it via {{ domxref("element.setAttribute()") }} or {{ domxref("element.getAttribute()") }}. The content attribute is always a string even when the expected value should be an integer. For example, to set an [`input`](/html/element/input/) element's `maxlength` to 42 using the content attribute, you have to call `setAttribute("maxlength", "42")` on that element.

The IDL attribute is also known as a JavaScript property. These are the attributes you can read or set using JavaScript properties like `element.foo`. The IDL attribute is always going to use (but might transform) the underlying content attribute to return a value when you get it and is going to save something in the content attribute when you set it. In other words, the IDL attributes, in essence, reflect the content attributes.

Most of the time, IDL attributes will return their values as they are really used. For example, the default `type` for [`input`](/html/element/input/) elements is "text", so if you set `input.type="foobar"`, the `<input>` element will be of type text (in the appearance and the behavior) but the "type" content attribute's value will be "foobar". However, the `type` IDL attribute will return the string "text".

IDL attributes are not always strings; for example, `input.maxlength` is a number (a signed long). When using IDL attributes, you read or set values of the desired type, so `input.maxlength` is always going to return a number and when you set `input.maxlength`, it wants a number. If you pass another type, it is automatically converted to a number as specified by the standard JavaScript rules for type conversion.

IDL attributes can [reflect other types](https://www.whatwg.org/specs/web-apps/current-work/multipage/urls.html#reflecting-content-attributes-in-idl-attributes) such as unsigned long, URLs, booleans, etc. Unfortunately, there are no clear rules and the way IDL attributes behave in conjunction with their corresponding content attributes depends on the attribute. Most of the time, it will follow [the rules laid out in the specification](https://www.whatwg.org/specs/web-apps/current-work/multipage/urls.html#reflecting-content-attributes-in-idl-attributes), but sometimes it doesn't. HTML specifications try to make this as developer-friendly as possible, but for various reasons (mostly historical), some attributes behave oddly (`select.size`, for example) and you should read the specifications to understand how exactly they behave.

## Boolean Attributes

Some content attributes (e.g. `required`, `readonly`, `disabled`) are called [boolean attributes](https://www.w3.org/TR/html52/infrastructure.html#sec-boolean-attributes). If a boolean attribute is present, its value is **true**, and if it’s absent, its value is **false**.

HTML5 defines restrictions on the allowed values of boolean attributes: If the attribute is present, its value must either be the empty string (equivalently, the attribute may have an unassigned value), or a value that is an ASCII case-insensitive match for the attribute’s canonical name, with no leading or trailing whitespace. The following examples are valid ways to mark up a boolean attribute:

```
<div itemscope> This is valid HTML but invalid XML. </div>
<div itemscope=itemscope> This is also valid HTML but invalid XML. </div>
<div itemscope=""> This is valid HTML and also valid XML. </div>
<div itemscope="itemscope"> This is also valid HTML and XML, but perhaps a bit verbose. </div>
```

To be clear, the values "`true`" and "`false`" are not allowed on boolean attributes. To represent a false value, the attribute has to be omitted altogether. This restriction clears up some common misunderstandings: With `checked="false"` for example, the element’s `checked` attribute would be interpreted as **true** because the attribute is present.

## See also

-   [HTML elements](/html/element)