---
title: <time>
tags:
  - Element
  - HTML
  - HTML text-level semantics
  - HTML5
  - 'HTML:Flow content'
  - 'HTML:Palpable Content'
  - 'HTML:Phrasing content'
  - Reference
  - Web
permalink: html/element/time
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/time'
browserCompact: html.elements.time
---
{{ HTMLRef }}

The HTML **`<time>` element** represents a specific period in time. It may include the `datetime` attribute to translate dates into machine-readable format, allowing for better search engine results or custom features such as reminders.

It may represent one of the following:

-   A time on a 24-hour clock.
-   A precise date in the [`Gregorian calendar`](https://en.wikipedia.org/wiki/Gregorian_calendar) (with optional time and timezone information).
-   [A valid time duration](https://www.w3.org/TR/2014/REC-html5-20141028/infrastructure.html#valid-duration-string).

{{ EmbedInteractiveExample("pages/tabbed/time.html", "tabbed-shorter") }}

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), [phrasing content](/html/content_categories#phrasing_content), palpable content. |
| Permitted content | [Phrasing content](/html/content_categories#phrasing_content). |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts [phrasing content](/html/content_categories#phrasing_content). |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | Any |
| DOM interface | {{ domxref("HTMLTimeElement") }} |

## Attributes

Like all other HTML elements, this element supports the [global attributes](/html/global_attributes).

{{ htmlattrdef("datetime") }}
: This attribute indicates the time and/or date of the element and must be in one of the formats described below.

## Usage notes

This element is for presenting dates and times in a machine readable format. For example, this can help a user agent offer to add an event to a user's calendar.

This element should not be used for dates prior to the introduction of the Gregorian calendar (due to complications in calculating those dates).

The datetime value (the machine-readable value of the datetime) is the value of the element’s `datetime` attribute, which must be in the proper format (see below). If the element does not have a `datetime` attribute, **it must not have any element descendants**, and the datetime value is the element’s child text content.

### Valid datetime Values

a valid year string
: `2011`

a valid month string
: `2011-11`

a valid date string
: `2011-11-18`

a valid yearless date string
: `11-18`

a valid week string
: `2011-W47`

a valid time string
: `14:54`

: `14:54:39`

: `14:54:39.929`

a valid local date and time string
: `2011-11-18T14:54:39.929`

: `2011-11-18 14:54:39.929`

a valid global date and time string
: `2011-11-18T14:54:39.929Z`

: `2011-11-18T14:54:39.929-0400`

: `2011-11-18T14:54:39.929-04:00`

: `2011-11-18 14:54:39.929Z`

: `2011-11-18 14:54:39.929-0400`

: `2011-11-18 14:54:39.929-04:00`

a valid duration string
: `PT4H18M3S`

## Examples

### Simple example

#### HTML

```html
<p>The concert starts at <time datetime="2018-07-07T20:00:00">20:00</time>.</p>

```

#### Output

{{ EmbedLiveSample('Simple_example', 250, 60) }}

### `datetime` example

#### HTML

```html
<p>The concert took place on <time
  datetime="2001-05-15T19:00">May 15</time>.</p>

```

#### Output

{{ EmbedLiveSample('Datetime_example', 250, 60) }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<time>' in that specification](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-time-element) | {{ Spec2('HTML WHATWG') }} | No change from [**HTML 5.1**](https://www.w3.org/TR/html51/) |
| [**HTML 5.1** The definition of '<time>' in that specification](https://www.w3.org/TR/html51/textlevel-semantics.html#the-time-element) | {{ Spec2('HTML5.1') }} | No change from [**HTML 5**](https://www.w3.org/TR/html52/) |
| [**HTML 5** The definition of '<time>' in that specification](https://www.w3.org/TR/html52/text-level-semantics.html#the-time-element) | {{ Spec2('HTML5 W3C') }} | Initial definition. |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.time") }}

## See also

-   The [`data`](/html/element/data/) element, allowing to signal other kind of values.