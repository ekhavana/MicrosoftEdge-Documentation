
# Microsoft Edge Developer Guide
This guide provides an overview of the developer features and standards included in Microsoft Edge.

## What's new in EdgeHTML 15
Here are the changes shipped with the current release of the Microsoft Edge platform,
 as of the [Windows Creators Update(MM/YYYY)](). For changes in Windows Insider Preview builds, see
 the Microsoft Edge [Changelog](https://developer.microsoft.com/en-us/microsoft-edge/platform/changelog/).

### New features

#### CSS Custom Properties

#### Intersection Observer

#### Payment Request API

#### Service Worker

#### WebRTC

#### WebVR

### Updated features

#### Content Security Policy (Level 2)
Sites already using CSP 1 should continue to work with Microsoft Edge support for CSP 2, however it's best to switch any `frame-src` directives that load worker scripts to the new `child-src` directive to future-proof your site. (In CSP 3, `frame-src` will no longer apply to workers.) CSP 2 also adds the following:

1. New directives: `base-uri`, `child-src`, `form-action`, `frame-ancestors` and `plugin-types`. See [Edge supported CSP directives](./security/content-Security-Policy) for more.

2. Workers support: Background worker scripts are governed by their own policy, separate from the policy of the document loading them. As with host documents, you can set the CSP for a worker in the response header. Also new in CSP 2 is that  `allow-scripts` and `allow-same-origin` flags of the `sandbox` directive now affect worker thread creation.

3. Inline scripts and styles: CSP 2 allows for the execution of inline scripts and style blocks by providing nonces (single-use base-64 codes) and hashes (generated via *sha256*, *sha384* or *sha512* algorithms) as a whitelisting mechanism.

4. CSP violation reporting: A new event, SecurityPolicyViolationEvent is now fired upon CSP violations. The earlier mechanism for CSP reporting, `report-uri`, continues to be supported. Several new fields have been added to the violation reports common to both, including `effectiveDirective` (the policy that was violated), `statusCode` (the HTTP response code), `sourceFile` (the URL of the offending resource), `lineNumber`, and `columnNumber`.

#### Fetch

#### Web Authentication

#### WebDriver

#### WebGL

## Previous EdgeHTML releases
[EdgeHTML 13 / Windows build 14393 (11/2015)](https://blogs.windows.com/msedgedev/2015/11/16/introducing-edgehtml-13-our-first-platform-update-for-microsoft-edge/#TuusgqsWj8X6pDcD.97)

[EdgeHTML 14 / Windows build 10240 (7/2016)](https://blogs.windows.com/msedgedev/2016/08/04/introducing-edgehtml-14/#6xVDezg4bfyDyIWJ.97)
