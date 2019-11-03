---
layout: post
title:  "CSS Paged Media"
date:   2019-11-01 13:20:36 -0700
categories: css pdf docs
---

An overview of toolchains that to generate PDFs using CSS Paged Media.

## Toolchains

| Tool           | CSS | XSL-FO | PDF Engine         | List Price        | Issues                                              |
|----------------|-----|--------|--------------------|-------------------|-----------------------------------------------------|
| [fop]          | n   | y      | [fop],[batik]      | Free              | Complex styling; No HTML+CSS, bad SVG rasterization |
| [wkhtmltopdf]  | y   | n      | [webkit],[poppler] | Free              | No CSS3 column support, bad SVG rasterization       |
| [puppeteer]    | y   | n      | [chromium],[skia]  | Free              | No PDF bookmarks                                    |
| [AntennaHouse] | y   | y      | [AntennaHouse]     | $5000/server      | Expensive                                           |
| [PDFreactor]   | y   | n      | [PDFreactor]       | $2950/server      | Expensive                                           |
| [PrinceXML]    | y   | y      | [PrinceXML]        | $3800/server      | Expensive                                           |
| [DocRaptor]    | y   | n      | [PrinceXML]        | $0.025-0.0090/doc | SaaS                                                |
| [WeasyPrint]   | y   | n      | [WeasyPrint]       | Free              | Limited CSS3 column support                         |

- Chromium PDF issue: Blink should use the new (2017) Skia API.
    - <https://bugs.chromium.org/p/chromium/issues/detail?id=607777> Issue 607777 - "save as PDF" doesn't generate a 508 compliance PDF
    - <https://bugs.chromium.org/p/chromium/issues/detail?id=738643> Issue 738643 - Blink text layout should attach original text to SkTextBlobs
    - <https://bugs.chromium.org/p/chromium/issues/detail?id=781797> Issue 781797 - Feature request PDF bookmarks/outlines
    - <https://bugs.chromium.org/p/chromium/issues/detail?id=988352> Issue 988352 - Fonts rendering wrong after PDF printing
-   <https://weasyprint.org/>

[fop]: https://xmlgraphics.apache.org/fop/
[batik]: https://xmlgraphics.apache.org/batik/
[chromium]: https://chromium.org/
[webkit]: https://webkit.org/
[poppler]: https://poppler.org/
[puppeteer]: https://puppeteer.org/
[wkhtmltopdf]: https://wkhtmltopdf.org/
[AntennaHouse]: https://antennahouse.com/
[PDFreactor]: https://pdfreactor.com/
[PrinceXML]: https://princexml.com/
[DocRaptor]: https://docraptor.com/
[WeasyPrint]: https://weasyprint.org/
