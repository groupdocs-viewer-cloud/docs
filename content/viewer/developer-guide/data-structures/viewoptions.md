---
id: "viewoptions"
url: "viewer/viewoptions"
title: "ViewOptions"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

# ViewOptions #

ViewOptions data structure used as input parameters for [Document Info]({{< ref "viewer/developer-guide/_index.md" >}})working-with-viewer-api/) API and [Document View]({{< ref "viewer/developer-guide/_index.md" >}})working-with-viewer-api/) API. 
|---|---|---|---

{{< alert style="info" >}}
Not all options are supported by all document formats. Each option may correspond to one or more formats.
{{< /alert >}}

##### ViewOptions example #####

```html 

{
  "ViewFormat": "HTML",
  "FileInfo": {
    "FilePath": "string",
    "StorageName": "string",
    "VersionId": "string",
    "Password": "string"
  },  
  "OutputPath": "string",
  "FontsPath": "string",
  "Watermark": {
    "Text": "string",
    "Color": "string",
    "Position": "string",
    "Size": 0
  },
  "RenderOptions": {
    "StartPageNumber": 0,
    "CountPagesToRender": 0,
	"ExternalResources": false,
	"ExtractText": false,
  }
}

 ```

##### ViewOptions fields #####

|Name|Description|API Version
|---|---|---
|ViewFormat|Allows to set rendering format, available values are: HTML, JPG, PNG, BMP, PDF.

Default value is "HTML".| 
|---
|FileInfo.FilePath|The path of the document, located in the storage. **Required.**| 
|FileInfo.StorageName|Storage name| 
|FileInfo.VersionId|File version Id| 
|FileInfo.Password|Password for rendering password-protected documents| 
|OutputPath|The output path for results. Default value is 'viewer\{input file path}_{file extension}\'|v19.4
|FontsPath|Path of the folder, containing fonts, used for documents rendering.| 
|Watermark.Text|The watermark text.| 
|Watermark.Color|The watermark color.
Supported formats "Magenta", "(112,222,11)", "(50,112,222,11)".
Default value is "Red".| 
|Watermark.Position|The watermark position.
Supported positions "Diagonal", "TopLeft", "TopCenter", "TopRight", "BottomLeft", "BottomCenter" and "BottomRight".
Default value is "Diagonal".| 
|Watermark.Size|Watermark size in percents.
Default value is 100. | 
|RenderOptions| [RenderOptions ]({{< ref "viewer/developer-guide/data-structures/renderoptions.md" >}}))in case of ViewFormat # PDF,

 [HtmlOptions ]({{< ref "viewer/developer-guide/data-structures/htmloptions.md" >}}))in case of ViewFormat # HTML,
|---|---

 [ImageOptions ]({{< ref "viewer/developer-guide/data-structures/imageoptions.md" >}}))in case of ViewFormat # PNG, BMP, or JPG| 
|---|---|---

