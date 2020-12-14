---
title: '<track>: The Embed Text Track element'
tags:
  - Accessibility
  - Cues
  - Element
  - HTML
  - HTML embedded content
  - HTML5
  - Multimedia
  - Reference
  - TextTrack
  - Web
  - a11y
  - track
permalink: html/element/track
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/track'
browserCompact: html.elements.track
---
{{ HTMLRef }}

The **HTML `<track>` element** is used as a child of the media elements, [`audio`](/html/element/audio/) and [`video`](/html/element/video/). It lets you specify timed text tracks (or time-based data), for example to automatically handle subtitles. The tracks are formatted in [WebVTT format](/api/web_video_text_tracks_format) (`.vtt` files) — Web Video Text Tracks.

{{ EmbedInteractiveExample("pages/tabbed/track.html", "tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | None |
| Permitted content | None, it is an [empty element](/glossary/empty_element/). |
| Tag omission | As it is a void element, the start tag must be present and the end tag must not be present. |
| Permitted parents | 
A media element, [`audio`](/html/element/audio/) or [`video`](/html/element/video/).

 |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | No `role` permitted |
| DOM interface | {{ domxref("HTMLTrackElement") }} |

## Attributes

This element includes the [global attributes](/html/global_attributes).

{{ htmlattrdef("default") }}
: This attribute indicates that the track should be enabled unless the user's preferences indicate that another track is more appropriate. This may only be used on one `track` element per media element.

{{ htmlattrdef("kind") }}
: How the text track is meant to be used. If omitted the default kind is `subtitles`. If the attribute contains an invalid value, it will use `metadata` (Versions of Chrome earlier than 52 treated an invalid value as `subtitles`). The following keywords are allowed:

-   `subtitles`
    -   Subtitles provide translation of content that cannot be understood by the viewer. For example dialogue or text that is not English in an English language film.
    -   Subtitles may contain additional content, usually extra background information. For example the text at the beginning of the Star Wars films, or the date, time, and location of a scene.
-   `captions`
    -   Closed captions provide a transcription and possibly a translation of audio.
    -   It may include important non-verbal information such as music cues or sound effects. It may indicate the cue's source (e.g. music, text, character).
    -   Suitable for users who are deaf or when the sound is muted.
-   `descriptions`
    -   Textual description of the video content.
    -   Suitable for users who are blind or where the video cannot be seen.
-   `chapters`
    -   Chapter titles are intended to be used when the user is navigating the media resource.
-   `metadata`
    -   Tracks used by scripts. Not visible to the user.

{{ htmlattrdef("label") }}
: A user-readable title of the text track which is used by the browser when listing available text tracks.

{{ htmlattrdef("src") }}
: Address of the track (`.vtt` file). Must be a valid URL. This attribute must be specified and its URL value must have the same origin as the document — unless the [`audio`](/html/element/audio/) or [`video`](/html/element/video/) parent element of the `track` element has a `[crossorigin](/html/cors_settings_attributes)` attribute.

{{ htmlattrdef("srclang") }}
: Language of the track text data. It must be a valid [BCP 47](https://r12a.github.io/app-subtags/) language tag. If the `kind` attribute is set to `subtitles`, then `srclang` must be defined.

## Usage notes

### Track data types

The type of data that `track` adds to the media is set in the `kind` attribute, which can take values of `subtitles`, `captions`, `descriptions`, `chapters` or `metadata`. The element points to a source file containing timed text that the browser exposes when the user requests additional data.

A `media` element cannot have more than one `track` with the same `kind`, `srclang`, and `label`.

### Detecting cue changes

{{ page("/en-US/docs/Web/API/TextTrack/cuechange_event", "On the track element") }}

## Examples

```html
<video controls poster="/images/sample.gif">
   <source src="sample.mp4" type="video/mp4">
   <source src="sample.ogv" type="video/ogv">
   <track kind="captions" src="sampleCaptions.vtt" srclang="en">
   <track kind="descriptions"
     src="sampleDescriptions.vtt" srclang="en">
   <track kind="chapters" src="sampleChapters.vtt" srclang="en">
   <track kind="subtitles" src="sampleSubtitles_de.vtt" srclang="de">
   <track kind="subtitles" src="sampleSubtitles_en.vtt" srclang="en">
   <track kind="subtitles" src="sampleSubtitles_ja.vtt" srclang="ja">
   <track kind="subtitles" src="sampleSubtitles_oz.vtt" srclang="oz">
   <track kind="metadata" src="keyStage1.vtt" srclang="en"
     label="Key Stage 1">
   <track kind="metadata" src="keyStage2.vtt" srclang="en"
     label="Key Stage 2">
   <track kind="metadata" src="keyStage3.vtt" srclang="en"
     label="Key Stage 3">
   <!-- Fallback -->
   ...
</video>

```

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of 'track element' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#the-track-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of 'track element' in that specification](https://www.w3.org/TR/html52/semantics-embedded-content.html#the-track-element) | {{ Spec2("HTML5 W3C") }} | Initial definition |

## Browser compatibility

The compatibility table in this page is generated from structured data. If you'd like to contribute to the data, please check out [https://github.com/mdn/browser-compat-data](https://github.com/mdn/browser-compat-data) and send us a pull request.

{{ Compat("html.elements.track") }}

## See also

-   [WebVTT text track format](/en-US/docs/HTML/WebVTT)
-   {{ domxref("HTMLMediaElement.textTracks") }}