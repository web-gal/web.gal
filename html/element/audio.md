---
title: '<audio>: The Embed Audio element'
tags:
  - Audio
  - Element
  - HTML
  - HTML embedded content
  - HTML5
  - 'HTML:Embedded content'
  - 'HTML:Flow content'
  - 'HTML:Phrasing content'
  - Media
  - Multimedia
  - Reference
  - Web
  - sound
permalink: html/element/audio
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio'
browserCompact: html.elements.audio
---
{{ HTMLRef }}

The **HTML `<audio>` element** is used to embed sound content in documents. It may contain one or more audio sources, represented using the `src` attribute or the [`source`](/html/element/source/) element: the browser will choose the most suitable one. It can also be the destination for streamed media, using a {{ domxref("MediaStream") }}.

{{ EmbedInteractiveExample("pages/tabbed/audio.html","tabbed-standard") }}

The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone [https://github.com/mdn/interactive-examples](https://github.com/mdn/interactive-examples) and send us a pull request.

The above example shows simple usage of the `<audio>` element. In a similar manner to the [`img`](/html/element/img/) element, we include a path to the media we want to embed inside the `src` attribute; we can include other attributes to specify information such as whether we want it to autoplay and loop, whether we want to show the browser's default audio controls, etc.

The content inside the opening and closing `<audio></audio>` tags is shown as a fallback in browsers that don't support the element.

## Attributes

This element's attributes include the [global attributes](/en-US/docs/HTML/Global_attributes).

{{ htmlattrdef("autoplay") }}
: A Boolean attribute: if specified, the audio will automatically begin playback as soon as it can do so, without waiting for the entire audio file to finish downloading.

**Note**: Sites that automatically play audio (or videos with an audio track) can be an unpleasant experience for users, so should be avoided when possible. If you must offer autoplay functionality, you should make it opt-in (requiring a user to specifically enable it). However, this can be useful when creating media elements whose source will be set at a later time, under user control. See our [autoplay guide](/media/autoplay_guide) for additional information about how to properly use autoplay.

{{ htmlattrdef("controls") }}
: If this attribute is present, the browser will offer controls to allow the user to control audio playback, including volume, seeking, and pause/resume playback.

{{ htmlattrdef("crossorigin") }}
: This enumerated attribute indicates whether to use CORS to fetch the related audio file. [CORS-enabled resources](/en-US/docs/CORS_Enabled_Image) can be reused in the [`canvas`](/html/element/canvas/) element without being _tainted_. The allowed values are:

`anonymous`
: Sends a cross-origin request without a credential. In other words, it sends the `Origin:` HTTP header without a cookie, X.509 certificate, or performing HTTP Basic authentication. If the server does not give credentials to the origin site (by not setting the `Access-Control-Allow-Origin:` HTTP header), the image will be _tainted_, and its usage restricted.

`use-credentials`
: Sends a cross-origin request with a credential. In other words, it sends the `Origin:` HTTP header with a cookie, a certificate, or performing HTTP Basic authentication. If the server does not give credentials to the origin site (through `Access-Control-Allow-Credentials:` HTTP header), the image will be _tainted_ and its usage restricted.

When not present, the resource is fetched without a CORS request (i.e. without sending the `Origin:` HTTP header), preventing its non-tainted used in [`canvas`](/html/element/canvas/) elements. If invalid, it is handled as if the enumerated keyword **anonymous** was used. See [CORS settings attributes](/en-US/docs/HTML/CORS_settings_attributes) for additional information.

{{ htmlattrdef("currentTime") }}
: Reading `currentTime` returns a double-precision floating-point value indicating the current playback position, in seconds, of the audio. If the audio's metadata isn't available yet—thereby preventing you from knowing the media's start time or duration—`currentTime` instead indicates, and can be used to change, the time at which playback will begin. Otherwise, setting `currentTime` sets the current playback position to the given time and seeks the media to that position if the media is currently loaded.

If the audio is being streamed, it's possible that the [user agent](/glossary/user_agent/) may not be able to obtain some parts of the resource if that data has expired from the media buffer. Other audio may have a media timeline that doesn't start at 0 seconds, so setting `currentTime` to a time before that would fail. For example, if the audio's media timeline starts at 12 hours, setting `currentTime` to 3600 would be an attempt to set the current playback position well before the beginning of the media, and would fail. The {{ domxref("HTMLMediaElement.getStartDate", "getStartDate()") }} method can be used to determine the beginning point of the media timeline's reference frame.

{{ htmlattrdef("disableRemotePlayback") }} {{ experimental_inline }}
: A Boolean attribute used to disable the capability of remote playback in devices that are attached using wired (HDMI, DVI, etc.) and wireless technologies (Miracast, Chromecast, DLNA, AirPlay, etc). See [this proposed specification](https://www.w3.org/TR/remote-playback/#the-disableremoteplayback-attribute) for more information.

In Safari, you can use [`x-webkit-airplay="deny"`](https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/AirPlayGuide/OptingInorOutofAirPlay/OptingInorOutofAirPlay.html) as a fallback.

{{ htmlattrdef("duration") }} {{ ReadOnlyInline }}
: A double-precision floating-point value which indicates the duration (total length) of the audio in seconds, on the media's timeline. If no media is present on the element, or the media is not valid, the returned value is `NaN`. If the media has no known end (such as for live streams of unknown duration, web radio, media incoming from [WebRTC](/api/webrtc_api), and so forth), this value is `+Infinity`.

{{ htmlattrdef("loop") }}
: A Boolean attribute: if specified, the audio player will automatically seek back to the start upon reaching the end of the audio.

{{ htmlattrdef("muted") }}
: A Boolean attribute that indicates whether the audio will be initially silenced. Its default value is `false`.

{{ htmlattrdef("preload") }}
: This enumerated attribute is intended to provide a hint to the browser about what the author thinks will lead to the best user experience. It may have one of the following values:

-   `none`: Indicates that the audio should not be preloaded.
-   `metadata`: Indicates that only audio metadata (e.g. length) is fetched.
-   `auto`: Indicates that the whole audio file can be downloaded, even if the user is not expected to use it.
-   _empty string_: A synonym of the `auto` value.

The default value is different for each browser. The spec advises it to be set to `metadata`.

**Usage notes:**

-   The `autoplay` attribute has precedence over `preload`. If `autoplay` is specified, the browser would obviously need to start downloading the audio for playback.
-   The browser is not forced by the specification to follow the value of this attribute; it is a mere hint.

{{ htmlattrdef("src") }}
: The URL of the audio to embed. This is subject to [HTTP access controls](/en-US/docs/HTTP_access_control). This is optional; you may instead use the [`source`](/html/element/source/) element within the audio block to specify the audio to embed.

## Events

| Event name | Fired when |
| --- | --- |
| {{ Event("audioprocess") }} | The input buffer of a {{ DOMxRef("ScriptProcessorNode") }} is ready to be processed. |
| {{ domxref("HTMLMediaElement.canplay_event", 'canplay') }} | The browser can play the media, but estimates that not enough data has been loaded to play the media up to its end without having to stop for further buffering of content. |
| {{ domxref("HTMLMediaElement.canplaythrough_event", 'canplaythrough') }} | The browser estimates it can play the media up to its end without stopping for content buffering. |
| {{ Event("complete") }} | The rendering of an {{ DOMxRef("OfflineAudioContext") }} is terminated. |
| {{ domxref("HTMLMediaElement.durationchange_event", 'durationchange') }} | The `duration` attribute has been updated. |
| {{ domxref("HTMLMediaElement.emptied_event", 'emptied') }} | The media has become empty; for example, this event is sent if the media has already been loaded (or partially loaded), and the [`load()`](/en-US/docs/XPCOM_Interface_Reference/NsIDOMHTMLMediaElement) method is called to reload it. |
| {{ domxref("HTMLMediaElement.ended_event", 'ended') }} | Playback has stopped because the end of the media was reached. |
| {{ domxref("HTMLMediaElement.loadeddata_event", 'loadeddata') }} | The first frame of the media has finished loading. |
| {{ domxref("HTMLMediaElement.loadedmetadata_event", 'loadedmetadata') }} | The metadata has been loaded. |
| {{ domxref("HTMLMediaElement.pause_event", 'pause') }} | Playback has been paused. |
| {{ domxref("HTMLMediaElement.play_event", 'play') }} | Playback has begun. |
| {{ domxref("HTMLMediaElement.playing_event", 'playing ') }} | Playback is ready to start after having been paused or delayed due to lack of data. |
| {{ domxref("HTMLMediaElement.ratechange_event", 'ratechange') }} | The playback rate has changed. |
| {{ domxref("HTMLMediaElement.seeked_event", 'seeked') }} | A _seek_ operation completed. |
| {{ domxref("HTMLMediaElement.seeking_event", 'seeking') }} | A _seek_ operation began. |
| {{ domxref("HTMLMediaElement.stalled_event", 'stalled') }} | The user agent is trying to fetch media data, but data is unexpectedly not forthcoming. |
| {{ domxref("HTMLMediaElement.suspend_event", 'suspend') }} | Media data loading has been suspended. |
| {{ domxref("HTMLMediaElement.timeupdate_event", 'timeupdate') }} | The time indicated by the `currentTime` attribute has been updated. |
| {{ domxref("HTMLMediaElement.volumechange_event", 'volumechange') }} | The volume has changed. |
| {{ domxref("HTMLMediaElement.waiting_event", 'waiting') }} | Playback has stopped because of a temporary lack of data |

## Usage notes

Browsers don't all support the same [file types](/media/formats/containers) and [audio codecs](/media/formats/audio_codecs); you can provide multiple sources inside nested [`source`](/html/element/source/) elements, and the browser will then use the first one it understands:

```html
<audio controls>
  <source src="myAudio.mp3" type="audio/mpeg">
  <source src="myAudio.ogg" type="audio/ogg">
  <p>Your browser doesn't support HTML5 audio. Here is
     a <a href="myAudio.mp4">link to the audio</a> instead.</p>
</audio>
```

We offer a substantive and thorough [guide to media file types](/media/formats) and the [audio codecs that can be used within them](/media/formats/audio_codecs). Also available is [a guide to the codecs supported for video](/media/formats/video_codecs).

Other usage notes:

-   If you don't specify the `controls` attribute, the audio player won't include the browser's default controls. You can, however, create your own custom controls using JavaScript and the {{ domxref("HTMLMediaElement") }} API.
-   To allow precise control over your audio content, `HTMLMediaElement`s fire many different [events](/guide/events/media_events). This also provides a way to monitor the audio's fetching process so you can watch for errors or detect when enough is available to begin to play or manipulate it.
-   You can also use the [Web Audio API](/api/web_audio_api) to directly generate and manipulate audio streams from JavaScript code rather than streaming pre-existing audio files.
-   `<audio>` elements can't have subtitles or captions associated with them in the same way that `<video>` elements can. See [WebVTT and Audio](https://www.iandevlin.com/blog/2015/12/html5/webvtt-and-audio) by Ian Devlin for some useful information and workarounds.

A good general source of information on using HTML `<audio>` is the [Video and audio content](/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content) beginner's tutorial.

### Styling with CSS

The `<audio>` element has no intrinsic visual output of its own unless the `controls` attribute is specified, in which case the browser's default controls are shown.

The default controls have a {{ cssxref("display") }} value of `inline` by default, and it is often a good idea set the value to `block` to improve control over positioning and layout, unless you want it to sit within a text block or similar.

You can style the default controls with properties that affect the block as a single unit, so for example you can give it a {{ cssxref("border") }} and {{ cssxref("border-radius") }}, {{ cssxref("padding") }}, {{ cssxref("margin") }}, etc. You can't however style the individual components inside the audio player (e.g. change the button size or icons, change the font, etc.), and the controls are different across the different browsers.

To get a consistent look and feel across browsers, you'll need to create custom controls; these can be marked up and styled in whatever way you want, and then JavaScript can be used along with the {{ domxref("HTMLMediaElement") }} API to wire up their functionality.

[Video player styling basics](/apps/fundamentals/audio_and_video_delivery/video_player_styling_basics) provides some useful styling techniques — it is written in the context of `<video>`, but much of it is equally applicable to `<audio>`.

### Detecting addition and removal of tracks

You can detect when tracks are added to and removed from an `<audio>` element using the {{ event("addtrack") }} and {{ event("removetrack") }} events. However, these events aren't sent directly to the `<audio>` element itself. Instead, they're sent to the track list object within the `<audio>` element's {{ domxref("HTMLMediaElement") }} that corresponds to the type of track that was added to the element:

{{ domxref("HTMLMediaElement.audioTracks") }}
: An {{ domxref("AudioTrackList") }} containing all of the media element's audio tracks. You can add a listener for `addtrack` to this object to be alerted when new audio tracks are added to the element.

{{ domxref("HTMLMediaElement.videoTracks") }}
: Add an `addtrack` listener to this {{ domxref("VideoTrackList") }} object to be informed when video tracks are added to the element.

{{ domxref("HTMLMediaElement.textTracks") }}
: Add an `addtrack` event listener to this {{ domxref("TextTrackList") }} to be notified when new text tracks are added to the element.

**Note:** Even though it's an `<audio>` element, it still has video and text track lists, and can in fact be used to present video, although the use interface implications can be odd.

For example, to detect when audio tracks are added to or removed from an `<audio>` element, you can use code like this:

```js
var elem = document.querySelector("audio");

elem.audioTrackList.onaddtrack = function(event) {
  trackEditor.addTrack(event.track);
};

elem.audioTrackList.onremovetrack = function(event) {
  trackEditor.removeTrack(event.track);
};

```

This code watches for audio tracks to be added to and removed from the element, and calls a hypothetical function on a track editor to register and remove the track from the editor's list of available tracks.

You can also use {{ domxref("EventTarget.addEventListener", "addEventListener()") }} to listen for the {{ event("addtrack") }} and {{ event("removetrack") }} events.

## Examples

### Basic usage

The following example shows simple usage of the `<audio>` element to play an OGG file. It will autoplay due to the `autoplay` attribute—if the page has permission to do so—and also includes fallback content.

```html
<!-- Simple audio playback -->
<audio
  src="AudioTest.ogg"
  autoplay>
  Your browser does not support the <code>audio</code> element.
</audio>

```

For details on when autoplay works, how to get permission to use autoplay, and how and when it's appropriate to use autoplay, see our [autoplay guide](/media/autoplay_guide).

### <audio> element with <source> element

This example specifies which audio track to embed using the `src` attribute on a nested `<source>` element rather than directly on the `<audio>` element. It is always useful to include the file's MIME type inside the `type` attribute, as the browser is able to instantly tell if it can play that file, and not waste time on it if not.

```html
<audio controls>
  <source src="foo.wav" type="audio/wav">
  Your browser does not support the <code>audio</code> element.
</audio>

```

### <audio> with multiple <source> elements

This example includes multiple `<source>` elements. The browser tries to load the first source element (Opus) if it is able to play it; if not it falls back to the second (Vorbis) and finally back to MP3:

```html
<audio controls>
 <source src="foo.opus" type="audio/ogg; codecs=opus"/>
 <source src="foo.ogg" type="audio/ogg; codecs=vorbis"/>
 <source src="foo.mp3" type="audio/mpeg"/>
</audio>
```

## Accessibility concerns

Audio with spoken dialog should provide both captions and transcripts that accurately describe its content. Captions, which are specified using [WebVTT](/api/webvtt_api), allow people who are experiencing hearing loss to understand an audio recording's content as the recording is being played, while transcripts allow people who need additional time to be able to review the recording's content at a pace and format that is comfortable for them.

If automatic captioning services are used, it is important to review the generated content to ensure it accurately represents the source audio.

The `<audio>` element doesn't directly support WebVTT. You will have to find a library or framework that provides the capability for you, or write the code to display captions yourself. One option is to play your audio using a [`video`](/html/element/video/) element, which does support WebVTT.

In addition to spoken dialog, subtitles and transcripts should also identify music and sound effects that communicate important information. This includes emotion and tone. For example, in the WebVTT below, note the use of square brackets to provide tone and emotional insight to the viewer; this can help establish the mood otherwise provided using music, nonverbal sounds and crucial sound effects, and so forth.

```
1
00:00:00 --> 00:00:45
[Energetic techno music]

2
00:00:46 --> 00:00:51
Welcome to the Time Keeper's podcast! In this episode we're discussing which Swisswatch is a wrist switchwatch?

16
00:00:52 --> 00:01:02
[Laughing] Sorry! I mean, which wristwatch is a Swiss wristwatch?

```

Also it's a good practice to provide some content (such as the direct download link) as a fallback for viewers who use a browser in which the `<audio>` element is not supported:

```html
<audio controls>
  <source src="myAudio.mp3" type="audio/mpeg">
  <source src="myAudio.ogg" type="audio/ogg">
  <p>
    Your browser doesn't support HTML5 audio.
    Here is a <a href="myAudio.mp4">link to download the audio</a> instead.
  </p>
</audio>


```

-   [MDN Subtitles and closed caption — Plugins](/en-US/docs/Plugins/Flash_to_HTML5/Video/Subtitles_captions)
-   [Web Video Text Tracks Format (WebVTT)](/api/webvtt_api)
-   [WebAIM: Captions, Transcripts, and Audio Descriptions](https://webaim.org/techniques/captions/)
-   [MDN Understanding WCAG, Guideline 1.2 explanations](/accessibility/understanding_wcag/perceivable#guideline_1.2_—_providing_text_alternatives_for_time-based_media)
-   [Understanding Success Criterion 1.2.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-av-only-alt.html)
-   [Understanding Success Criterion 1.2.2 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-captions.html)

## Technical summary

| Property | Value |
| --- | --- |
| [Content categories](/html/content_categories) | [Flow content](/html/content_categories#flow_content), phrasing content, embedded content. If it has a {{ htmlattrxref("controls", "audio") }} attribute: interactive content and palpable content. |
| Permitted content | If the element has a {{ htmlattrxref("src", "audio") }} attribute: zero or more [`track`](/html/element/track/) elements followed by transparent content that contains no [`audio`](/html/element/audio/) or [`video`](/html/element/video/) media elements.  
Else: zero or more [`source`](/html/element/source/) elements followed by zero or more [`track`](/html/element/track/) elements followed by transparent content that contains no [`audio`](/html/element/audio/) or [`video`](/html/element/video/) media elements. |
| Tag omission | {{ no_tag_omission }} |
| Permitted parents | Any element that accepts embedded content. |
| Implicit ARIA role | [No corresponding role](https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role) |
| Permitted ARIA roles | [`application`](https://w3c.github.io/aria/#application) |
| DOM interface | {{ domxref("HTMLAudioElement") }} |

## Specifications

| Specification | Status | Comment |
| --- | --- | --- |
| [**HTML Living Standard** The definition of '<audio>' in that specification](https://html.spec.whatwg.org/multipage/embedded-content.html#the-audio-element) | {{ Spec2('HTML WHATWG') }} |  |
| [**HTML 5** The definition of '<audio>' in that specification](https://www.w3.org/TR/html52/semantics-embedded-content.html#the-audio-element) | {{ Spec2('HTML5 W3C') }} |  |

## Browser compatibility

{{ Compat("html.elements.audio") }}

## See also

-   [Web media technologies](/media)
    -   [Media container formats (file types)](/media/formats/containers)
    -   [Guide to audio codecs used on the web](/media/formats/audio_codecs)
-   [Web Audio API](/en-US/docs/Web_Audio_API)
-   {{ domxref("HTMLAudioElement") }}
-   [`source`](/html/element/source/)
-   [`video`](/html/element/video/)
-   [Learning area: Video and audio content](/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
-   [Cross-browser audio basics](/en-US/Apps/Fundamentals/Audio_and_video_delivery/Cross-browser_audio_basics)