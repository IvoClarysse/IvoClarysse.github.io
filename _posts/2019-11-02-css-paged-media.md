---
layout: post
title:  "CSS Paged Media"
date:   2019-11-01 13:20:36 -0700
categories: css pdf docs
---

An overview of toolchains that can generate PDFs using CSS Paged Media.

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

[fop]: https://xmlgraphics.apache.org/fop/
[batik]: https://xmlgraphics.apache.org/batik/
[chromium]: https://www.chromium.org/Home
[skia]: https://www.skia.org/
[webkit]: https://webkit.org/
[poppler]: https://poppler.freedesktop.org/
[puppeteer]: https://github.com/GoogleChrome/puppeteer
[wkhtmltopdf]: https://wkhtmltopdf.org/
[AntennaHouse]: https://antennahouse.com/
[PDFreactor]: https://pdfreactor.com/
[PrinceXML]: https://princexml.com/
[DocRaptor]: https://docraptor.com/
[WeasyPrint]: https://weasyprint.org/

## PlantUML

- [PlantUML](http://plantuml.com/) : Open-source tool that uses simple textual descriptions to draw UML diagrams.
    - [plantuml/plantuml](https://github.com/plantuml/plantuml) : Generate UML diagram from textual description
    - [plantuml/plantuml-server](https://github.com/plantuml/plantuml-server) : PlantUML server
- [plantuml/plantuml-server](https://hub.docker.com/r/plantuml/plantuml-server/) : Official docker image of PlantUML server over Jetty or Tomcat.
- [Wikipedia: PLantUML](https://en.wikipedia.org/wiki/PlantUML) : "PlantUML is an open-source tool allowing users to create UML diagrams from a plain text language."

## References

- [DocBook xslt10-stylesheets](https://github.com/docbook/xslt10-stylesheets)
    - [Release 1.79.2](https://github.com/docbook/xslt10-stylesheets/releases/tag/release%2F1.79.2)
- [Why You Should Be Using XSLT 3.0](https://www.xml.com/articles/2017/02/14/why-you-should-be-using-xslt-30/) - A look at the upcoming XSLT 3.0 release, and why it matters beyond the XML community. February 14, 2017, XML.com
- [yEd - Graph Editor](https://www.yworks.com/products/yed) : yEd - Graph Editor
