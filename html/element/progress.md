---
title: '<progress>: The Progress Indicator element'
tags:
  - Element
  - HTML
  - HTML forms
  - HTML5
  - Reference
  - Web
permalink: html/element/progress
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress'
browserCompact: html.elements.progress
---
{{ HTMLRef }}

The **HTML `<progress>` element** displays an indicator showing the completion progress of a task, typically displayed as a progress bar.

{{ EmbedInteractiveExample("pages/tabbed/progress.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), labelable content, palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content), but there must be no `<progress>` element among its descendants. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [`progressbar`](https://w3c.github.io/aria/#progressbar) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLProgressElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("max")  }}
: This attribute describes how much work the task indicated by the `progress` element requires. The `max` attribute, if present, must have a value greater than `0` and be a valid floating point number. The default value is `1`.

{{ htmlattrdef("value")  }}
: This attribute specifies how much of the task that has been completed. It must be a valid floating point number between `0` and `max`, or between `0` and `1` if `max` is omitted. If there is no `value` attribute, the progress bar is indeterminate; this indicates that an activity is ongoing with no indication of how long it is expected to take.

**Note:** Unlike the [`meter`](/html/element/meter/) element, the minimum value is always 0, and the `min` attribute is not allowed for the `<progress>` element.

**Note:** The {{ cssxref(":indeterminate") }} pseudo-class can be used to match against indeterminate progress bars. To change the progress bar to indeterminate after giving it a value you must remove the value attribute with {{ domxref("Element.removeAttribute", "element.removeAttribute('value')") }}.

## Examples

```html
<progress value="70" max="100">70 %</progress>

```

### Result

{{ EmbedLiveSample("Examples", 200, 50)  }}

On Windows 7, the resulting progress looks like this:

![progress-firefox.JPG](/@api/deki/files/6031/=progress-firefox.JPG)

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<progress>' in that specification](https://html.spec.whatwg.org/multipage/forms.html#the-progress-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<progress>' in that specification](https://www.w3.org/TR/html52/sec-forms.html#the-progress-element) | {{ Spec2('HTML5 W3C') }} | Initial definition |

## Browser compatibility

{{ Compat("html.elements.progress") }}

## See also

-   [`meter`](/html/element/meter/)
-   {{ cssxref(":indeterminate")  }}
-   {{ cssxref("-moz-orient")  }}
-   {{ cssxref("::-moz-progress-bar")  }}
-   {{ cssxref("::-ms-fill")  }}
-   {{ cssxref("::-webkit-progress-bar")  }}
-   {{ cssxref("::-webkit-progress-value")  }}
-   {{ cssxref("::-webkit-progress-inner-element")  }}