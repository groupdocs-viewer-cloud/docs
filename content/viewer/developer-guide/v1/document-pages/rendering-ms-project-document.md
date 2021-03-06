---
id: "rendering-ms-project-document"
url: "viewer/rendering-ms-project-document"
title: "Rendering MS Project Document"
productName: "GroupDocs.Viewer Cloud"
weight: 6
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

Starting from GroupDocs.Viewer Cloud 18.2 two new options have been added which allows to adjust Page Size and Time Unit when rendering MS Project documents. By default GroupDocs.Viewer API tries to find optimal output size and time unit, depending on the projects overall length, depending on the projects overall length. In case you need to set your own page size or time unit, you can specify **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** which provides two options **PageSize** and **TimeUnit**.  Time unit refers to smallest unit (days, third of a month or month) used in timescale bar, when the TimeUnit = "Days" is set you will get the most detailed view of your tasks and opposite, when TimeUnit = "Month" is set you will get more general representation of tasks. This example demonstrates how to create pages cache as HTML with provided **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}).**

**NOTE:** [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

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

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

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

Starting from GroupDocs.Viewer Cloud 18.2 two new options have been added which allows to adjust Page Size and Time Unit when rendering MS Project documents. By default GroupDocs.Viewer API tries to find optimal output size and time unit, depending on the projects overall length, depending on the projects overall length. In case you need to set your own page size or time unit, you can specify **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** which provides two options **PageSize** and **TimeUnit**.  Time unit refers to smallest unit (days, third of a month or month) used in timescale bar, when the TimeUnit = "Days" is set you will get the most detailed view of your tasks and opposite, when TimeUnit = "Month" is set you will get more general representation of tasks. This example demonstrates how to create pages cache as Image with provided **[ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}).**

**NOTE: [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

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

{{< tabs tabTotal="6" tabID="11" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

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

# Render MS Project documents by specifying Project Start and End dates #

Since the version 18.11 GroupDocs.Viewer Cloud API allows to render part of MS Project  document according to specified StartDate and EndDate properties of [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) class as shown in examples below. When only one of this properties is set, rendering starts from project start or to end date correspondingly.

**NOTE: [ProjectOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}})** is supported by all methods which accepts [DocumentInfoOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [ImageOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}), [HtmlOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) and [PdfFileOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) objects.

![](viewer/images/StartEndDate.png)

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [create document cache as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="3" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl --request POST \
  --url https://api.groupdocs.cloud/v1/viewer/sample.mpp/html/pages \
  --header 'authorization: Bearer [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"projectOptions": {"startDate": "07/01/2008","endDate": "07/31/2008"}}'
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
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

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Pages Cache as Image of MS Project Document by specifying Project Start and End dates ###

{{< tabs tabTotal="6" tabID="12" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Render_Project_DateRange_HTML.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Render_Project_DateRange_HTML.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Render_Project_DateRange_HTML.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Render_Project_DateRange_HTML.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Render_Project_DateRanges_HTML.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Render_Project_DateRange_HTML.py >}}

{{< /tab >}} {{< /tabs >}}
