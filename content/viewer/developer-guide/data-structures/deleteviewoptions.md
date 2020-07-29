---
id: "deleteviewoptions"
url: "viewer/deleteviewoptions"
title: "DeleteViewOptions"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

# DeleteViewOptions #

DeleteViewOptions data structure used as input parameters for [Delete View]({{< ref "viewer/developer-guide/_index.md" >}})working-with-viewer-api/) API 
|---|---

##### DeleteViewOptions example #####

```html 

{
  "FileInfo": {
    "FilePath": "string",
    "StorageName": "string",
    "VersionId": "string",
    "Password": "string"
  }
}

 ```

##### DeleteViewOptions fields #####

|Name|Description
|---|---
|FileInfo.FilePath|The path of the document, delete view requested for. **Required.**
|FileInfo.StorageName|Storage name
|FileInfo.VersionId|File version Id
|FileInfo.Password|Not used

