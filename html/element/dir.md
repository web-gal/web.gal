---
title: '<dir>: The Directory element (obsolete)'
tags:
  - Directory
  - Element
  - HTML
  - HTML Lists
  - Obsolete
  - Reference
  - Web
  - dir
  - lists
permalink: html/element/dir
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dir'
obsolete: true
browserCompact: html.elements.dir
---
{{ HTMLRef }}

The obsolete **HTML Directory element** (**`<dir>`**) is used as a container for a directory of files and/or folders, potentially with styles and icons applied by the [user agent](/glossary/user_agent/). Do not use this obsolete element; instead, you should use the [`ul`](/html/element/ul/) element for lists, including lists of files.

**Usage note:** Do not use this element. Though present in early HTML specifications, it has been deprecated in HTML 4, and has since been removed entirely. **No major browsers support this element.**

## DOM interface

This element implements the {{ domxref("HTMLDirectoryElement") }} interface.

## Attributes

Like all other HTML elements, this element supports the [global attributes](/en-US/docs/HTML/Global_attributes "HTML/Global attributes").

{{ htmlattrdef("compact") }}
: This Boolean attribute hints that the list should be rendered in a compact style. The interpretation of this attribute depends on the user agent and it doesn't work in all browsers.

**Usage note:** Do not use this attribute, as it has been deprecated: the [`dir`](/html/element/dir/) element should be styled using [CSS](/en-US/docs/CSS "CSS"). To give a similar effect as that achieved with the `compact` attribute, the [CSS](/en-US/docs/CSS "CSS") property {{ cssxref("line-height") }} can be used with a value of `80%`.

## Browser compatibility

{{ Compat("html.elements.dir") }}

## See also

-   Other list-related HTML Elements: [`ol`](/html/element/ol/), [`ul`](/html/element/ul/), [`li`](/html/element/li/), and [`menu`](/html/element/menu/);
-   CSS properties that may be specially useful to style the `<dir>` element:
    -   The {{ cssxref('list-style') }} property, useful to choose the way the ordinal is displayed.
    -   [CSS counters](/css/css_lists_and_counters/using_css_counters), useful to handle complex nested lists.
    -   The {{ Cssxref('line-height') }} property, useful to simulate the deprecated {{ htmlattrxref("compact", "dir") }} attribute.
    -   The {{ cssxref('margin') }} property, useful to control the indent of the list.