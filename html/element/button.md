---
title: '<button>: The Button element'
tags:
  - Element
  - Forms
  - HTML
  - HTML forms
  - Reference
  - Web
permalink: html/element/button
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button'
browserCompact: html.elements.button
---
{{ HTMLRef }}

The **HTML `<button>` element** represents a clickable button, used to submit [forms](/en-US/docs/Learn/HTML/Forms) or anywhere in a document for accessible, standard button functionality. By default, HTML buttons are presented in a style resembling the platform the [user agent](/glossary/user_agent/) runs on, but you can change buttons’ appearance with [CSS](/css).

{{ EmbedInteractiveExample("pages/tabbed/button.html", "tabbed-shorter") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), [Interactive content](/html/content_categories#interactive_content), [listed](/html/content_categories#form_listed), [labelable](/html/content_categories#form_labelable), and [submittable](/html/content_categories#form_submittable) [form-associated](/docs/Web/HTML/Content_categories#Form-associated_content) element, palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content) but there must be no [Interactive content](/html/content_categories#interactive_content) |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | `[button](/accessibility/aria/roles/button_role)` |
| Permitted ARIA roles | [`checkbox`](https://w3c.github.io/aria/#checkbox), [`link`](https://w3c.github.io/aria/#link), [`menuitem`](https://w3c.github.io/aria/#menuitem), [`menuitemcheckbox`](https://w3c.github.io/aria/#menuitemcheckbox), [`menuitemradio`](https://w3c.github.io/aria/#menuitemradio), [`option`](https://w3c.github.io/aria/#option), [`radio`](https://w3c.github.io/aria/#radio), [`switch`](https://w3c.github.io/aria/#switch), [`tab`](https://w3c.github.io/aria/#tab) |
| DOM interface | {{ domxref("HTMLButtonElement") }} |

## Attributes

This element's attributes include the [global attributes](/html/global_attributes).

{{ htmlattrdef("autofocus") }} {{ HTMLVersionInline(5) }}
: This Boolean attribute specifies that the button should have input [focus](/api/htmlelement/focus) when the page loads. **Only one element in a document can have this attribute.**

{{ htmlattrdef("autocomplete") }} {{ non-standard_inline }}
: This attribute on a [`button`](/html/element/button/) is nonstandard and Firefox-specific. Unlike other browsers, [Firefox persists the dynamic disabled state](https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing) of a [`button`](/html/element/button/) across page loads. Setting `autocomplete="off"` on the button disables this feature; see [bug 654072](https://bugzilla.mozilla.org/show_bug.cgi?id=654072).

{{ htmlattrdef("disabled") }}
: This Boolean attribute prevents the user from interacting with the button: it cannot be pressed or focused.

Firefox, unlike other browsers, [persists the dynamic disabled state](https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing) of a [`button`](/html/element/button/) across page loads. Use the {{ htmlattrxref("autocomplete","button") }} attribute to control this feature.

{{ htmlattrdef("form") }} {{ HTMLVersionInline(5) }}
: The [`form`](/html/element/form/) element to associate the button with (its _form owner_). The value of this attribute must be the `id` of a `<form>` in the same document. (If this attribute is not set, the `<button>` is associated with its ancestor `<form>` element, if any.)

: This attribute lets you associate `<button>` elements to `<form>`s anywhere in the document, not just inside a `<form>`. It can also override an ancestor `<form>` element.

{{ htmlattrdef("formaction") }} {{ HTMLVersionInline(5) }}
: The URL that processes the information submitted by the button. Overrides the {{ htmlattrxref("action","form") }} attribute of the button's form owner. Does nothing if there is no form owner.

{{ htmlattrdef("formenctype") }} {{ HTMLVersionInline(5) }}
: If the button is a submit button (it's inside/associated with a `<form>` and doesn't have `type="button"`), specifies how to encode the form data that is submitted. Possible values:

-   `application/x-www-form-urlencoded`: The default if the attribute is not used.
-   `multipart/form-data`: Use to submit [`input`](/html/element/input/) elements with their {{ htmlattrxref("type","input") }} attributes set to `file`.
-   `text/plain`: Specified as a debugging aid; shouldn’t be used for real form submission.

If this attribute is specified, it overrides the {{ htmlattrxref("enctype","form") }} attribute of the button's form owner.

{{ htmlattrdef("formmethod") }} {{ HTMLVersionInline(5) }}
: If the button is a submit button (it's inside/associated with a `<form>` and doesn't have `type="button"`), this attribute specifies the [HTTP method](/http/methods) used to submit the form. Possible values:

-   `post`: The data from the form are included in the body of the HTTP request when sent to the server. Use when the form contains information that shouldn’t be public, like login credentials.
-   `get`: The form data are appended to the form's `action` URL, with a `?` as a separator, and the resulting URL is sent to the server. Use this method when the form [has no side effects](/en-US/docs/Glossary/Idempotent), like search forms.

If specified, this attribute overrides the {{ htmlattrxref("method","form") }} attribute of the button's form owner.

{{ htmlattrdef("formnovalidate") }} {{ HTMLVersionInline(5) }}
: If the button is a submit button, this Boolean attribute specifies that the form is not to be [validated](/en-US/docs/Learn/HTML/Forms/Form_validation) when it is submitted. If this attribute is specified, it overrides the {{ htmlattrxref("novalidate","form") }} attribute of the button's form owner.

: This attribute is also available on `[<input type="image">](/html/element/input/image)` and `[<input type="submit">](/html/element/input/submit)` elements.

{{ htmlattrdef("formtarget") }} {{ HTMLVersionInline(5) }}
: If the button is a submit button, this attribute is a author-defined name or standardized, underscore-prefixed keyword indicating where to display the response from submitting the form. This is the `name` of, or keyword for, a _browsing context_ (a tab, window, or [`iframe`](/html/element/iframe/)). If this attribute is specified, it overrides the {{ htmlattrxref("target", "form") }} attribute of the button's form owner. The following keywords have special meanings:

-   `_self`: Load the response into the same browsing context as the current one. This is the default if the attribute is not specified.
-   `_blank`: Load the response into a new unnamed browsing context — usually a new tab or window, depending on the user’s browser settings.
-   `_parent`: Load the response into the parent browsing context of the current one. If there is no parent, this option behaves the same way as `_self`.
-   `_top`: Load the response into the top-level browsing context (that is, the browsing context that is an ancestor of the current one, and has no parent). If there is no parent, this option behaves the same way as `_self`.

{{ htmlattrdef("name") }}
: The name of the button, submitted as a pair with the button’s `value` as part of the form data.

{{ htmlattrdef("type") }}
: The default behavior of the button. Possible values are:

-   `submit`: The button submits the form data to the server. This is the default if the attribute is not specified for buttons associated with a `<form>`, or if the attribute is an empty or invalid value.
-   `reset`: The button resets all the controls to their initial values, like [<input type="reset">](/html/element/input/reset). (This behavior tends to annoy users.)
-   `button`: The button has no default behavior, and does nothing when pressed by default. It can have client-side scripts listen to the element's events, which are triggered when the events occur.

{{ htmlattrdef("value") }}
: Defines the value associated with the button’s `name` when it’s submitted with the form data. This value is passed to the server in params when the form is submitted.

## Notes

A submit button with the attribute `formaction` set, but without an associated form does nothing. You have to set a form owner, either by wrapping it in a `<form>` or set the attribute `form` to the id of the form.

`<button>` elements are much easier to style than [`input`](/html/element/input/) elements. You can add inner HTML content (think `<i>`, `<br>`, or even `<img>`), and use {{ Cssxref("::after") }} and {{ Cssxref("::before") }} pseudo-elements for complex rendering.

If your buttons are not for submitting form data to a server, be sure to set their `type` attribute to `button`. Otherwise they will try to submit form data and to load the (nonexistent) response, possibly destroying the current state of the document.

## Example

```html
<button name="button">Press me</button>

```

{{ EmbedLiveSample('Example', 200, 64)  }}

## Accessibility concerns

### Icon buttons

Buttons that only show an icon to represent do not have an _accessible name_. Accessible names provide information for assistive technology, such as screen readers, to access when they parse the document and generate [an accessibility tree](/en-US/docs/Learn/Accessibility/What_is_accessibility#Accessibility_APIs). Assistive technology then uses the accessibility tree to navigate and manipulate page content.

To give an icon button an accessible name, put text in the `<button>` element that concisely describes the button's functionality.

#### Example

```
<button name="favorite">
  <svg aria-hidden="true" viewBox="0 0 10 10"><path d="M7 9L5 8 3 9V6L1 4h3l1-3 1 3h3L7 6z"/></svg>
  Add to favorites
</button>

```

If you want to visually hide the button's text, an accessible way to do so is to use [a combination of CSS properties](https://gomakethings.com/hidden-content-for-better-a11y/#hiding-the-link) to remove it visually from the screen, but keep it parseable by assistive technology.

However, it is worth noting that leaving the button text visually apparent can aid people who may not be familiar with the icon's meaning or understand the button's purpose. This is especially relevant for people who are not technologically sophisticated, or who may have different cultural interpretations for the icon the button uses.

-   [What is an accessible name? | The Paciello Group](https://developer.paciellogroup.com/blog/2017/04/what-is-an-accessible-name/)
-   [MDN Understanding WCAG, Guideline 4.1 explanations](/accessibility/understanding_wcag/robust#guideline_4.1_—_compatible_maximize_compatibility_with_current_and_future_user_agents_including_assistive_technologies)
-   [Understanding Success Criterion 4.1.2 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html)

### Size and Proximity

#### Size

Interactive elements such as buttons should provide an area large enough that it is easy to activate them. This helps a variety of people, including people with motor control issues and people using non-precise forms of input such as a stylus or fingers. A minimum interactive size of 44×44 [CSS pixels](https://www.w3.org/TR/WCAG21/#dfn-css-pixels) is recommended.

-   [Understanding Success Criterion 2.5.5: Target Size | W3C Understanding WCAG 2.1](https://www.w3.org/WAI/WCAG21/Understanding/target-size.html)
-   [Target Size and 2.5.5 | Adrian Roselli](http://adrianroselli.com/2019/06/target-size-and-2-5-5.html)
-   [Quick test: Large touch targets - The A11Y Project](https://a11yproject.com/posts/large-touch-targets/)

#### Proximity

Large amounts of interactive content — including buttons — placed in close visual proximity to each other should have space separating them. This spacing is beneficial for people who are experiencing motor control issues, who may accidentally activate the wrong interactive content.

Spacing may be created using CSS properties such as {{ cssxref("margin") }}.

-   [Hand tremors and the giant-button-problem - Axess Lab](https://axesslab.com/hand-tremors/)

### Firefox

Firefox will add a small dotted border on a focused button. This border is declared through CSS in the browser stylesheet, but you can override it to add your own focused style using `[button::-moz-focus-inner { }](/css/::-moz-focus-inner)`.

If overridden, it is important to **ensure that the state change when focus is moved to the button is high enough** that people experiencing low vision conditions will be able to perceive it.

Color contrast ratio is determined by comparing the luminosity of the button text and background color values compared to the background the button is placed on. In order to meet current [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/WAI/intro/wcag), a ratio of 4.5:1 is required for text content and 3:1 for large text. (Large text is defined as 18.66px and {{ cssxref("font-weight", "bold") }} or larger, or 24px or larger.)

-   [WebAIM: Color Contrast Checker](https://webaim.org/resources/contrastchecker/)
-   [MDN Understanding WCAG, Guideline 1.4 explanations](/accessibility/understanding_wcag/perceivable#guideline_1.4_make_it_easier_for_users_to_see_and_hear_content_including_separating_foreground_from_background)
-   [Understanding Success Criterion 1.4.3 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-contrast.html)

### Clicking and focus

Whether clicking on a [`button`](/html/element/button/) causes it to (by default) become focused varies by browser and OS. The results for [`input`](/html/element/input/) of `type="button"` and `type="submit"` are the same.

Does clicking on a [`button`](/html/element/button/) give it focus?
| Desktop Browsers | Windows 8.1 | OS X 10.X |
| --- | --- | --- |
| Firefox | Yes - Firefox 30.0 | No (even with a `tabindex`) Firefox 63 |
| Chrome | Yes - Chrome 35 | Yes - Chrome 65 |
| Safari | N/A | No (even with a `tabindex`) Safari 12 ([bug 22261](https://bugs.webkit.org/show_bug.cgi?id=22261)) |
| Internet Explorer | Yes - Internet Explorer 11 | N/A |
| Presto | Yes - Opera 12 | Yes - Opera 12 |

Does tapping on a [`button`](/html/element/button/) give it focus?
| Mobile Browsers | iOS 7.1.2 | Android 4.4.4 |
| --- | --- | --- |
| Safari Mobile | No (even with a `tabindex`) | N/A |
| Chrome 35 | No (even with a `tabindex`) | Yes |

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<button>' in that specification](https://html.spec.whatwg.org/multipage/form-elements.html#the-button-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<button>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-button-element) | {{ Spec2('HTML5 W3C') }} |  |
| [**HTML 4.01 Specification** The definition of '<button>' in that specification](https://www.w3.org/TR/html401/interact/forms.html#h-17.5) | {{ Spec2('HTML4.01') }} |  |

## Browser compatibility

{{ Compat("html.elements.button") }}