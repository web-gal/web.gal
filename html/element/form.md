---
title: <form>
tags:
  - Element
  - Form Element
  - Forms
  - HTML
  - HTML Form Element
  - HTML forms
  - Reference
  - Web
permalink: html/element/form
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form'
browserCompact: html.elements.form
---
{{ HTMLRef }}

The **HTML `<form>` element** represents a document section containing interactive controls for submitting information.

{{ EmbedInteractiveExample("pages/tabbed/form.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

It is possible to use the {{ cssxref(':valid') }} and {{ cssxref(':invalid') }} CSS [pseudo-classes](/css/pseudo-classes) to style a `<form>` element based on whether or not the {{ domxref("HTMLFormElement.elements", "elements") }} inside the form are valid.

| Property | Value |
| --- | --- |
| [Content categories](/guide/html/content_categories) | [Flow content](/guide/html/content_categories#flow_content), [palpable content](/guide/html/content_categories#palpable_content) |
| Permitted content | [Flow content](/guide/html/content_categories#flow_content), but not containing `<form>` elements |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [flow content](/guide/html/content_categories#flow_content) |
| Implicit ARIA role | `[form](/accessibility/aria/roles/form_role)` if the form has an [accessible name](https://www.w3.org/TR/accname-1.1/#dfn-accessible-name), otherwise [no corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | `[search](/accessibility/aria/roles/search_role)`, [`none`](https://w3c.github.io/aria/#none) or [`presentation`](https://w3c.github.io/aria/#presentation) |
| DOM interface | {{ domxref("HTMLFormElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("accept") }} {{ obsolete_inline }}
: Comma-separated [content types](/svg/content_type) the server accepts.

**This attribute was removed in HTML5 and should not be used.** Instead, use the {{ htmlattrxref("accept", "input") }} attribute on `<input type=file>` elements.

{{ htmlattrdef("accept-charset") }}
: Space-separated [character encodings](/guide/localizations_and_character_encodings) the server accepts. The browser uses them in the order in which they are listed. The default value means [the same encoding as the page](/http/headers/content-encoding).  
(In previous versions of HTML, character encodings could also be delimited by commas.)

{{ htmlattrdef("autocapitalize") }} {{ non-standard_inline }}
: A nonstandard attribute used by iOS Safari that controls how textual form elements should be automatically capitalized. `autocapitalize` attributes on a form elements override it on `<form>`. Possible values:

-   `none`: No automatic capitalization.
-   `sentences` (default): Capitalize the first letter of each sentence.
-   `words`: Capitalize the first letter of each word.
-   `characters`: Capitalize all characters — that is, uppercase.

{{ htmlattrdef("autocomplete") }}
: Indicates whether input elements can by default have their values automatically completed by the browser. `autocomplete` attributes on form elements override it on `<form>`. Possible values:

-   `off`: The browser may not automatically complete entries. (Browsers tend to ignore this for suspected login forms; see [The autocomplete attribute and login fields](/security/securing_your_site/turning_off_form_autocompletion#the_autocomplete_attribute_and_login_fields).)
-   `on`: The browser may automatically complete entries.

{{ htmlattrdef("name") }}
: The name of the form. Deprecated as of HTML 4 (use `id` instead). It must be unique among the forms in a document and not an empty string as of HTML5.

{{ htmlattrdef("rel") }}
: Creates a hyperlink or annotation depending on the value, see the [{{ htmlattrdef("rel") }}](/docs/Web/HTML/Attributes/rel) attribute for details.

### Attributes for form submission

The following attributes control behavior during form submission.

{{ htmlattrdef("action") }}
: The URL that processes the form submission. This value can be overridden by a {{ htmlattrxref("formaction", "button") }} attribute on a [`button`](/html/element/button/), `[<input type="submit">](/html/element/input/submit)`, or `[<input type="image">](/html/element/input/image)` element.

{{ htmlattrdef("enctype") }}
: If the value of the `method` attribute is `post`, `enctype` is the [MIME type](https://en.wikipedia.org/wiki/Mime_type) of the form submission. Possible values:

-   `application/x-www-form-urlencoded`: The default value.
-   `multipart/form-data`: Use this if the form contains [`input`](/html/element/input/) elements with `type=file`.
-   `text/plain`: Introduced by HTML5 for debugging purposes.

This value can be overridden by {{ htmlattrxref("formenctype", "button") }} attributes on [`button`](/html/element/button/), `[<input type="submit">](/html/element/input/submit)`, or `[<input type="image">](/html/element/input/image)` elements.

{{ htmlattrdef("method") }}
: The [HTTP](/http) method to submit the form with. Possible (case insensitive) values:

-   `post`: The [POST method](https://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.5); form data sent as the [request body](/api/body).
-   `get`: The [GET method](https://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.3); form data appended to the `action` URL with a `?` separator. Use this method when the form [has no side-effects](/en-US/docs/Glossary/Idempotent).
-   `dialog`: When the form is inside a [`dialog`](/html/element/dialog/), closes the dialog on submission.

This value is overridden by {{ htmlattrxref("formmethod", "button") }} attributes on [`button`](/html/element/button/), `[<input type="submit">](/html/element/input/submit)`, or `[<input type="image">](/html/element/input/image)` elements.

{{ htmlattrdef("novalidate") }}
: This Boolean attribute indicates that the form shouldn't be validated when submitted. If this attribute is not set (and therefore the form _**is**_ validated), it can be overridden by a {{ htmlattrxref("formnovalidate", "button") }} attribute on a [`button`](/html/element/button/), `[<input type="submit">](/html/element/input/submit)`, or `[<input type="image">](/html/element/input/image)` element belonging to the form.

{{ htmlattrdef("target") }}
: Indicates where to display the response after submitting the form. In HTML 4, this is the name/keyword for a frame. In HTML5, it is a name/keyword for a _browsing context_ (for example, tab, window, or iframe). The following keywords have special meanings:

-   `_self` (default): Load into the same browsing context as the current one.
-   `_blank`: Load into a new unnamed browsing context.
-   `_parent`: Load into the parent browsing context of the current one. If no parent, behaves the same as `_self`.
-   `_top`: Load into the top-level browsing context (i.e., the browsing context that is an ancestor of the current one and has no parent). If no parent, behaves the same as `_self`.

This value can be overridden by a {{ htmlattrxref("formtarget", "button") }} attribute on a [`button`](/html/element/button/), `[<input type="submit">](/html/element/input/submit)`, or `[<input type="image">](/html/element/input/image)` element.

## Examples

### HTML

```html
<!-- Form which will send a GET request to the current URL -->
<form>
  <label>Name:
    <input name="submitted-name" autocomplete="name">
  </label>
  <button>Save</button>
</form>

<!-- Form which will send a POST request to the current URL -->
<form method="post">
  <label>Name:
    <input name="submitted-name" autocomplete="name">
  </label>
  <button>Save</button>
</form>

<!-- Form with fieldset, legend, and label -->
<form method="post">
  <fieldset>
    <legend>Title</legend>
    <label><input type="radio" name="radio"> Select me</label>
  </fieldset>
</form>
```

{{ EmbedLiveSample('Examples', '100%', 110)  }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<form>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-form-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<form>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-form-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<form>' in that specification](https://www.w3.org/TR/html401/interact/forms.html#h-17.3) | {{ Spec2('HTML4.01') }} | Initial definition |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.form") }}

## See also

-   [HTML forms guide](/guide/html/forms)
-   Other elements that are used when creating forms: [`button`](/html/element/button/), [`datalist`](/html/element/datalist/), [`fieldset`](/html/element/fieldset/), [`input`](/html/element/input/),[`keygen`](/html/element/keygen/), [`label`](/html/element/label/), [`legend`](/html/element/legend/), [`meter`](/html/element/meter/), [`optgroup`](/html/element/optgroup/), [`option`](/html/element/option/), [`output`](/html/element/output/), [`progress`](/html/element/progress/), [`select`](/html/element/select/), [`textarea`](/html/element/textarea/).
-   Getting a list of the elements in the form: {{ domxref("HTMLFormElement.elements") }}
-   [ARIA: Form role](/accessibility/aria/roles/form_role)
-   [ARIA: Search role](/accessibility/aria/roles/search_role)