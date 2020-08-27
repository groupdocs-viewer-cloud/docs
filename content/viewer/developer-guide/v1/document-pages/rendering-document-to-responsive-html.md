---
id: "rendering-document-to-responsive-html"
url: "viewer/rendering-document-to-responsive-html"
title: "Rendering Document to Responsive HTML"
productName: "GroupDocs.Viewer Cloud"
weight: 3
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

GroupDocs.Viewer supports to render a document to responsive HTML. It provides a **EnableResponsiveRendering** property, that lets you get responsive output HTML. The following example demonstrates how to minify output content when creating cache.

**NOTE:** This feature is supported by all methods which accepts  objects.

Please note, that currently this option works for most document types, but there are few (listed below) that are not supported yet. We are planning to extend support for this option in coming releases.

**List of document types that do not support responsive rendering.**

|Format Name|Extension
|---|---
|Portable Document Format|PDF
|Microsoft Excel|XLS, XLSX, XLSM, XLSB
|Microsoft PowerPoint|PPT, PPTX, PPS, PPSX
|Microsoft Project|MPP, MPT
|OpenDocument Formats|ODS, ODP, OTP, OTS
|Plain Text File|TXT
|Comma-Separated Values|CSV
|HyperText Markup Language|HTML, MHT, MHTML
|Extensible Markup Language|XML
|XML Paper Specification|XPS
|Electronic publication|EPUB
|Mobipocket e-book format|MOBI
|LaTeX|TEX

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [get document page as responsive HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlGetPage).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1?embedResources#true&#x26;enableResponsiveRendering#true" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer xxxxxxxxxxx"

```

{{< /tab >}} {{< tab tabNum="2" >}}

```html

<!DOCTYPE html>

<html>

<head>

<meta http-equiv#"Content-Type" content#"text/html; charset#utf-8" />

<title>
</title>

<link rel#"stylesheet" type#"text/css"
href#"http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/styles.css" media#"all" />

<link rel#"stylesheet" type#"text/css"
href#"http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/styles.css" media#"all" />

</head>

<body>

<div class#"p1-uaUyVgCv-div p1-uaUyVgCv-page" style#"width:612pt;height:792pt; >}}
<div class#"p1-uaUyVgCv-div" style#"left:72pt; top:72pt; z-index:1; >}}
<span class#"p1-uaUyVgCv-span p1-uaUyVgCv-text1" style#"font-size:11pt; left:0pt; top:0pt; >}}This is test
</span>
</div>
<div class#"p1-uaUyVgCv-div" style#"z-i
ndex:1; >}}
<img class#"p1-uaUyVgCv-img" style#"left:512pt; top:346pt; width:100pt; height:100pt;" src#"http://api.groupdocs.cloud/v1/viewer/one-page.docx/html/pages/1/resources/image.png" />
</div>
</div>

</body>

</html>
```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Render Document Page as Responsive HTML ###

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Responsive_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Get_Responsive_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Responsive_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Responsive_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Responsive_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Responsive_HTML.py >}}

{{< /tab >}} {{< /tabs >}}
