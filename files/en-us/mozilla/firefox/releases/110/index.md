---
title: Firefox 110 for developers
slug: Mozilla/Firefox/Releases/110
tags:
  - "110"
  - Firefox
  - Mozilla
  - Release
---

{{FirefoxSidebar}}

This article provides information about the changes in Firefox 110 that will affect developers. Firefox 110 is the current [Beta version of Firefox](https://www.mozilla.org/en-US/firefox/channel/desktop/#beta) and will ship on [February 14, 2023](https://wiki.mozilla.org/RapidRelease/Calendar#Future_branch_dates).

## Changes for web developers

### Developer Tools

### HTML

#### Removals

### CSS

- Container queries and container query length units are now supported by default.
  For more information on these queries and the related units of length, see the [CSS Container Queries](/en-US/docs/Web/CSS/CSS_Container_Queries#container_query_length_units) documentation ({{bug(1809720)}}).
- The [color-gamut media query](/en-US/docs/Web/CSS/@media/color-gamut) is now supported ({{bug(1422237)}}).

#### Removals

### JavaScript

- Serialization of [native Error types](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error#error_types) now includes the [`stack`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error/Stack) property in workers when using [`Worker.postMessage()`](/en-US/docs/Web/API/Worker/postMessage) and [`structuredClone()`](/en-US/docs/Web/API/structuredClone).
  With this addition, cloning native error stacks now works for all methods that use the [structured clone algorithm](/en-US/docs/Web/API/Web_Workers_API/Structured_clone_algorithm), in both the main thread and workers.
  (See {{bug(1774866)}} for more details.)

#### Removals

### SVG

#### Removals

### HTTP

#### Removals

### Security

#### Removals

### APIs

- The `midi` permission of the [Permission API](/en-US/docs/Web/API/Permissions_API) is now supported.
  This allows the permission status for using the [Web MIDI API](/en-US/docs/Web/API/Web_MIDI_API) to be queried using [`navigator.permissions.query()`](/en-US/docs/Web/API/Permissions/query) ({{bug(1772166)}}).

- {{domxref("ReadableStream")}} now supports [asynchronous iteration over the chunks in a stream](/en-US/docs/Web/API/ReadableStream#async_iteration) using the `for await...of` syntax ({{bug(1734244)}}).

#### DOM

#### Media, WebRTC, and Web Audio

#### Removals

### WebAssembly

#### Removals

### WebDriver conformance (WebDriver BiDi, Marionette)

#### WebDriver BiDi

- Added support for the `network.beforeRequestSent` ({{bug(1790368)}}), the `network.responseStarted` ({{bug(1790370)}}), and the `network.responseCompleted` ({{bug(1790372)}}) events.

- Added support for the `browsingContext.captureScreenshot` command to capture full page screenshots ({{bug(1800086)}}).

- Added support for serialization and deserialization of generic platform objects ({{bug(1792524)}}), and for `NodeList` and `HTMLCollection` platform objects ({{bug(1802284)}}).

- Added a `timestamp` field to the `browsingContext.domContentLoaded` and `browsingContext.load` events ({{bug(1790378)}}).

- Added a `type` field to the response for `script.evaluate` and `script.callFunction` to indicate either `success` or `exception` results ({{bug(1803599)}}).

#### Marionette

- The cache for known nodes (element and shadow root references) has been moved from the parent to the web content process following recent WebDriver classic changes ({{bug(1692468)}}).

- Improved the JSON serialization and deserialization algorithms to be compliant with the WebDriver classic specification ({{bug(1794078)}}).

## Changes for add-on developers

- The `defaultZoomFactor` property of {{WebExtAPIRef("tabs.ZoomSettings")}} now returns the value of the default zoom factor setting ({{bug(1772166)}})

### Removals

### Other

## Older versions

{{Firefox_for_developers(109)}}
