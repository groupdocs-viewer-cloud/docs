---
id: "minification-of-html-and-svg"
url: "viewer/minification-of-html-and-svg"
title: "Minification of HTML and SVG"
productName: "GroupDocs.Viewer Cloud"
weight: 2
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}






# Minification of HTML and SVG #

Since the version 18.2 GroupDocs.Viewer API, we have provide a new **EnableMinification **property of the **** object, that lets you get output content minified. Minification removes comments, extra white-spaces, and other unneeded characters without breaking the content structure. As a result page become smaller in size and loads faster. The following example demonstrates how to minify output content when creating cache.

**NOTE: **This feature is supported by all methods which accepts  objects.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages" \
-X POST \
-H "Content-Type: application/json" \
-d "{{enableMinification: true}}" \
-H "authorization: Bearer xxxxxxxxxxx"

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
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/
1/resources/font.woff"
        },
        {
          "name": "image.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/
1/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/
1/resources/styles.css"
        }
      ],
      "url": "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Document Pages Cache as Minified HTML ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Pages_Cache_Minified_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Pages_Cache_Minified_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Pages_Cache_Minified_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Pages_Cache_Minified_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Pages_Cache_Minified_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Pages_Cache_Minified_HTML.py >}}







