---
title: manifest
tags:
  - Cache
  - application cache
permalink: html/element/html/manifest
mdn: 'https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html/manifest'
deprecated: true
nonStandard: true
browserCompact: html.elements.html.manifest
---
The `**manifest**` attribute of `<html>` element specifies a URL of a application cache manifest that is downloaded in the early stages of page load.

**Note:** manifest-based caching mechanism has been deprecated. Use service workers instead.

The manifest attribute has only effect during early stages of page load, thus changing it via regular DOM interfaces has no effect, {{ domxref("Window.applicationCache") }} interface instead.

## Browser compatibility

{{ Compat("html.elements.html.manifest") }}

## See also

-   {{ domxref("Window.applicationCache") }}
-   [Using the application cache](/html/using_the_application_cache)
-   [Service Worker API](/api/service_worker_api)