---
title: '<bgsound>: The Background Sound element (obsolete)'
tags:
  - Audio
  - Background Sound
  - Element
  - HTML
  - Internet Explorer
  - Non-standard
  - Obsolete
  - Reference
  - Web
permalink: html/element/bgsound
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/bgsound'
obsolete: true
nonStandard: true
browserCompact: html.elements.bgsound
---
The Internet Explorer only **HTML Background Sound element** (**`<bgsound>`**) sets up a sound file to play in the background while the page is used; use [`audio`](/html/element/audio/) instead.

**Do not use this!** In order to embed audio in a Web page, you should be using the [`audio`](/html/element/audio/) element.

## Attributes

{{ htmlattrdef("balance") }}
: This attribute defines a number between -10,000 and +10,000 that determines how the volume will be divided between the speakers.

{{ htmlattrdef("loop") }}
: This attribute indicates the number of times a sound is to be played and either has a numeric value or the keyword infinite.

{{ htmlattrdef("src") }}
: This attribute specifies the URL of the sound file to be played, which must be one of the following types: .wav, .au, or .mid.

{{ htmlattrdef("volume") }}
: This attribute defines a number between -10,000 and 0 that determines the loudness of a page's background sound.

## Example

```html
<bgsound src="sound1.mid">

<bgsound src="sound2.au" loop="infinite">

```

## Usage notes

Historically, the [`embed`](/html/element/embed/) element could be used with audio player plug-ins to play audio in the background in most browsers. However, even this is no longer appropriate, and you should use `<audio>` instead, since it's more capable, more compatible, and doesn't require plug-ins.

You can write `<bgsound>` as a self-closing tag (`<bgsound />`); however, since this element is non-standard, doing so will still not validate.

## Browser compatibility

{{ Compat("html.elements.bgsound") }}

## See also

-   The [`audio`](/html/element/audio/), which is the standard element to embed audio in a document.

{{ HTMLRef }}