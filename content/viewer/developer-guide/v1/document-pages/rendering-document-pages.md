---
id: "rendering-document-pages"
url: "viewer/rendering-document-pages"
title: "Rendering Document Pages"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}





This section provides API details to create document pages cache, retrieve pages, modify pages and delete document pages cache.






# Get List of Links to Document Pages as HTML #

You can retrieve list of links to document pages as HTML. The API returns an object which contains list of links to document pages.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get list of links to document pages as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"

 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "font.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/font.woff"
        },
        {
          "name": "styles.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/styles.css"
        },
        {
          "name": "styles1.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/styles1.css"
        }
      ],
      "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1"
    },
    {
      "number": 2,
      "resources": [
        {
          "name": "font.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/2/resources/font.woff"
        },
        {
          "name": "styles.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/2/resources/styles.css"
        },
        {
          "name": "styles1.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/2/resources/styles1.css"
        }
      ],
      "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/2"
    },
    {
      "number": 3,
      "resources": [
        {
          "name": "font.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/3/resources/font.woff"
        },
        {
          "name": "styles.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/3/resources/styles.css"
        },
        {
          "name": "styles1.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/3/resources/styles1.css"
        }
      ],
      "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/3"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocscloud/GroupDocs.Viewer-Cloud/tree/master/SDKs).

### Get Lists of Document Pages link for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pages_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pages_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pages_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pages_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Pages_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pages_HTML.py >}}









# Get List of Links to Document Pages as Image #

You can retrieve list of links to document pages as images. The API returns an object which contains list of links to document pages as images or ZIP archive with actual pages as image when "application/zip" accept header specified.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get list of links to document pages as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageGetPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages/1"
    },
    {
      "number": 2,
      "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages/2"
    },
    {
      "number": 3,
      "url": "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages/3"
    }
  ],
  "url": null
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocscloud/GroupDocs.Viewer-Cloud/tree/master/SDKs).

### Get Lists of Document Pages link for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pages_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pages_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pages_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pages_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Pages_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pages_Image.py >}}









# Download ZIP Archive with Document Pages as HTML #

GroupDocs.Viewer Cloud can retrieve ZIP archive of Document pages as HTML. API returns ZIP archive with pages as HTML. Please check [ZIP File Structure]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/zip-file-structure/) for more details.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get ZIP archive of document pages as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetZipWithPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/zip" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
ZIP archive with document pages as HTML
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get ZIP Archive of Document Pages as HTML ###



 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_ZIP_With_Pages_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_ZIP_With_Pages_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_ZIP_With_Pages_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_ZIP_With_Pages_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_ZIP_With_Pages_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_ZIP_With_Pages_HTML.py >}}





 

# Download ZIP Archive with Document Pages as Image #

GroupDocs.Viewer Cloud can retrieve ZIP archive of Document pages as Image. The API returns ZIP archive with pages as Image. Please check [ZIP File Structure]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/zip-file-structure/) for more details.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get zip archive of document pages as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageGetZipWithPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages/zip" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
ZIP archive with document pages as Image
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get ZIP Archive of Document Pages as Image ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_ZIP_With_Pages_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_ZIP_With_Pages_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_ZIP_With_Pages_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_ZIP_With_Pages_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_ZIP_With_Pages_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_ZIP_With_Pages_Image.py >}}









# Get List of Links to Document Pages from provided URL as HTML #

You can retrieve list of links to document pages of document at provided URL. The API returns an object that contains list of links to document pages as HTML.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get list of links to document pages from provided URL as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetPagesFromUrl).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/html/pages?url#https%3a%2f%2fwww.dropbox.com%2fs%2fumokluz338w4ng7%2fone-page.docx%3fdl%3d1&#x26;embeddedResources#true" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"

 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "folder": null,
  "pages": [
     {
      "number": 1,
      "resources": [],
      "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1?embedResources#true"
     }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Lists of Document Pages link from provided URL for HTML Representation ###



 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pages_URL_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pages_URL_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pages_URL_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pages_URL_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Pages_URL_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pages_URL_HTML.py >}}





 

# Get List of Links to Document Pages from provided URL as Image #

You can retrieve list of links to document pages of document at provided URL. The API returns an object that contains list of links to document pages as Image.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get list of links to document pages from provided URL as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageGetPagesFromUrl).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/image/pages?url#https%3a%2f%2fwww.dropbox.com%2fs%2fumokluz338w4ng7%2fone-page.docx%3fdl%3d1" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Lists of Document Pages from provided URL link for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pages_URL_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pages_URL_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pages_URL_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pages_URL_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Pages_URL_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pages_URL_Image.py >}}









# Download Document Page as HTML #

You can download the document page as HTML. The API returns the actual data of document page as HTML.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document page as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetPage).

## cURL REST Example ##





 Request

```html 
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/sample-one-page.docx/html/pages/1?ignoreResourcePathInResources#true&#x26;embedResources#true&#x26;renderComments#false&#x26;renderHiddenPages#true&#x26;appsid#XXXX&#x26;signature#XXX-XX" 
-H "Content-Type: application/json" 
-X GET -d "{}"
 ```




 Response

```html 
Contents of page as HTML
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download Document Page as HTML ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Download_Document_Page_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Download_Document_Page_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Download_Document_Page_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Download_Document_Page_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Download_Document_Page_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Download_Document_Page_HTML.py >}}









# Download Document Page as Image #

You can download the document page as Image. The API returns the actual data of document page as Image.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document page as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageGetPage).

## cURL REST Example ##





 Request

```html 
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/sample-one-page.docx/image/pages/1?extractText#true&#x26;renderComments#false&#x26;renderHiddenPages#true&#x26;appsid#XXXX&#x26;signature#XXX-XX" 
-H "Content-Type: application/json" 
-X GET -d "{}"
 ```




 Response

```html 
Contents of page as Image
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download Document Page as Image ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Download_Document_Page_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Download_Document_Page_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Download_Document_Page_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Download_Document_Page_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Download_Document_Page_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Download_Document_Page_Image.py >}}









# Create Document Cache as HTML #

You can create the document pages as HTML and save them in cache. The API returns object which contains list of links to document pages along with '201 Created' status and if pages already created will be removed from cache.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Request

```html 
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/sample.docx/html/pages?storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX" 
-H "Content-Type: application/json" 
-X POST -d "{'resourcePath': 'page/1/resource/style.css','embedResources': true,'startPageNumber': 1,'countPages': 3,'renderComments': false}"
 ```




 Response

```html 
{
  "fileName": "sample.docx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [],
      "url": "http://api.groupdocs.cloud/v1.0/viewer/sample.docx/html/pages/1"
    },
    {
      "number": 2,
      "resources": [],
      "url": "http://api.groupdocs.cloud/v1.0/viewer/sample.docx/html/pages/2"
    },
    {
      "number": 3,
      "resources": [],
      "url": "http://api.groupdocs.cloud/v1.0/viewer/sample.docx/html/pages/3"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache as HTML ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Document_Cache_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Document_Cache_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Document_Cache_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Document_Cache_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Document_Cache_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Document_Cache_HTML.py >}}









# Create Document Cache as Image #

You can create the document pages as Images and save them in cache. The API returns object which contains list of links to document pages along with '201 Created' status and if pages already created will be removed from cache.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageCreatePagesCache).

## cURL REST Example ##





 Request

```html 
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/sample.docx/image/pages?storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX" 
-H "Content-Type: application/json" 
-X POST -d "{'resourcePath': 'page/1/resource/style.css','embedResources': true,'startPageNumber': 1,'countPages': 3,'renderComments': false}"
 ```




 Response

{
 "fileName": "sample.docx",
 "folder": null,
 "pages": [
 {
 "number": 1,
 "url": ""
 },
 {
 "number": 2,
 "url": ""
 },
 {
 "number": 3,
 "url": ""
 }
 ],
 "url": null
}








## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache as Image ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Document_Cache_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Document_Cache_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Document_Cache_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Document_Cache_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Document_Cache_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Document_Cache_HTML.py >}}









# Rendering MS Project Document Pages as HTML #

Starting from GroupDocs.Viewer Cloud 18.2 two new options have been added which allows to adjust Page Size and Time Unit when rendering MS Project documents. By default GroupDocs.Viewer API tries to find optimal output size and time unit, depending on the projects overall length, depending on the projects overall length. In case you need to set your own page size or time unit, you can specify **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** which provides two options **PageSize** and **TimeUnit**.  Time unit refers to smallest unit (days, third of a month or month) used in timescale bar, when the TimeUnit # "Days" is set you will get the most detailed view of your tasks and opposite, when TimeUnit # "Month" is set you will get more general representation of tasks. This example demonstrates how to create pages cache as HTML with provided **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}).**

**NOTE: [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/document-information.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages" \
-X POST \
-H "Content-Type: application/json" \
-d "{"projectOptions": {"pageSize": "A0","timeUnit": "unknown"}}" \
-H "authorization: Bearer [Access Token]"
 ```




 Response

```html 
{
  "fileName": "sample.mpp",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [],
      "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Pages Cache as HTML of MS Project Document ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Project_Page_Cache_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Project_Page_Cache_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Project_Page_Cache_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Project_Page_Cache_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Project_Page_Cache_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Project_Page_Cache_HTML.py >}}









# Rendering MS Project Document Pages as Image #

Starting from GroupDocs.Viewer Cloud 18.2 two new options have been added which allows to adjust Page Size and Time Unit when rendering MS Project documents. By default GroupDocs.Viewer API tries to find optimal output size and time unit, depending on the projects overall length, depending on the projects overall length. In case you need to set your own page size or time unit, you can specify **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** which provides two options **PageSize** and **TimeUnit**.  Time unit refers to smallest unit (days, third of a month or month) used in timescale bar, when the TimeUnit # "Days" is set you will get the most detailed view of your tasks and opposite, when TimeUnit # "Month" is set you will get more general representation of tasks. This example demonstrates how to create pages cache as Image with provided **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}).**

**NOTE: [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/document-information.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/sample.mpp/image/pages" \
-X POST \
-H "Content-Type: application/json" \
-d "{"projectOptions": {"pageSize": "A0","timeUnit": "unknown"}}" \
-H "authorization: Bearer [Access Token]"
 ```




 Response

```html 
{
  "fileName": "sample.mpp",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [],
      "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Pages Cache as Image of MS Project Document ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Project_Page_Cache_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Project_Page_Cache_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Project_Page_Cache_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Project_Page_Cache_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Project_Page_Cache_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Project_Page_Cache_Image.py >}}









# Create Document Cache as HTML from Document in Request Body #

You can create the document pages as HTML from document in request body and saves them in cache. The API returns object which contains list of links to document pages along with '201 Created' status and if pages already created will be removed from cache.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML from document in request body](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCacheFromContent).

## cURL REST Example ##





 Request

```html 
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/html/pages?fileName#one-page.docx&#x26;appsid#XXXX&#x26;signature#XXX-XX" 
-H "Content-Type: application/json" 
-X POST 
-H "Accept: application/json" 
-d "{'resourcePath':'page/{page-number}/resource/{resource-name}"
 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [
          {
            "resourceName": "font2.woff",
            "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/font2.woff"
          },
          {
            "resourceName": "fontFaces.css",
            "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/fontFaces.css"
          },
          {
            "resourceName": "styles.css",
            "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/styles.css"
          }
      ]
    }
  ]
}


 
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache as HTML from Document in Request Body ###

 





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pages_Cache_Request_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pages_Cache_Request_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pages_Cache_Request_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pages_Cache_Request_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Pages_Cache_Request_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pages_Cache_Request_HTML.py >}}









# Create Document Cache as Image from Document in Request Body #

You can create the document pages as Image from document in request body and saves them in cache. The API returns object which contains list of links to document pages along with '201 Created' status and if pages already created will be removed from cache.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as Image from document in request body](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageCreatePagesCacheFromContent).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1.0/viewer/image/pages?fileName#one-page.docx&#x26;appsid#XXXX&#x26;signature#XXX-XX" 
-H "Content-Type: application/json" 
-X POST 
-H "Accept: application/json" 
-d "{'format':'jpg','quality':90,'width':600,'height':800,'startPageNumber':1,'countPages':1,'extractText':true,'renderComments':true}"
 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache as Image from Document in Request Body ###

 





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pages_Cache_Request_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pages_Cache_Request_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pages_Cache_Request_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pages_Cache_Request_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Pages_Cache_Request_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pages_Cache_Request_Image.py >}}









# Create Document Cache for Document URL with HtmlOptions as HTML #

You can create the document pages as HTML and saves them in cache with HtmlOptions. The API returns object which contains list of links to document pages along with '201 Created' status and if file name already exist then unique file name will be will be used for file.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache for document url with HtmlOptions as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCacheFromUrl).

## cURL REST Example ##





 Request

curl -v "https://api.groupdocs.cloud/v1.0/viewer/html/pages?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&fileName#one-page.docx&storage#First%20Storage&appsid#XXXX&signature#XXX-XX"

-H "Content-Type: application/json"

-X PUT -d "{'embedResources': true}"






 Response

```html 
{
  "fileName": "one-page.docx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [],
      "url": "http://api.groupdocs.cloud/v1.0/viewer/one-page.docx/html/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache for Document URL with HTMLOptions as HTML ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Document_Cache_Url_With_HTMLOptions.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Document_Cache_Url_With_HTMLOptions.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Document_Cache_Url_With_HTMLOptions.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Document_Cache_Url_With_HTMLOptions.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Document_Cache_Url_With_HTMLOptions.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Document_Cache_Url_With_HTMLOptions.py >}}









# Create Document Cache for Document URL with ImageOptions as Image #

You can create the document pages as Image and saves them in cache with ImageOptions. The API returns object which contains list of links to document pages or ZIP archive with actual pages as image when "application/zip" accept header specified along with '201 Created' status and if file name already exist then unique file name will be will be used for file.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache for document url with ImageOptions as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageCreatePagesCacheFromUrl).

## cURL REST Example ##





 Request

curl -v  "XX-XX" 

-H "Content-Type: application/json" 

-X PUT -d "{'format': 'jpeg','quality': 70}"






 Response

```html 
{
  "fileName": "one-page3.docx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "url": "http://api.groupdocs.cloud/v1.0/viewer/one-page3.docx/image/pages/1"
    }
  ],
  "url": null
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache for Document URL with ImageOptions as Image ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Document_Cache_Url_With_ImageOptions.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Document_Cache_Url_With_ImageOptions.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Document_Cache_Url_With_ImageOptions.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Document_Cache_Url_With_ImageOptions.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Document_Cache_Url_With_ImageOptions.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Document_Cache_Url_With_ImageOptions.py >}}









# Rotate Document Pages for HTML Representation #

GroupDocs.Viewer Cloud can rotate document page for HTML Representation. The API returns object with updated list of pages upon success. Please check [RotateOptions Object]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HRotateOptionsObject) for request parameter.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [rotate the document pages with HTML representation](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlTransformPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"pageNumber":1,"angle":90}" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
  "pages": [
    {
      "number": 1,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 90,
      "visible": true,
      "rows": null
    },
    {
      "number": 2,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 3,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Rotate Document Pages for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Rotate_Page_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Rotate_Page_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Rotate_Page_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Rotate_Page_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Rotate_Page_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Rotate_Page_HTML.py >}}









# Rotate Document Pages for Image Representation #

GroupDocs.Viewer Cloud can rotate document page for Image Representation. The API returns object with updated list of pages upon success. Please check [RotateOptions Object]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HRotateOptionsObject) for request body parameter.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [rotate document pages with Image representation](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageTransformPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"pageNumber":1,"angle":90}" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
  "pages": [
    {
      "number": 1,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 90,
      "visible": true,
      "rows": null
    },
    {
      "number": 2,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 3,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Rotate Document Pages for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Rotate_Page_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Rotate_Page_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Rotate_Page_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Rotate_Page_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Rotate_Page_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Rotate_Page_Image.py >}}









# Reorder Document Pages for HTML Representation #

GroupDocs.Viewer Cloud can reorder document pages for HTML Representation. The API returns object with updated list of pages upon success. Please check [ReorderOptions Object]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/) for request parameter.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [reorder the document pages with HTML representation](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlTransformPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"pageNumber":1,"newPosition":3}" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
  "pages": [
    {
      "number": 2,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 3,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 1,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 90,
      "visible": true,
      "rows": null
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Reorder Document Pages for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Reorder_Page_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Reorder_Page_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Reorder_Page_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Reorder_Page_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Reorder_Page_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Reorder_Page_HTML.py >}}









# Reorder Document Pages for Image Representation #

GroupDocs.Viewer Cloud can reorder document page for Image Representation. The API returns object with updated list of pages upon success. Please check [ReorderOptions Object]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/) for request body parameter.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [reorder document pages with Image representation](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageTransformPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"pageNumber":1,"newPosition":3}" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
  "pages": [
    {
      "number": 2,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 3,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    },
    {
      "number": 1,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 90,
      "visible": true,
      "rows": null
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Reorder Document Pages for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Reorder_Page_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Reorder_Page_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Reorder_Page_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Reorder_Page_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Reorder_Page_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Reorder_Page_Image.py >}}









# Remove Document Cache for HTML Pages #

You can remove the document HTML pages cache. The API returns an empty response with '204 No Content' status will be returned to confirm deletion.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [remove document cache for HTML pages](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlDeletePagesCache).

## cURL REST Example ##





 Request

curl -v  "XX-XX" 

-H "Content-Type: application/json" -X DELETE -d "{}"






 Response

```html 
Empty response with '204 No Content' status.
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Remove Document Cache for HTML Pages ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Remove_Document_Cache_for_HTML_Pages.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Remove_Document_Cache_for_HTML_Pages.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Remove_Document_Cache_for_HTML_Pages.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Remove_Document_Cache_for_HTML_Pages.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Remove_Document_Cache_for_HTML_Pages.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Remove_Document_Cache_for_HTML_Pages.py >}}









# Remove Document Cache for Page Images #

You can remove the document page images cache. The API returns an empty response with '204 No Content' status will be returned to confirm deletion.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [remove document cache for page Images](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageDeletePagesCache).

## cURL REST Example ##





 Request

curl -v  "XX-XX" 

-H "Content-Type: application/json" 

-X DELETE -d "{}"






 Response

```html 
Empty response with '204 No Content' status.
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Remove Document Cache for Page Image ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Remove_Document_Cache_for_Image_Pages.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Remove_Document_Cache_for_Image_Pages.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Remove_Document_Cache_for_HTML_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Remove_Document_Cache_for_Image_Pages.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Remove_Document_Cache_for_Image_Pages.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Remove_Document_Cache_for_Image_Pages.py >}}









# Specify Image Quality when Rendering PDF Documents as HTML #

You can set image quality of PDF document when rendering as HTML. The API returns an object which contains list of links to document pages.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Specify Image Quality when Rendering PDF Documents as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Requestcurl -v "[http:~~/~~/api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages](http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages)" \

-X GET \

-data '{"pdfOptions": {"imageQuality": "High"}' \

-H"Content-Type: application/json" \

-H "authorization: Bearer "






 Response

```html 
{
  "fileName": "sample2.pdf",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "font.woff",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages/1/resources/font.woff"
        },
        {
          "name": "font1.woff",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages/1/resources/font1.woff"
        },
        {
          "name": "image.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages/1/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages/1/resources/styles.css"
        }
      ],
      "url": "http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages/1"
    },
    {
      "number": 2,
      "resources": [
        {
          "name": "font.woff",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages/2/resources/font.woff"
        },
        {
          "name": "styles.css",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages/2/resources/styles.css"
        }
      ],
      "url": "http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages/2"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Specify Image Quality when Rendering PDF Documents as HTML ###



 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Set_image_quality.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Set_image_quality.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Set_image_quality.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Set_image_quality.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Set_image_quality.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Set_image_quality.py >}}





 

# Exclude fonts when rendering as HTML #

You can prevent adding fonts in resultant document when rendering as HTML, to decrease the file size. The API returns an object which contains list of links to document pages.

{{< alert style="info" >}}
.ExcludeFontsList option allows to exclude specific fonts (that are commonly available on most of the devices). The example below shows how to prevent adding fonts into output HTML. Currently, it works only for Presentation documents. We are planning to extend support for this feature for all document types where it is applicable in the upcoming releases.--data '{"embedResources": true, "excludeFontsList": ["Arial"]}'
{{< /alert >}}

Resource

The following GroupDocs.Viewer Cloud REST API resource has been used to [Prevent Adding Fonts in document when rendering as Html](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Requestcurl -v "http:~/~/api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages"  \

-X GET -data '{"excludeFonts": true }' \

-H "Content-Type: application/json"  \

-H "authorization: Bearer [Access Token]"






 Response

```html 
      {
  "fileName": "one-page1.docx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "image.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1/resources/styles.css"
        }
      ],
      "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Exclude font when rendering as HTML ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Exclude_Fonts.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Exclude_Fonts.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Exclude_Fonts.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Exclude_Fonts.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Exclude_Fonts.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_Exclude_Fonts.py >}}










# Auto Fit column width rendering document as HTML #

You can set property to auto fit column with depending upon content when rendering document as Html. The API returns an object which contains list of links to document pages.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Auto Fit column width rendering document as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Requestcurl -v "[http:~~/~~/api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages](http://api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages)" \

-X GET -data '{"cellsOptions": {"textOverflowMode": "AutoFitColumn"}'  \

-H "Content-Type: application/json"  \

-H "authorization: Bearer [Access Token]"






 Response

```html 
      {
  "fileName": "with-overflowed-text.xlsx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "image.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1/resources/styles.css"
        }
      ],
      "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Autofit column width rendering document as HTML ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_text_Overflow_Mode.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_text_Overflow_Mode.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_text_Overflow_Mode.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_text_Overflow_Mode.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_text_Overflow_Mode.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_Exclude_Fonts.py >}}










# Rendering only Print Area in Excel document as HTML #

You can set property to render sections of the workshet(s) defined as [print area](https://support.office.com/en-us/article/set-or-clear-a-print-area-on-a-worksheet-27048af8-a321-416d-ba1b-e99ae2182a7e when rendering MS Excel document as Html. The API returns an object which contains list of links to document pages.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Rendering only Print Area in Excel document as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Requestcurl -v "[http:~~/~~/api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages](http://api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages)"  \

-X GET -data '{"cellsOptions": {"renderPrintAreaOnly": true, "renderHiddenColumns": true}}'  \

-H "Content-Type: application/json"  \

-H "authorization: Bearer [Access Token]"






 Response

```html 
      {
  "fileName": "with-overflowed-text.xlsx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "image.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1/resources/styles.css"
        }
      ],
      "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Rendering only Print Area in Excel document as HTML ###




 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_render_PrintArea_Only.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_render_PrintArea_Only.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_render_PrintArea_Only.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_render_PrintArea_Only.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_render_PrintArea_Only.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_render_PrintArea_Only.py >}}





 


# Include/exclude hidden content in Excel documents as HTML #

You can set property to include/exclude hidden content when rendering MS Excel document as Html. The API returns an object which contains list of links to document pages.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [include/exclude hidden content in Excel documents as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Requestcurl -v "[http:~~/~~/api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages](http://api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages)"  \

-X GET -data '{"cellsOptions": {"renderHiddenRows": true, "renderHiddenColumns": true}}'  \

-H "Content-Type: application/json" \

-H "authorization: Bearer [Access Token]"






 Response

```html 
      {
  "fileName": "with-overflowed-text.xlsx",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "image.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1/resources/styles.css"
        }
      ],
      "url": "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Include/exclude hidden content in Excel documents as HTML ###






 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_render_Hidden_Rows.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_render_Hidden_Rows.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_render_Hidden_Rows.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_render_Hidden_Rows.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_render_Hidden_Rows.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_render_Hidden_Rows.py >}}










# Rendering PDF Documents into HTML with Setting (Default Font) #


Since the version 18.7, it is possible to set default font when rendering PDF document into HTML. This setting may be useful when you would like to specify which font should be used in case PDF document missing some font(s)


## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Rendering PDF Document into Html](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetPagesFromUrl).

## cURL REST Example ##





 Request\\



# Set default font name when rendering PDF document as HTML




curl request POST \




url http:~/~/api.groupdocs.cloud/v1/viewer/missing-font.pdf/html/pages \




header 'authorization: [Access Token]' \




header 'content-type: application/json' \




data '{"defaultFontName": "Arial"}'




  




# Retrieve created page




curl request GET \




  ~-~-url http:~/~/api.groupdocs.cloud/v1/viewer/missing-font.pdf/html/pages/1 \




  ~-~-header 'authorization: [Access Token]'







 Response

```html 
      {
  "fileName": "sample.pdf",
  "folder": null,
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "image.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample.pdf/html/pages/1/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample.pdf/html/pages/1/resources/styles.css"
        }
      ],
      "url": "http://api.groupdocs.cloud/v1/viewer/sample.pdf/html/pages/1"
    }
  ]
}
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Rendering PDF Documents into HTML with Setting (Default Font) ###



 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Render_PDF_DefaultFont.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Render_PDF_DefaultFont.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Render_PDF_DefaultFont.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Render_PDF_DefaultFont.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Render_PDF_DefaultFont.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_Render_PDF_DefaultFont.py >}}





 





 

 