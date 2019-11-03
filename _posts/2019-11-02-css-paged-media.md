---
layout: post
title:  "CSS Paged Media"
date:   2019-11-01 13:20:36 -0700
categories: css pdf docs
---

## Toolchains

| Tool         | CSS | XSL-FO | PDF Engine     | List Price        | Issues                                              |
|--------------|-----|--------|----------------|-------------------|-----------------------------------------------------|
| fop          | n   | y      | fop,batik      | Free              | Complex styling; No HTML+CSS, bad SVG rasterization |
| wkhtmltopdf  | y   | n      | webkit,poppler | Free              | No CSS3 column support, bad SVG rasterization       |
| puppeteer    | y   | n      | chrome,skia    | Free              | No PDF bookmarks                                    |
| AntennaHouse | y   | y      | AntennaHouse   | $5000/server      | Expensive                                           |
| PDFreactor   | y   | n      | PDFreactor     | $2950/server      | Expensive                                           |
| PrinceXML    | y   | y      | PrinceXML      | $3800/server      | Expensive                                           |
| DocRaptor    | y   | n      | PrinceXML      | $0.025-0.0090/doc | SaaS                                                |
| WeasyPrint   | y   | n      | WeasyPrint     | Free              | Limited CSS3 column support, Python3.4+             |

-   Chrome: <https://bugs.chromium.org/p/chromium/issues/detail?id=781797> Issue 781797: Feature request PDF bookmarks/outlines
-   <https://weasyprint.org/>


