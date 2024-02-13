---
id: "pdf-rendering"
url: "viewer/pdf-rendering"
title: "PDF Rendering"
productName: "GroupDocs.Viewer Cloud"
weight: 12
description: ""
keywords: ""
toc: True
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

## Dwonload file as PDF from Storage (HTML mode)

You can render a document to PDF for HTML representation and download it. The API returns actual file data of document in PDF format.

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document as PDF for HTML representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlGetPdfFile).

### cURL example

{{< tabs "download-file-as-pdf-from-storage-curl">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pdf" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} 
{{< tab "Response" >}}
```log
Contents of PDF document
```
{{< /tab >}} 
{{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "download-file-as-pdf-from-storage-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pdf_File_HTML.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pdf_File_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pdf_File_HTML.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pdf_File_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Pdf_File_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pdf_File_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Download Document as PDF by URL (HTML mode)

You can render a document to PDF from document URL for HTML representation and download it. The API returns actual file data of document in PDF format.

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document as PDF from document Url for HTML representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlGetPdfFileFromUrl).

### cURL example

{{< tabs "download-pdf-by-url-curl">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1.0/viewer/html/pdf?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&#x26;fileName#one-page.docx&#x26;renderComments#false&#x26;renderHiddenPages#true&#x26;folder#viewerdocs&#x26;storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X GET -d "{}" 
```
{{< /tab >}} 
{{< tab "Response">}}
```log
Contents of PDF document
```
{{< /tab >}} 
{{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "download-pdf-by-url-curl-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pdf_File_from_Url_HTML.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pdf_File_from_Url_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pdf_File_from_Url_HTML.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pdf_File_from_Url_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Pdf_File_from_Url_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pdf_File_from_Url_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Download Document as PDF from Storage (Image mode)

You can render a document to PDF for Image representation and download it. The API returns actual file data of document in PDF format.

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document as PDF with Image representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageGetPdfFile).

### cURL example

{{< tabs "download-document-as-pdf-from-storage-image-curl">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pdf" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} 
{{< tab "Response" >}}
```log
Contents of PDF document
```
{{< /tab >}} 
{{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "download-document-as-pdf-from-storage-image-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pdf_File_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pdf_File_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pdf_File_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pdf_File_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Pdf_File_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pdf_File_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Download Document as PDF by URL (Image mode)

You can render a document to PDF from document URL for Image representation and download it. The API returns actual file data of document in PDF format.

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document as PDF from document Url for Image representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageGetPdfFileFromUrl).

### cURL example

{{< tabs "download-document-as-pdf-by-url-image-curl">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1.0/viewer/image/pdf?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&#x26;fileName#one-page.docx&#x26;renderComments#false&#x26;renderHiddenPages#true&#x26;folder#viewerdocs&#x26;storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X GET -d "{}"
```
{{< /tab >}} 
{{< tab "Response" >}}
```log
Contents of PDF document
```
{{< /tab >}} 
{{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "download-document-as-pdf-by-url-image-sdks">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pdf_File_from_Url_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pdf_File_from_Url_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pdf_File_from_Url_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pdf_File_from_Url_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Pdf_File_from_Url_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pdf_File_from_Url_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Add watermark (HTML mode)

You can watermark and download a document as PDF with GroupDocs.Viewer Cloud API. It creates new PDF document, removes PDF document if it was created before.

The API expects [PdfFileOptions]({{< ref "viewer/developer-guide/_index.md" >}}) object data in request body. It returns object which contains information about newly created PDF document along with '201 Created' status.

The following GroupDocs.Viewer Cloud REST API resource has been used to [watermark Document as PDF document for HTML representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlCreatePdfFile).

### cURL example

{{< tabs "add-watermark-html-curl">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"watermark":{"text":"My Company"}}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} 
{{< tab "Response" >}}
```json
{
  "fileName": "one-page.docx",
  "folder": null,
  "pdfFileName": "one-page.pdf",
  "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pdf"
}
```
{{< /tab >}}
{{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "add-watermark-html-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Watermark_Pdf_File_HTML.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Watermark_Pdf_File_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Watermark_Pdf_File_HTML.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Watermark_Pdf_File_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Watermark_Pdf_File_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Watermark_Pdf_File_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Add watermark (Image mode)

You can watermark and download a document as PDF with GroupDocs.Viewer Cloud API. It creates new PDF document, removes PDF document if it was created before.

The API expects [PdfFileOptions]({{< ref "viewer/developer-guide/_index.md" >}}) object data in request body. It returns object which contains information about newly created PDF document along with '201 Created' status.

The following GroupDocs.Viewer Cloud REST API resource has been used to [watermark a document and download as PDF for Image Representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageCreatePdfFile).

### cURL example

{{< tabs "add-watermark-image-curl">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"watermark":{"text":"My Company","color":"Magenta","position":"Diagonal","size":50}}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
```
{{< /tab >}} 
{{< tab "Response" >}}
```json
{
  "fileName": "one-page.docx",
  "folder": null,
  "pdfFileName": "one-page.pdf",
  "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pdf"
}
```
{{< /tab >}}
{{< /tabs >}}

### SDK example

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "add-watermark-image-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Watermark_PdfFile_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Watermark_Pdf_File_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Watermark_Pdf_File_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Watermark_Pdf_File_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Watermark_Pdf_File_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Watermark_Pdf_File_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Create PDF from file in request body (HTML mode)

You can create a PDF document as HTML representation from document passed in request body. The API returns object which contains information about newly created PDF document along with '201 Created' status.

The following GroupDocs.Viewer Cloud REST API resource has been used to [create PDF document as HTML representation from document in request body](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlCreatePdfFileFromContent).

### cURL example

{{< tabs "create-pdf-from-file-in-body-html-curl">}}
{{< tab "Request" >}}
```bash
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/html/pdf?fileName#one-page.docx&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X POST
-H "Accept: application/json"
-d "{'watermark':{'text':'My Company'}}"
```
{{< /tab >}}
{{< tab "Response" >}}
```json
{
  "fileName": "one-page.docx",
  "folder": null,
  "pdfFileName": "one-page.pdf",
  "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pdf"
}
```
{{< /tab >}} 
{{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "create-pdf-from-file-in-body-html-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pdf_File_Request_HTML.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pdf_File_Request_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pdf_File_Request_HTML.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pdf_File_Request_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Pdf_File_Request_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pdf_File_Request_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Create PDF from file in request body (Image mode)

You can create a PDF document as Image representation from document passed in request body. The API returns object which contains information about newly created PDF document along with '201 Created' status.

The following GroupDocs.Viewer Cloud REST API resource has been used to [create PDF document as Image representation from document in request body](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageCreatePdfFileFromContent).

### cURL example

{{< tabs "create-pdf-from-file-in-request-body-image-curl">}}
{{< tab "Request" >}}
```bash
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/image/pdf?fileName#one-page.docx&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X POST
-H "Accept: application/json"
-d "{'watermark':{'text':'My Company'}}"
```
{{< /tab >}} 
{{< tab "Response" >}}
```json
{
  "fileName": "one-page.docx",
  "folder": null,
  "pdfFileName": "one-page.pdf",
  "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pdf"
}
```
{{< /tab >}} 
{{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "create-pdf-from-file-in-request-body-image-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pdf_File_Request_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pdf_File_Request_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pdf_File_Request_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pdf_File_Request_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Pdf_File_Request_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pdf_File_Request_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Create PDF from URL (HTML mode)

You can create a PDF document from document URL for HTML representation. The API returns object which contains information about newly created PDF document along with '201 Created' status.

The following GroupDocs.Viewer Cloud REST API resource has been used to [create PDF document from document Url for HTML representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlCreatePdfFileFromUrl).

### cURL example

{{< tabs "create-psd-from-url-html-curl">}}
{{< tab "Request" >}}
```bash
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/html/pdf?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&#x26;fileName#one-page.docx&#x26;folder#viewerdocs&#x26;storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X PUT -d "{'watermark': {'text': 'My Company','color': 'Magenta','position': 'Diagonal','size': 50}}"
```
{{< /tab >}} 
{{< tab "Response" >}}
```json
{
  "fileName": "one-page4.docx",
  "folder": "viewerdocs",
  "pdfFileName": "one-page4.pdf",
  "url": "http://api.groupdocs.cloud/v1.0/viewer/one-page4.docx/html/pdf?folder#viewerdocs"
}
```
{{< /tab >}} 
{{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "create-psd-from-url-html-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pdf_File_from_Url_HTML.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pdf_File_from_Url_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_java_Create_Pdf_File_from_Url_HTML.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pdf_File_from_Url_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Pdf_File_from_Url_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pdf_File_from_Url_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Create PDF from URL (Image mode)

You can create a PDF document from document URL for Image representation. The API returns object which contains information about newly created PDF document along with '201 Created' status.

The following GroupDocs.Viewer Cloud REST API resource has been used to [create PDF document from document Url for Image representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageCreatePdfFileFromUrl).

### cURL example

{{< tabs "create-pdf-from-url-image-curl">}}
{{< tab "Request" >}}
```bash
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/image/pdf?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&#x26;fileName#one-page.docx&#x26;folder#viewerdocs&#x26;storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X PUT -d "{'watermark': {'text': 'My Company','color': 'Magenta','position': 'Diagonal','size': 50}}"
```
{{< /tab >}} 
{{< tab "Response" >}}
```json
{
  "fileName": "one-page6.docx",
  "folder": "viewerdocs",
  "pdfFileName": "one-page6.pdf",
  "url": "http://api.groupdocs.cloud/v1.0/viewer/one-page6.docx/image/pdf?folder#viewerdocs"
}
```
{{< /tab >}} 
{{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "create-pdf-from-url-image-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pdf_File_from_Url_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pdf_File_from_Url_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pdf_File_from_Url_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pdf_File_from_Url_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Pdf_File_from_Url_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pdf_File_from_Url_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}
