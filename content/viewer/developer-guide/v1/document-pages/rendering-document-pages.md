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

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"

```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocscloud/GroupDocs.Viewer-Cloud/tree/master/SDKs).

### Get Lists of Document Pages link for HTML Representation ###

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pages_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pages_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pages_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pages_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Pages_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pages_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Get List of Links to Document Pages as Image #

You can retrieve list of links to document pages as images. The API returns an object which contains list of links to document pages as images or ZIP archive with actual pages as image when "application/zip" accept header specified.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get list of links to document pages as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageGetPages).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocscloud/GroupDocs.Viewer-Cloud/tree/master/SDKs).

### Get Lists of Document Pages link for Image Representation ###

{{< tabs tabTotal="6" tabID="11" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pages_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pages_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pages_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pages_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Pages_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pages_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Download ZIP Archive with Document Pages as HTML #

GroupDocs.Viewer Cloud can retrieve ZIP archive of Document pages as HTML. API returns ZIP archive with pages as HTML. Please check [ZIP File Structure]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/zip-file-structure/) for more details.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get ZIP archive of document pages as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetZipWithPages).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="3" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/zip" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
ZIP archive with document pages as HTML
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get ZIP Archive of Document Pages as HTML ###

{{< tabs tabTotal="6" tabID="12" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_ZIP_With_Pages_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_ZIP_With_Pages_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_ZIP_With_Pages_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_ZIP_With_Pages_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_ZIP_With_Pages_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_ZIP_With_Pages_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Download ZIP Archive with Document Pages as Image #

GroupDocs.Viewer Cloud can retrieve ZIP archive of Document pages as Image. The API returns ZIP archive with pages as Image. Please check [ZIP File Structure]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/zip-file-structure/) for more details.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get zip archive of document pages as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageGetZipWithPages).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="4" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages/zip" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
ZIP archive with document pages as Image
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get ZIP Archive of Document Pages as Image ###

{{< tabs tabTotal="6" tabID="13" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_ZIP_With_Pages_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_ZIP_With_Pages_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_ZIP_With_Pages_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_ZIP_With_Pages_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_ZIP_With_Pages_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_ZIP_With_Pages_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Get List of Links to Document Pages from provided URL as HTML #

You can retrieve list of links to document pages of document at provided URL. The API returns an object that contains list of links to document pages as HTML.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get list of links to document pages from provided URL as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetPagesFromUrl).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="5" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/html/pages?url#https%3a%2f%2fwww.dropbox.com%2fs%2fumokluz338w4ng7%2fone-page.docx%3fdl%3d1&#x26;embeddedResources#true" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"

```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Lists of Document Pages link from provided URL for HTML Representation ###

{{< tabs tabTotal="6" tabID="14" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pages_URL_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pages_URL_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pages_URL_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pages_URL_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Pages_URL_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pages_URL_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Get List of Links to Document Pages from provided URL as Image #

You can retrieve list of links to document pages of document at provided URL. The API returns an object that contains list of links to document pages as Image.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get list of links to document pages from provided URL as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageGetPagesFromUrl).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="6" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/image/pages?url#https%3a%2f%2fwww.dropbox.com%2fs%2fumokluz338w4ng7%2fone-page.docx%3fdl%3d1" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Lists of Document Pages from provided URL link for Image Representation ###

{{< tabs tabTotal="6" tabID="15" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Pages_URL_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Pages_URL_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Pages_URL_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Pages_URL_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Pages_URL_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Pages_URL_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Download Document Page as HTML #

You can download the document page as HTML. The API returns the actual data of document page as HTML.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document page as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetPage).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="7" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/sample-one-page.docx/html/pages/1?ignoreResourcePathInResources#true&#x26;embedResources#true&#x26;renderComments#false&#x26;renderHiddenPages#true&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X GET -d "{}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
Contents of page as HTML
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download Document Page as HTML ###

{{< tabs tabTotal="6" tabID="16" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Download_Document_Page_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Download_Document_Page_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Download_Document_Page_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Download_Document_Page_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Download_Document_Page_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Download_Document_Page_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Download Document Page as Image #

You can download the document page as Image. The API returns the actual data of document page as Image.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download document page as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageGetPage).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="8" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/sample-one-page.docx/image/pages/1?extractText#true&#x26;renderComments#false&#x26;renderHiddenPages#true&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X GET -d "{}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
Contents of page as Image
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download Document Page as Image ###

{{< tabs tabTotal="6" tabID="17" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Download_Document_Page_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Download_Document_Page_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Download_Document_Page_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Download_Document_Page_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Download_Document_Page_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Download_Document_Page_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Create Document Cache as HTML #

You can create the document pages as HTML and save them in cache. The API returns object which contains list of links to document pages along with '201 Created' status and if pages already created will be removed from cache.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="9" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/sample.docx/html/pages?storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X POST -d "{'resourcePath': 'page/1/resource/style.css','embedResources': true,'startPageNumber': 1,'countPages': 3,'renderComments': false}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache as HTML ###

{{< tabs tabTotal="6" tabID="18" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Document_Cache_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Document_Cache_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Document_Cache_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Document_Cache_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Document_Cache_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Document_Cache_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Create Document Cache as Image #

You can create the document pages as Images and save them in cache. The API returns object which contains list of links to document pages along with '201 Created' status and if pages already created will be removed from cache.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="40" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/sample.docx/image/pages?storage#First%20Storage&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X POST -d "{'resourcePath': 'page/1/resource/style.css','embedResources': true,'startPageNumber': 1,'countPages': 3,'renderComments': false}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html

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
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache as Image ###

{{< tabs tabTotal="6" tabID="19" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Document_Cache_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Document_Cache_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Document_Cache_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Document_Cache_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Document_Cache_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Document_Cache_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Rendering MS Project Document Pages as HTML #

Starting from GroupDocs.Viewer Cloud 18.2 two new options have been added which allows to adjust Page Size and Time Unit when rendering MS Project documents. By default GroupDocs.Viewer API tries to find optimal output size and time unit, depending on the projects overall length, depending on the projects overall length. In case you need to set your own page size or time unit, you can specify **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** which provides two options **PageSize** and **TimeUnit**.  Time unit refers to smallest unit (days, third of a month or month) used in timescale bar, when the TimeUnit # "Days" is set you will get the most detailed view of your tasks and opposite, when TimeUnit # "Month" is set you will get more general representation of tasks. This example demonstrates how to create pages cache as HTML with provided **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}).**

**NOTE: [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/document-information.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="41" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages" \
-X POST \
-H "Content-Type: application/json" \
-d "{"projectOptions": {"pageSize": "A0","timeUnit": "unknown"}}" \
-H "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Pages Cache as HTML of MS Project Document ###

{{< tabs tabTotal="6" tabID="20" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Project_Page_Cache_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Project_Page_Cache_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Project_Page_Cache_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Project_Page_Cache_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Project_Page_Cache_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Project_Page_Cache_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Rendering MS Project Document Pages as Image #

Starting from GroupDocs.Viewer Cloud 18.2 two new options have been added which allows to adjust Page Size and Time Unit when rendering MS Project documents. By default GroupDocs.Viewer API tries to find optimal output size and time unit, depending on the projects overall length, depending on the projects overall length. In case you need to set your own page size or time unit, you can specify **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** which provides two options **PageSize** and **TimeUnit**.  Time unit refers to smallest unit (days, third of a month or month) used in timescale bar, when the TimeUnit # "Days" is set you will get the most detailed view of your tasks and opposite, when TimeUnit # "Month" is set you will get more general representation of tasks. This example demonstrates how to create pages cache as Image with provided **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}).**

**NOTE: [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/document-information.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="42" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/sample.mpp/image/pages" \
-X POST \
-H "Content-Type: application/json" \
-d "{"projectOptions": {"pageSize": "A0","timeUnit": "unknown"}}" \
-H "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Pages Cache as Image of MS Project Document ###

{{< tabs tabTotal="6" tabID="21" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Project_Page_Cache_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Project_Page_Cache_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Project_Page_Cache_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Project_Page_Cache_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Project_Page_Cache_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Project_Page_Cache_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Create Document Cache as HTML from Document in Request Body #

You can create the document pages as HTML from document in request body and saves them in cache. The API returns object which contains list of links to document pages along with '201 Created' status and if pages already created will be removed from cache.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML from document in request body](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCacheFromContent).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="43" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "https://api.groupdocs.cloud/v1.0/viewer/html/pages?fileName#one-page.docx&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X POST
-H "Accept: application/json"
-d "{'resourcePath':'page/{page-number}/resource/{resource-name}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache as HTML from Document in Request Body ###

{{< tabs tabTotal="6" tabID="22" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pages_Cache_Request_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pages_Cache_Request_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pages_Cache_Request_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pages_Cache_Request_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Pages_Cache_Request_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pages_Cache_Request_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Create Document Cache as Image from Document in Request Body #

You can create the document pages as Image from document in request body and saves them in cache. The API returns object which contains list of links to document pages along with '201 Created' status and if pages already created will be removed from cache.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as Image from document in request body](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageCreatePagesCacheFromContent).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="44" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1.0/viewer/image/pages?fileName#one-page.docx&#x26;appsid#XXXX&#x26;signature#XXX-XX"
-H "Content-Type: application/json"
-X POST
-H "Accept: application/json"
-d "{'format':'jpg','quality':90,'width':600,'height':800,'startPageNumber':1,'countPages':1,'extractText':true,'renderComments':true}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache as Image from Document in Request Body ###

{{< tabs tabTotal="6" tabID="23" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pages_Cache_Request_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pages_Cache_Request_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pages_Cache_Request_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pages_Cache_Request_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Pages_Cache_Request_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pages_Cache_Request_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Create Document Cache for Document URL with HtmlOptions as HTML #

You can create the document pages as HTML and saves them in cache with HtmlOptions. The API returns object which contains list of links to document pages along with '201 Created' status and if file name already exist then unique file name will be will be used for file.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache for document url with HtmlOptions as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCacheFromUrl).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="45" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

curl -v "https://api.groupdocs.cloud/v1.0/viewer/html/pages?url#https%3A%2F%2Fwww.dropbox.com%2Fs%2Fumokluz338w4ng7%252fone-page.docx&fileName#one-page.docx&storage#First%20Storage&appsid#XXXX&signature#XXX-XX"

-H "Content-Type: application/json"

-X PUT -d "{'embedResources': true}"

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache for Document URL with HTMLOptions as HTML ###

{{< tabs tabTotal="6" tabID="24" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Document_Cache_Url_With_HTMLOptions.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Document_Cache_Url_With_HTMLOptions.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Document_Cache_Url_With_HTMLOptions.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Document_Cache_Url_With_HTMLOptions.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Document_Cache_Url_With_HTMLOptions.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Document_Cache_Url_With_HTMLOptions.py >}}

{{< /tab >}} {{< /tabs >}}

# Create Document Cache for Document URL with ImageOptions as Image #

You can create the document pages as Image and saves them in cache with ImageOptions. The API returns object which contains list of links to document pages or ZIP archive with actual pages as image when "application/zip" accept header specified along with '201 Created' status and if file name already exist then unique file name will be will be used for file.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache for document url with ImageOptions as Image](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageCreatePagesCacheFromUrl).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="46" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

curl -v  "XX-XX"

-H "Content-Type: application/json"

-X PUT -d "{'format': 'jpeg','quality': 70}"

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Cache for Document URL with ImageOptions as Image ###

{{< tabs tabTotal="6" tabID="25" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Document_Cache_Url_With_ImageOptions.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Document_Cache_Url_With_ImageOptions.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Document_Cache_Url_With_ImageOptions.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Document_Cache_Url_With_ImageOptions.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Document_Cache_Url_With_ImageOptions.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Document_Cache_Url_With_ImageOptions.py >}}

{{< /tab >}} {{< /tabs >}}

# Rotate Document Pages for HTML Representation #

GroupDocs.Viewer Cloud can rotate document page for HTML Representation. The API returns object with updated list of pages upon success. Please check [RotateOptions Object]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HRotateOptionsObject) for request parameter.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [rotate the document pages with HTML representation](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlTransformPages).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="47" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"pageNumber":1,"angle":90}" \
-H "authorization: Bearer [Access Token]"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Rotate Document Pages for HTML Representation ###

{{< tabs tabTotal="6" tabID="26" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Rotate_Page_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Rotate_Page_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Rotate_Page_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Rotate_Page_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Rotate_Page_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Rotate_Page_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Rotate Document Pages for Image Representation #

GroupDocs.Viewer Cloud can rotate document page for Image Representation. The API returns object with updated list of pages upon success. Please check [RotateOptions Object]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HRotateOptionsObject) for request body parameter.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [rotate document pages with Image representation](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageTransformPages).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="48" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"pageNumber":1,"angle":90}" \
-H "authorization: Bearer [Access Token]"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Rotate Document Pages for HTML Representation ###

{{< tabs tabTotal="6" tabID="27" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Rotate_Page_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Rotate_Page_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Rotate_Page_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Rotate_Page_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Rotate_Page_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Rotate_Page_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Reorder Document Pages for HTML Representation #

GroupDocs.Viewer Cloud can reorder document pages for HTML Representation. The API returns object with updated list of pages upon success. Please check [ReorderOptions Object]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/) for request parameter.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [reorder the document pages with HTML representation](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlTransformPages).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="49" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"pageNumber":1,"newPosition":3}" \
-H "authorization: Bearer [Access Token]"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Reorder Document Pages for HTML Representation ###

{{< tabs tabTotal="6" tabID="28" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Reorder_Page_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Reorder_Page_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Reorder_Page_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Reorder_Page_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Reorder_Page_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Reorder_Page_HTML.py >}}

{{< /tab >}} {{< /tabs >}}

# Reorder Document Pages for Image Representation #

GroupDocs.Viewer Cloud can reorder document page for Image Representation. The API returns object with updated list of pages upon success. Please check [ReorderOptions Object]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/) for request body parameter.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [reorder document pages with Image representation](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageTransformPages).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="50" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/pages" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"pageNumber":1,"newPosition":3}" \
-H "authorization: Bearer [Access Token]"
 
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Reorder Document Pages for HTML Representation ###

{{< tabs tabTotal="6" tabID="29" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Reorder_Page_Image.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Reorder_Page_Image.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Reorder_Page_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Reorder_Page_Image.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Reorder_Page_Image.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Reorder_Page_Image.py >}}

{{< /tab >}} {{< /tabs >}}

# Remove Document Cache for HTML Pages #

You can remove the document HTML pages cache. The API returns an empty response with '204 No Content' status will be returned to confirm deletion.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [remove document cache for HTML pages](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlDeletePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="51" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "XX-XX"
-H "Content-Type: application/json" -X DELETE -d "{}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
Empty response with '204 No Content' status.
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Remove Document Cache for HTML Pages ###

{{< tabs tabTotal="6" tabID="30" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Remove_Document_Cache_for_HTML_Pages.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Remove_Document_Cache_for_HTML_Pages.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Remove_Document_Cache_for_HTML_Pages.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Remove_Document_Cache_for_HTML_Pages.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Remove_Document_Cache_for_HTML_Pages.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Remove_Document_Cache_for_HTML_Pages.py >}}

{{< /tab >}} {{< /tabs >}}

# Remove Document Cache for Page Images #

You can remove the document page images cache. The API returns an empty response with '204 No Content' status will be returned to confirm deletion.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [remove document cache for page Images](https://apireference.groupdocs.cloud/viewer/#!/Rendering/ImageDeletePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="52" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v  "XX-XX"
-H "Content-Type: application/json"
-X DELETE -d "{}"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
Empty response with '204 No Content' status.
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Remove Document Cache for Page Image ###

{{< tabs tabTotal="6" tabID="31" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Remove_Document_Cache_for_Image_Pages.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Remove_Document_Cache_for_Image_Pages.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Remove_Document_Cache_for_HTML_Image.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Remove_Document_Cache_for_Image_Pages.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Remove_Document_Cache_for_Image_Pages.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Remove_Document_Cache_for_Image_Pages.py >}}

{{< /tab >}} {{< /tabs >}}

# Specify Image Quality when Rendering PDF Documents as HTML #

You can set image quality of PDF document when rendering as HTML. The API returns an object which contains list of links to document pages.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Specify Image Quality when Rendering PDF Documents as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="53" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

 ```html
 curl -v "[http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages](http://api.groupdocs.cloud/v1/viewer/sample2.pdf/html/pages)" \
-X GET \
-data '{"pdfOptions": {"imageQuality": "High"}' \
-H"Content-Type: application/json" \
-H "authorization: Bearer "
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Specify Image Quality when Rendering PDF Documents as HTML ###

{{< tabs tabTotal="6" tabID="32" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Set_image_quality.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Set_image_quality.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Set_image_quality.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Set_image_quality.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Set_image_quality.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Set_image_quality.py >}}

{{< /tab >}} {{< /tabs >}}

# Exclude fonts when rendering as HTML #

You can prevent adding fonts in resultant document when rendering as HTML, to decrease the file size. The API returns an object which contains list of links to document pages.

{{< alert style="info" >}}
.ExcludeFontsList option allows to exclude specific fonts (that are commonly available on most of the devices). The example below shows how to prevent adding fonts into output HTML. Currently, it works only for Presentation documents. We are planning to extend support for this feature for all document types where it is applicable in the upcoming releases.--data '{"embedResources": true, "excludeFontsList": ["Arial"]}'
{{< /alert >}}

Resource

The following GroupDocs.Viewer Cloud REST API resource has been used to [Prevent Adding Fonts in document when rendering as Html](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="54" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
 curl -v "http://api.groupdocs.cloud/v1/viewer/one-page1.docx/html/pages"  \
-X GET -data '{"excludeFonts": true }' \
-H "Content-Type: application/json"  \
-H "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Exclude font when rendering as HTML ###

{{< tabs tabTotal="6" tabID="33" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Exclude_Fonts.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Exclude_Fonts.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Exclude_Fonts.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Exclude_Fonts.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Exclude_Fonts.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_Exclude_Fonts.py >}}

{{< /tab >}} {{< /tabs >}}

# Auto Fit column width rendering document as HTML #

You can set property to auto fit column with depending upon content when rendering document as Html. The API returns an object which contains list of links to document pages.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Auto Fit column width rendering document as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="55" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
 curl -v "[http://api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages](http://api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages)" \
-X GET -data '{"cellsOptions": {"textOverflowMode": "AutoFitColumn"}'  \
-H "Content-Type: application/json"  \
-H "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Autofit column width rendering document as HTML ###

{{< tabs tabTotal="6" tabID="34" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_text_Overflow_Mode.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_text_Overflow_Mode.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_text_Overflow_Mode.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_text_Overflow_Mode.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_text_Overflow_Mode.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_Exclude_Fonts.py >}}

{{< /tab >}} {{< /tabs >}}

# Rendering only Print Area in Excel document as HTML #

You can set property to render sections of the workshet(s) defined as [print area](https://support.office.com/en-us/article/set-or-clear-a-print-area-on-a-worksheet-27048af8-a321-416d-ba1b-e99ae2182a7e when rendering MS Excel document as Html. The API returns an object which contains list of links to document pages.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Rendering only Print Area in Excel document as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="56" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
 curl -v "[http://api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages](http://api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages)"  \
-X GET -data '{"cellsOptions": {"renderPrintAreaOnly": true, "renderHiddenColumns": true}}'  \
-H "Content-Type: application/json"  \
-H "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Rendering only Print Area in Excel document as HTML ###

{{< tabs tabTotal="6" tabID="35" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_render_PrintArea_Only.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_render_PrintArea_Only.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_render_PrintArea_Only.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_render_PrintArea_Only.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_render_PrintArea_Only.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_render_PrintArea_Only.py >}}

{{< /tab >}} {{< /tabs >}}

# Include/exclude hidden content in Excel documents as HTML #

You can set property to include/exclude hidden content when rendering MS Excel document as Html. The API returns an object which contains list of links to document pages.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [include/exclude hidden content in Excel documents as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="57" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
 curl -v "[http://api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages](http://api.groupdocs.cloud/v1/viewer/with-overflowed-text.xlsx/html/pages)"  \
-X GET -data '{"cellsOptions": {"renderHiddenRows": true, "renderHiddenColumns": true}}'  \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Include/exclude hidden content in Excel documents as HTML ###

{{< tabs tabTotal="6" tabID="36" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_render_Hidden_Rows.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_render_Hidden_Rows.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_render_Hidden_Rows.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_render_Hidden_Rows.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_render_Hidden_Rows.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_render_Hidden_Rows.py >}}

{{< /tab >}} {{< /tabs >}}

# Rendering PDF Documents into HTML with Setting (Default Font) #

Since the version 18.7, it is possible to set default font when rendering PDF document into HTML. This setting may be useful when you would like to specify which font should be used in case PDF document missing some font(s)

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Rendering PDF Document into Html](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetPagesFromUrl).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="58" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
# Set default font name when rendering PDF document as HTML

curl request POST \
url http://api.groupdocs.cloud/v1/viewer/missing-font.pdf/html/pages \
header 'authorization: [Access Token]' \
header 'content-type: application/json' \
data '{"defaultFontName": "Arial"}'

# Retrieve created page

curl request GET \
  --url http://api.groupdocs.cloud/v1/viewer/missing-font.pdf/html/pages/1 \
  --header 'authorization: [Access Token]'
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Rendering PDF Documents into HTML with Setting (Default Font) ###

{{< tabs tabTotal="6" tabID="37" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Render_PDF_DefaultFont.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Render_PDF_DefaultFont.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Render_PDF_DefaultFont.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Render_PDF_DefaultFont.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Render_PDF_DefaultFont.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Node_Render_PDF_DefaultFont.py >}}

{{< /tab >}} {{< /tabs >}}
