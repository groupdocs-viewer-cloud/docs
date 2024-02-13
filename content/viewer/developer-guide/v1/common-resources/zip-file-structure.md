---
id: "zip-file-structure"
url: "viewer/zip-file-structure"
title: "ZIP File Structure"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

{{< alert style="info" >}}
Note:  The features listed in this Page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

Page contains description about structure and naming of ZIP files.

## ZIP File Naming

All ZIP files returned by the API follows same naming convention. File name consists of three parts where first is string "viewer-download-", second is combined date and time in UTC presented in [ISO_8601](https://en.wikipedia.org/wiki/ISO_8601) format and third is extension ".zip".

### Example ZIP file name template

```bash

viewer-download-yyyyMMddTHHmmssZ.zip

```

### Example ZIP file name

```bash

viewer-download-20170728T235959Z.zip

```

## ZIP File With Images

ZIP archive contains document pages where each file is image. Image file name consists of three parts where first is string "p", second is page number and third is one of listed extensions ".jpg" or ".png".

### Example image file name template

```bash

p{page-number}.[jpg|png]

```

### Example image file name

```bash

p1.png

```

### Example ZIP file with images

```bash

ROOT
 ├── p1.png
 ├── p2.png
 ├── p3.png
 ├── ...

```

## ZIP File With HTML

ZIP archive contains document pages in HTML format and HTML resources (styles, fonts and images). HTML file name consists of three parts where first is string "p", second is page number and third is extension ".html".

### Example HTML file name template

```bash

p{page-number}.html

```

### Example HTML file name ###

```bash

p1.html

```

### Example ZIP file with HTML pages

```bash
ROOT
 ├── p1
 │   ├── p1.html
 │   ├── r
 │   │   ├── styles.css
 │   │   ├── font.ttf
 │   │   ├── font1.ttf
 │   │   ├── font2.ttf
 │   │   ├── image.png
 ├── p2
 │   ├── p2.html
 │   ├── r
 │   │   ├── styles.css
 │   │   ├── font.ttf
 │   │   ├── font1.ttf
 │   │   ├── font2.ttf
 │   │   ├── image.png
 ├── p3
 │   ├── p3.html
 │   ├── r
 │   │   ├── styles.css
 │   │   ├── font.ttf
 │   │   ├── font1.ttf
 │   │   ├── font2.ttf
 │   │   ├── image.png
 ├── ...

```
