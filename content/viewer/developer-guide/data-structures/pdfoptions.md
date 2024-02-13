---
id: "pdfoptions"
url: "viewer/pdfoptions"
title: "PdfOptions"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

PdfOptions data structure inherits [RenderOptions]({{< ref "viewer/developer-guide/data-structures/renderoptions.md" >}}) and used as part of [ViewOptions]({{< ref "viewer/developer-guide/data-structures/viewoptions.md" >}}) data structure.

### ImageOptions example

```json
{
    "DocumentOpenPassword": "string",
    "PermissionsPassword": "string",
    "Permissions": ["AllowAll", "DenyModification"],
    "PdfOptimizationOptions": {},
    "ImageMaxWidth": 0,
    "ImageMaxHeight": 0,
    "ImageWidth": 0,
    "ImageHeight": 0
}
```

### ImageOptions fields

|Name|Description
|---|---
|RenderOptions fields|PdfOptions inherits all properties of [RenderOptions]({{< ref "viewer/developer-guide/data-structures/renderoptions.md" >}})
|DocumentOpenPassword|The password required to open the PDF document
|PermissionsPassword|The password required to change permission settings; Using a permissions password you can restrict printing, modification and data extraction
|Permissions|The array of PDF document permissions. Allowed values are: AllowAll, DenyPrinting, DenyModification, DenyDataExtraction, DenyAll. Default value is AllowAll, if now permissions are set.
|PdfOptimizationOptions|Contains options for rendering documents into PDF format. See [PdfOptimizationOptions]({{< ref "viewer/developer-guide/data-structures/pdfoptimizationoptions.md" >}})
|ImageMaxWidth|Max width of an output image in pixels. (When converting single image to PDF only)
|ImageMaxHeight|Max height of an output image in pixels. (When converting single image to PDF only)
|ImageWidth|The width of the output image in pixels. (When converting single image to PDF only)
|ImageHeight|The height of an output image in pixels. (When converting single image to PDF only)
