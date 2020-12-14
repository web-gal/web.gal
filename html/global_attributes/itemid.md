---
title: itemid
tags:
  - Attribute
  - Global attribute
  - HTML
  - HTML Microdata
  - Microdata
  - Reference
  - itemid
permalink: html/global_attributes/itemid
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemid'
browserCompact: html.global_attributes.itemid
---
The `**itemid**` [global attribute](/html/global_attributes) provides microdata in the form of a unique, global identifier of an item. An `itemid` attribute can only be specified for an element that has both {{ htmlattrxref("itemscope") }} and {{ htmlattrxref("itemtype") }} attributes. Also, `itemid` can only be specified on elements that possess an `itemscope` attribute whose corresponding `itemtype` refers to or defines a vocabulary that supports global identifiers.

The exact meaning of an `itemtype`'s global identifier is provided by the definition of that identifier within the specified vocabulary. The vocabulary defines whether several items with the same global identifier can coexist and, if so, how items with the same identifier are handled.

**Note:** The [WHATWG](/glossary/whatwg/) definition specifies that an `itemid` must be a [URL](/glossary/url/). However, the following example correctly illustrates that a [URN](/glossary/urn/) may also be used. This inconsistency may reflect the incomplete nature of the Microdata specification.

## Example

### HTML

```html
<dl itemscope
    itemtype="http://vocab.example.net/book"
    itemid="urn:isbn:0-330-34032-8">
<dt>Title <dd itemprop="title">The Reality Dysfunction
<dt>Author <dd itemprop="author">Peter F. Hamilton
<dt>Publication date
<dd><time itemprop="pubdate" datetime="1996-01-26">26 January 1996</time> </dl>
```

### Structured data

<table class="standard-table"><tbody><tr><td colspan="1" rowspan="14">itemscope</td><td>itemtype: itemid</td><td colspan="2" rowspan="1"><div class="jyrRxf-eEDwDf jcd3Mb IZ65Hb-hUbt4d">http://vocab.example.net/book: urn:isbn:0-330-34032-8</div></td></tr><tr><td>itemprop</td><td>title</td><td>The Reality Dysfunction</td></tr><tr><td>itemprop</td><td>author</td><td><div class="jyrRxf-eEDwDf jcd3Mb">Peter F. Hamilton</div></td></tr><tr><td>itemprop</td><td>pubdate</td><td>1996-01-26</td></tr></tbody></table>

### Result

{{ EmbedLiveSample('HTML', '', '', '', 'Web/HTML/Global_attributes/itemid') }}

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'itemid' in that specification](https://html.spec.whatwg.org/multipage/microdata.html#attr-itemid) | {{ Spec2('HTML WHATWG') }} |  |

## Browser compatibility

{{ Compat("html.global_attributes.itemid") }}

## See also

-   All [global attributes](/html/global_attributes).
-   Other, microdata related, global attributes:
    -   {{ htmlattrxref("itemid") }}
    -   {{ htmlattrxref("itemprop") }}
    -   {{ htmlattrxref("itemref") }}
    -   {{ htmlattrxref("itemscope") }}
    -   {{ htmlattrxref("itemtype") }}