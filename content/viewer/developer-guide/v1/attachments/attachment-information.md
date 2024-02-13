---
id: "attachment-information"
url: "viewer/attachment-information"
title: "Attachment Information"
productName: "GroupDocs.Viewer Cloud"
weight: 2
description: ""
keywords: ""
toc: True
---

{{< alert style="info" >}}
Note: The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

## HTML Representation of Email Attachment Information

Sometimes it is required to get email attachment information for HTML representation. Info API helps to retrieves attachment information. It returns an object that contains information about file format and file size. It also includes information about attachment pages and attachments

The following GroupDocs.Viewer Cloud REST API resource has been used in the [attachment Information (HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetAttachmentInfo).

### cURL example

{{< tabs "example1">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/info" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "fileName": "Test.pdf",
  "extension": ".pdf",
  "fileFormat": "Portable Document Format",
  "size": 298902,
  "dateModified": "2017-12-19T12:16:55.2103401Z",
  "pages": [
    {
      "number": 1,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 2,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 3,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 4,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ],
  "attachments": []
}
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).


{{< tabs "example1-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Info_Html.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Info_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Info_Html.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Info_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Info_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Info_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Image Representation of Email Attachment Information

GroupDocs.Viewer Cloud also supports to get email attachment information for Image representation. Info API helps to retrieves attachment information. It returns an object that contains information about file format and file size. It also includes information about attachment pages and attachments.

The following GroupDocs.Viewer Cloud REST API resource has been used in the [attachment information (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetAttachmentInfo).

### cURL example

{{< tabs "example2">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/info" \
-X GET \
-H "Content-Type: application/json" \-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "fileName": "Test.pdf",
  "extension": ".pdf",
  "fileFormat": "Portable Document Format",
  "size": 298902,
  "dateModified": "2017-12-19T12:16:55.2103401Z",
  "pages": [
    {
      "number": 1,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 2,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 3,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 4,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ],
  "attachments": []
}
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example2-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Info_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Info_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Info_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Info_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Info_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Info_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## HTML Representation of Email Attachment Info with Document Information Options

You can retrieve attachment information with specified [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject) for HTML representation. API expects [DocumentInfoOptions ]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject)object data in request body. It returns an object that contains information about file format and file size. Response also includes information about attachment pages and attachments..

The following GroupDocs.Viewer Cloud REST API resource has been used in the [attachment information with option (HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetAttachmentInfoWithOptions).

### cURL example

{{< tabs "example3">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/info" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"password": "test"}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "fileName": "Test.pdf",
  "extension": ".pdf",
  "fileFormat": "Portable Document Format",
  "size": 298902,
  "dateModified": "2017-12-19T12:16:55.2103401Z",
  "pages": [
    {
      "number": 1,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 2,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 3,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 4,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ],
  "attachments": []
}
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example3-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Info_WithOptions_Html.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Info_WithOptions_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Info_WithOptions_Html.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Info_WithOptions_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Info_WithOptions_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Info_WithOptions_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Image Representation of Email Attachment Info with Document Information Options

You can retrieve attachment information with specified [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject) for Image representation. API expects [DocumentInfoOptions ]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject)object data in request body. It returns an object that contains information about file format and file size. Response also includes information about attachment pages and attachments.

The following GroupDocs.Viewer Cloud REST API resource has been used in the [attachment information with option (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetAttachmentInfoWithOptions).

### cURL example

{{< tabs "example4">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/info" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"password": "test"}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "fileName": "Test.pdf",
  "extension": ".pdf",
  "fileFormat": "Portable Document Format",
  "size": 298902,
  "dateModified": "2017-12-19T12:16:55.2103401Z",
  "pages": [
    {
      "number": 1,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 2,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 3,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 4,
      "name": null,
      "width": 595,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ],
  "attachments": []
}
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example4-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Info_WithOptions_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Info_WithOptions_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Info_WithOptions_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Info_WithOptions_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Info_WithOptions_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Info_WithOptions_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}
