---
id: "pdf-rendering"
url: "viewer/pdf-rendering"
title: "PDF Rendering"
productName: "GroupDocs.Viewer Cloud"
weight: 12
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

You can render a document to PDF for HTML representation and download it. The API returns actual file data of document in PDF format.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document as PDF for HTML representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlGetPdfFile).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pdf" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
Contents of PDF document
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download Document as PDF for HTML Representation ###

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pdf_File_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pdf_File_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pdf_File_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pdf_File_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Pdf_File_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pdf_File_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Download Document as PDF from Document URL for HTML Representation #

You can render a document to PDF from document URL for HTML representation and download it. The API returns actual file data of document in PDF format.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document as PDF from document Url for HTML representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlGetPdfFileFromUrl).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1.0/viewer/html/pdf?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&#x26;fileName#one-page.docx&#x26;renderComments#false&#x26;renderHiddenPages#true&#x26;folder#viewerdocs&#x26;storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X GET -d "{}" 
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
Contents of PDF document
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download Document as PDF from Document URL for HTML Representation ###

{{< tabs tabTotal="6" tabID="11" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pdf_File_from_Url_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pdf_File_from_Url_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pdf_File_from_Url_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pdf_File_from_Url_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Pdf_File_from_Url_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pdf_File_from_Url_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Download Document as PDF for Image Representation #

You can render a document to PDF for Image representation and download it. The API returns actual file data of document in PDF format.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document as PDF with Image representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageGetPdfFile).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="3" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pdf" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
Contents of PDF document
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Downlaod Document as PDF for Image Representation ###

{{< tabs tabTotal="6" tabID="12" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pdf_File_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pdf_File_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pdf_File_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pdf_File_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Pdf_File_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pdf_File_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Download Document as PDF from Document URL for Image Representation #

You can render a document to PDF from document URL for Image representation and download it. The API returns actual file data of document in PDF format.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document as PDF from document Url for Image representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageGetPdfFileFromUrl).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="4" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1.0/viewer/image/pdf?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&#x26;fileName#one-page.docx&#x26;renderComments#false&#x26;renderHiddenPages#true&#x26;folder#viewerdocs&#x26;storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X GET -d "{}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
Contents of PDF document
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download Document as PDF from Document URL for Image Representation ###

{{< tabs tabTotal="6" tabID="13" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pdf_File_from_Url_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pdf_File_from_Url_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pdf_File_from_Url_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pdf_File_from_Url_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Pdf_File_from_Url_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pdf_File_from_Url_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Watermark Document for HTML Representation #

You can watermark and download a document as PDF with GroupDocs.Viewer Cloud API. It creates new PDF document, removes PDF document if it was created before.

The API expects [PdfFileOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HPdfFileOptionsObject)object data in request body. It returns object which contains information about newly created PDF document along with '201 Created' status.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [watermark Document as PDF document for HTML representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlCreatePdfFile).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="5" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"watermark":{"text":"My Company"}}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "fileName": "one-page.docx",
  "folder": null,
  "pdfFileName": "one-page.pdf",
  "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pdf"
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Watermark document and download as PDF for HTML Representation ###

{{< tabs tabTotal="6" tabID="14" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Watermark_Pdf_File_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Watermark_Pdf_File_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Watermark_Pdf_File_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Watermark_Pdf_File_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Watermark_Pdf_File_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Watermark_Pdf_File_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Watermark Document for Image Representation #

You can watermark and download a document as PDF with GroupDocs.Viewer Cloud API. It creates new PDF document, removes PDF document if it was created before.

The API expects [PdfFileOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HPdfFileOptionsObject))object data in request body. It returns object which contains information about newly created PDF document along with '201 Created' status.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [watermark a document and download as PDF for Image Representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageCreatePdfFile).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="6" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"watermark":{"text":"My Company","color":"Magenta","position":"Diagonal","size":50}}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "fileName": "one-page.docx",
  "folder": null,
  "pdfFileName": "one-page.pdf",
  "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pdf"
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Watermark document and download as PDF for Image Representation ###

{{< tabs tabTotal="6" tabID="15" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Watermark_PdfFile_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Watermark_Pdf_File_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Watermark_Pdf_File_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Watermark_Pdf_File_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Watermark_Pdf_File_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Watermark_Pdf_File_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Create PDF Document as HTML Representation from Document in Request Body #

You can create a PDF document as HTML representation from document passed in request body. The API returns object which contains information about newly created PDF document along with '201 Created' status.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create PDF document as HTML representation from document in request body](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlCreatePdfFileFromContent).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="7" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/html/pdf?fileName#one-page.docx&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X POST
-H "Accept: application/json"
-d "{'watermark':{'text':'My Company'}}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "fileName": "one-page.docx",
  "folder": null,
  "pdfFileName": "one-page.pdf",
  "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pdf"
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create PDF Document as HTML Representation from Document in Request Body ###

{{< tabs tabTotal="6" tabID="16" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pdf_File_Request_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pdf_File_Request_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pdf_File_Request_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pdf_File_Request_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Pdf_File_Request_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pdf_File_Request_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Create PDF Document as Image Representation from Document in Request Body #

You can create a PDF document as Image representation from document passed in request body. The API returns object which contains information about newly created PDF document along with '201 Created' status.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create PDF document as Image representation from document in request body](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageCreatePdfFileFromContent).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="8" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/image/pdf?fileName#one-page.docx&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X POST
-H "Accept: application/json"
-d "{'watermark':{'text':'My Company'}}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "fileName": "one-page.docx",
  "folder": null,
  "pdfFileName": "one-page.pdf",
  "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pdf"
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create PDF Document as Image Representation from Document in Request Body ###

{{< tabs tabTotal="6" tabID="17" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pdf_File_Request_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pdf_File_Request_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pdf_File_Request_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pdf_File_Request_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Pdf_File_Request_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pdf_File_Request_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Create PDF Document from Document URL for HTML Representation #

You can create a PDF document from document URL for HTML representation. The API returns object which contains information about newly created PDF document along with '201 Created' status.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create PDF document from document Url for HTML representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/HtmlCreatePdfFileFromUrl).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="9" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/html/pdf?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&#x26;fileName#one-page.docx&#x26;folder#viewerdocs&#x26;storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X PUT -d "{'watermark': {'text': 'My Company','color': 'Magenta','position': 'Diagonal','size': 50}}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "fileName": "one-page4.docx",
  "folder": "viewerdocs",
  "pdfFileName": "one-page4.pdf",
  "url": "http://api.groupdocs.cloud/v1.0/viewer/one-page4.docx/html/pdf?folder#viewerdocs"
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create PDF Document from Document URL for HTML Representation ###

{{< tabs tabTotal="6" tabID="18" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pdf_File_from_Url_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pdf_File_from_Url_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_java_Create_Pdf_File_from_Url_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pdf_File_from_Url_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Pdf_File_from_Url_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pdf_File_from_Url_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Create PDF Document from Document URL for Image Representation #

You can create a PDF document from document URL for Image representation. The API returns object which contains information about newly created PDF document along with '201 Created' status.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create PDF document from document Url for Image representation](https://apireference.groupdocs.cloud/viewer/#!/PDF/ImageCreatePdfFileFromUrl).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="10" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/image/pdf?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&#x26;fileName#one-page.docx&#x26;folder#viewerdocs&#x26;storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X PUT -d "{'watermark': {'text': 'My Company','color': 'Magenta','position': 'Diagonal','size': 50}}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "fileName": "one-page6.docx",
  "folder": "viewerdocs",
  "pdfFileName": "one-page6.pdf",
  "url": "http://api.groupdocs.cloud/v1.0/viewer/one-page6.docx/image/pdf?folder#viewerdocs"
}
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create PDF Document from Document URL for Image Representation ###

{{< tabs tabTotal="6" tabID="19" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pdf_File_from_Url_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pdf_File_from_Url_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pdf_File_from_Url_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pdf_File_from_Url_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Pdf_File_from_Url_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pdf_File_from_Url_Image.py >}}

{{< /tab >}} {{< /tabs >}}

