---
layout: post
title:  "CSS Paged Media"
date:   2019-11-01 13:20:36 -0700
categories: css pdf docs
---

An overview of toolchains that to generate PDFs using CSS Paged Media.

## Toolchains

| Tool           | CSS   | XSL-FO | PDF Engine         | List Price        | Issues                                              |
|----------------|-------|--------|--------------------|-------------------|-----------------------------------------------------|
| [fop]          | **✕** | ✓      | [fop],[batik]      | Free              | Complex styling; No HTML+CSS, bad SVG rasterization |
| [wkhtmltopdf]  | ✓     | ✕      | [webkit],[poppler] | Free              | No CSS3 column support, bad SVG rasterization       |
| [puppeteer]    | ✓     | ✕      | [chromium],[skia]  | Free              | No PDF bookmarks                                    |
| [AntennaHouse] | ✓     | ✓      | [AntennaHouse]     | $5000/server      | Expensive                                           |
| [PDFreactor]   | ✓     | ✕      | [PDFreactor]       | $2950/server      | Expensive                                           |
| [PrinceXML]    | ✓     | ✓      | [PrinceXML]        | $3800/server      | Expensive                                           |
| [DocRaptor]    | ✓     | ✕      | [PrinceXML]        | $0.025-0.0090/doc | SaaS                                                |
| [WeasyPrint]   | ✓     | ✕      | [WeasyPrint]       | Free              | Limited CSS3 column support                         |

- Chromium PDF issue: Blink should use the new (2017) Skia API.
    - [607777 - "save as PDF" doesn't generate a 508 compliance PDF](https://bugs.chromium.org/p/chromium/issues/detail?id=607777)
    - [738643 - Blink text layout should attach original text to SkTextBlobs](https://bugs.chromium.org/p/chromium/issues/detail?id=738643)
    - [781797 - Feature request PDF bookmarks/outlines](https://bugs.chromium.org/p/chromium/issues/detail?id=781797)
    - [988352 - Fonts rendering wrong after PDF printing](https://bugs.chromium.org/p/chromium/issues/detail?id=988352)
-   <https://weasyprint.org/>

[fop]: https://xmlgraphics.apache.org/fop/
[batik]: https://xmlgraphics.apache.org/batik/
[chromium]: https://www.chromium.org/Home
[webkit]: https://webkit.org/
[poppler]: https://poppler.freedesktop.org/
[puppeteer]: https://github.com/GoogleChrome/puppeteer
[wkhtmltopdf]: https://wkhtmltopdf.org/
[AntennaHouse]: https://antennahouse.com/
[PDFreactor]: https://pdfreactor.com/
[PrinceXML]: https://princexml.com/
[DocRaptor]: https://docraptor.com/
[WeasyPrint]: https://weasyprint.org/
