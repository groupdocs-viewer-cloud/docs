---
id: "rendering-ms-project-document"
url: "viewer/rendering-ms-project-document"
title: "Rendering MS Project Document"
productName: "GroupDocs.Viewer Cloud"
weight: 6
description: ""
keywords: ""
toc: True
---

{{< alert style="info" >}}
Note: The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

Starting from GroupDocs.Viewer Cloud 18.2 two new options have been added which allows to adjust Page Size and Time Unit when rendering MS Project documents. By default GroupDocs.Viewer API tries to find optimal output size and time unit, depending on the projects overall length, depending on the projects overall length. In case you need to set your own page size or time unit, you can specify **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** which provides two options **PageSize** and **TimeUnit**.  Time unit refers to smallest unit (days, third of a month or month) used in timescale bar, when the TimeUnit = "Days" is set you will get the most detailed view of your tasks and opposite, when TimeUnit = "Month" is set you will get more general representation of tasks. This example demonstrates how to create pages cache as HTML with provided **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}).**

**NOTE:** [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

### cURL example

{{< tabs "example1">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages" \
-X POST \
-H "Content-Type: application/json" \
-d "{"projectOptions": {"pageSize": "A0","timeUnit": "unknown"}}" \
-H "authorization: Bearer [Access Token]"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
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

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).


{{< tabs "example1-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Project_Page_Cache_HTML.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Project_Page_Cache_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Project_Page_Cache_HTML.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Project_Page_Cache_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Project_Page_Cache_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Project_Page_Cache_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Rendering MS Project Document Pages as Image

Starting from GroupDocs.Viewer Cloud 18.2 two new options have been added which allows to adjust Page Size and Time Unit when rendering MS Project documents. By default GroupDocs.Viewer API tries to find optimal output size and time unit, depending on the projects overall length, depending on the projects overall length. In case you need to set your own page size or time unit, you can specify **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** which provides two options **PageSize** and **TimeUnit**.  Time unit refers to smallest unit (days, third of a month or month) used in timescale bar, when the TimeUnit = "Days" is set you will get the most detailed view of your tasks and opposite, when TimeUnit = "Month" is set you will get more general representation of tasks. This example demonstrates how to create pages cache as Image with provided **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}).**

**NOTE: [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

### cURL example

{{< tabs "example2">}}
{{< tab "Request" >}}
```bash
curl -v "https://api.groupdocs.cloud/v1/viewer/sample.mpp/image/pages" \
-X POST \
-H "Content-Type: application/json" \
-d "{"projectOptions": {"pageSize": "A0","timeUnit": "unknown"}}" \
-H "authorization: Bearer [Access Token]"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
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

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example2-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Project_Page_Cache_Image.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Create_Project_Page_Cache_Image.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Project_Page_Cache_Image.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Project_Page_Cache_Image.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Project_Page_Cache_Image.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Project_Page_Cache_Image.py >}}
{{< /tab >}} 
{{< /tabs >}}

## Render MS Project documents by specifying Project Start and End dates

Since the version 18.11 GroupDocs.Viewer Cloud API allows to render part of MS Project  document according to specified StartDate and EndDate properties of [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) class as shown in examples below. When only one of this properties is set, rendering starts from project start or to end date correspondingly.

**NOTE: [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

![](/viewer/images/StartEndDate.png)

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

### cURL example

{{< tabs "example3">}}
{{< tab "Request" >}}
```bash
curl --request POST \
  --url https://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages \
  --header 'authorization: Bearer [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"projectOptions": {"startDate": "07/01/2008","endDate": "07/31/2008"}}'
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "fileName": "sample.mpp",
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "styles.css",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1/resources/styles.css"
        },
        {
          "name": "image.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1/resources/image.png"
        },
        {
          "name": "image1.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1/resources/image1.png"
        },
        {
          "name": "image2.png",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1/resources/image2.png"
        },
        {
          "name": "graphics.svg",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1/resources/graphics.svg"
        },
        {
          "name": "font.ttf",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1/resources/font.ttf"
        },
        {
          "name": "font1.ttf",
          "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1/resources/font1.ttf"
        }
      ],
      "url": "http://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages/1"
    }
  ]
}
```
{{< /tab >}} {{< /tabs >}}

### SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example3-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Render_Project_DateRange_HTML.cs >}}
{{< /tab >}} 
{{< tab "PHP">}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Render_Project_DateRange_HTML.php >}}
{{< /tab >}} 
{{< tab "Java">}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Render_Project_DateRange_HTML.java >}}
{{< /tab >}} 
{{< tab "Ruby">}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Render_Project_DateRange_HTML.rb >}}
{{< /tab >}} 
{{< tab "Node.js">}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Render_Project_DateRanges_HTML.js >}}
{{< /tab >}} 
{{< tab "Python">}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Render_Project_DateRange_HTML.py >}}
{{< /tab >}} 
{{< /tabs >}}
