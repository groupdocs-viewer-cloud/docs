---
id: "attachment-pages"
url: "viewer/attachment-pages"
title: "Attachment Pages"
productName: "GroupDocs.Viewer Cloud"
weight: 3
description: ""
keywords: ""
toc: True
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

## Get Email Attachment Pages List for HTML Rrepresentation

Sometimes, it is required to get email attachments as pages. You can retrieve list of attachment pages for HTML representation using following API. It returns object with list of attachment pages or ZIP archive with actual pages as HTML when "application/zip" accept header specified.

The following GroupDocs.Viewer Cloud REST API resource has been used in [retrieving pages list of email attachment (HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetAttachmentPages).

### cURL example

{{< tabs "example1">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"

```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "fileName": "Test.msg",
  "folder": null,
  "attachmentName": "Freescale OSC.pdf",
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "font.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/font.woff"
        },
        {
          "name": "font1.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/font1.woff"
        },
        {
          "name": "font2.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/font2.woff"
        },
        {
          "name": "image.png",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/styles.css"
        }
      ],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1"
    },
    {
      "number": 2,
      "resources": [
        {
          "name": "font.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/font.woff"
        },
        {
          "name": "font1.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/font1.woff"
        },
        {
          "name": "font2.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/font2.woff"
        },
        {
          "name": "image.png",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/styles.css"
        }
      ],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2"
    }
  ]
}
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example1-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Pages_Html.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Pages_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Pages_Html.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Pages_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Pages_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Pages_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Get Email Attachment Pages List for Image Representation

GroupDocs.Viewer Cloud also supports to get email attachments pages list for  Image representation. You can retrieve list of attachment pages as image using following API. It returns object with list of attachment pages or ZIP archive with actual pages as Image when "application/zip" accept header specified.

The following GroupDocs.Viewer Cloud REST API resource has been used in the [retrieving pages list of email attachment (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetAttachmentPages).

### cURL example

{{< tabs "example2">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "fileName": "Test.msg",
  "folder": null,
  "attachmentName": "Test.pdf",
  "pages": [
    {
      "number": 1,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/1"
    },
    {
      "number": 2,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/2"
    }
  ]
}
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example2-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Pages_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Pages_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Pages_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Pages_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Pages_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Pages_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Download ZIP Archive of Email Attachment Pages for HTML Representation

You can download ZIP archive of email attachments pages for HTML representation using following API. Please check [ZIP Archive structure]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/zip-file-structure/) for more details.

The following GroupDocs.Viewer Cloud REST API resource has been used to [download ZIP archive of attachment pages (HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetZipWithAttachmentPages).

### cURL example

{{< tabs "example3">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/zip" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```log
ZIP Archive with document pages as HTML
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example3-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Pages_ZIP_Html.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Pages_Zip_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Pages_ZIP_Html.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Pages_Zip_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Pages_Zip_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Pages_Zip_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Download ZIP Archive of Email Attachment Pages for Image Representation

You can download ZIP archive of email attachments pages for Image representation using following API. Please check [ZIP Archive structure]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/zip-file-structure/) for more details.

The following GroupDocs.Viewer Cloud REST API resource has been used in the [download ZIP archive of page attachments (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetZipWithAttachmentPages).

### cURL example

{{< tabs "example4">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/zip" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```log
ZIP Archive with document pages as Image
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example4-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Pages_ZIP_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Pages_Zip_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Pages_ZIP_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Pages_Zip_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Pages_Zip_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Pages_Zip_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Get Email Attachment Page for HTML Representation

You can download a specific page of an email attachment, following API is used to get specific page of email attachment as HTML. It returns actual contents of the page.

The following GroupDocs.Viewer Cloud REST API resource has been used [to retrieve specific page of email attachment (HTML Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetAttachmentPage).

### cURL example

{{< tabs "example5">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```log
Contents of Page as HTML
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example5-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Page_Html.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Page_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Page_Html.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Page_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Page_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Page_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Get Email Attachment Page for Image Representation

You can download a specific page of an email attachment, following API is used to get specific page of email attachment for Image Representation. It returns actual contents of the page.

The following GroupDocs.Viewer Cloud REST API resource has been used [to retrieve specific page of email attachment as Image](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetAttachmentPage).

### cURL example

{{< tabs "example6">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/1" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```log
page Contents as Image
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example6-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Page_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Page_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Page_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Page_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Attachment_Page_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Page_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Create Email Attachment Pages Cache for HTML Representation

You can create email attachment pages cache for HTML representation using following API. It expects [HtmlOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HHtmlOptionsObject||style#"background-color: transparent;" shape#"rect")  object data in request body and returns an object which contains list of links to attachment pages or ZIP archive with actual pages as HTML when "application/zip" accept header specified.

The following GroupDocs.Viewer Cloud REST API resource has been used [to create cache of email attachment pages( HTML Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlCreateAttachmentPagesCache).

### cURL example

{{< tabs "example7">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"resourcePath": "page/1/resource/styles.css","embedResources": true,"startPageNumber": 1,"countPages": 3,"renderComments": false}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-
LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9Td
wZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-
6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-
vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "fileName": "Test.msg",
  "folder": null,
  "attachmentName": "Test.pdf",
  "pages": [
    {
      "number": 1,
      "resources": [],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1"
    },
    {
      "number": 2,
      "resources": [],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2"
    },
    {
      "number": 3,
      "resources": [],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/3"
    }
  ]
}
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example7-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Attachment_Pages_Cache_Html.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Create_Attachment_Pages_Cache_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Attachment_Pages_Cache_Html.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Attachment_Pages_Cache_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Attachment_Pages_Cache_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Attachment_Pages_Cache_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Create Email Attachment Pages Cache for Image Representation #

You can create email attachment pages cache for Image representation using following API. It expects [ImageOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HHtmlOptionsObject) object data in request body and returns an object which contains list of links to attachment pages or ZIP archive with actual pages as HTML when "application/zip" accept header specified.

The following GroupDocs.Viewer Cloud REST API resource has been used [to create cache of email attachment pages (Image Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageCreateAttachmentPagesCache).

### cURL example

{{< tabs "example8">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"ExtractText":true,"startPageNumber":1,"countPages":3}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-
LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9Td
wZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-
6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-
vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "fileName": "Test.msg",
  "folder": null,
  "attachmentName": "Test.pdf",
  "pages": [
    {
      "number": 1,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/1"
    },
    {
      "number": 2,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/2"
    },
    {
      "number": 3,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/3"
    }
  ]
}
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example8-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Attachment_Pages_Cache_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Create_Attachment_Pages_Cache_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Attachment_Pages_Cache_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Attachment_Pages_Cache_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Attachment_Pages_Cache_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Attachment_Pages_Cache_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Remove Email Attachment Pages Cache

You can delete email attachment pages cache for HTML presentation using following API. An empty response with '204 No Content' status will be returned to confirm deletion.

The following GroupDocs.Viewer Cloud REST API resource has been used [to remove email attachment pages cache (HTML Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlDeleteAttachmentPagesCache).

### cURL example

{{< tabs "example9">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/cache" \
-X DELETE \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-
LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9Td
wZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-
6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-
vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```log
Empty response with '204 No Content' status.
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example9-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Delete_Attachment_Pages_Cache_Html.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Delete_Attachment_Pages_Cache_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Delete_Attachment_Pages_Cache_Html.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Delete_Attachment_Pages_Cache_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Delete_Attachment_Pages_Cache_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Delete_Attachment_Pages_Cache_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Remove Email Attachment Pages Cache for Image Representation #

You can delete email attachment pages cache for Image Representation using following API. An empty response with '204 No Content' status will be returned to confirm deletion.

The following GroupDocs.Viewer Cloud REST API resource has been used [to delete cache of email attachment pages (Image Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageDeleteAttachmentPagesCache).

### cURL example

{{< tabs "example10">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/cache" \
-X DELETE \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-
LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9Td
wZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-
6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-
vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} {{< tab "Resonse" >}}
```log
Empty response with '204 No Content' status.
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example10-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Delete_Attachment_Pages_Cache_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Delete_Attachment_Pages_Cache_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Delete_Attachment_Pages_Cache_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Delete_Attachment_Pages_Cache_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Delete_Attachment_Pages_Cache_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Delete_Attachment_Pages_Cache_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}
