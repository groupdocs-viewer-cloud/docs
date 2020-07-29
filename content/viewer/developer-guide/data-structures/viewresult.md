---
id: "viewresult"
url: "viewer/viewresult"
title: "ViewResult"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

# ViewResult #

ViewResult data structure returned by Document [View API]({{< ref "viewer/developer-guide/_index.md" >}})working-with-viewer-api/) as output result
|---|---

##### ViewResult example #####

```html 

{
  "pages": [
    {
      "number": 1,
      "resources": [],
      "path": "viewer/words/docx/four-pages_docx/p1.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/words/docx/four-pages_docx/p1.html"
    },
    {
      "number": 2,
      "resources": [],
      "path": "viewer/words/docx/four-pages_docx/p2.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/words/docx/four-pages_docx/p2.html"
    },
    {
      "number": 3,
      "resources": [],
      "path": "viewer/words/docx/four-pages_docx/p3.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/words/docx/four-pages_docx/p3.html"
    },
    {
      "number": 4,
      "resources": [],
      "path": "viewer/words/docx/four-pages_docx/p4.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/words/docx/four-pages_docx/p4.html"
    }
  ],
  "attachments": [],
  "file": null
}

 ```

##### ViewResult fields #####

|Name|Description
|---|---
|pages|List of document pages
|page.number|Page number, starts from 1
|page.resources|Page resources. Returned if HTML view format requested with ExternalResources option set to true
|page.path|Page file path in the cloud storage. Use this value to download page using [File API]({{< ref "viewer/developer-guide/working-with-files.md" >}}))
|page.downloadUrl|Page file direct download link (Requires Authorization).
|attachments|List of document attachments
|file|PDF file path. Returned instead of pages, if PDF view format requested

