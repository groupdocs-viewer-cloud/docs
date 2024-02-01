---
id: "pdf-viewer-optimization-options"
url: "viewer/pdf-viewer-optimization-options"
title: "PDF Viewer - Optimization options"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

# Introduction #

GroupDocs.Viewer Cloud allows you to optimize the output PDF file for a web browser or to reduce the file size by optimizing resources. Optimization for a web allows a browser to display the first pages of a PDF file when you open the  document, instead of waiting for the entire file to download. Resource optimization allows you to reduce the size of the output PDF file. While optimizing, GroupDocs.Viewer may reduce the image size or quality, remove notes or form fields, remove objects, fonts, or personal information from a document, and so on.
See [PdfOptimizationOptions]({{< ref "viewer/developer-guide/data-structures/pdfoptimizationoptions.md" >}}) for more information.

The following code sample shows how to adjust image quality in the output PDF document.

## API Usage ##

There are steps that usage of GroupDocs.Viewer Cloud consists of:

1. Upload input document into cloud storage
1. Render document or get document info
1. Download rendered document from storage

Steps 1 and 3 are storage operations, please refer to this [File API documentation]({{< ref "viewer/developer-guide/working-with-files.md" >}}) for usage details.

[Swagger UI](https://apireference.groupdocs.cloud/viewer/) lets you call this REST API directly from the browser.

## cURL REST Example ##

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html

* First get JSON Web Token
* Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type=client_credentials&client_id=xxxx&client_secret=xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

* cURL example to get document information
curl -v "https://api.groupdocs.cloud/v2.0/viewer/view" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{
  'FileInfo': {
    'FilePath': 'SampleFiles/with_jpg_image.pptx'
  },
  'ViewFormat': 'PDF',
  'RenderOptions': {
     'PdfOptimizationOptions': {
        'CompressImages': true,
        'ImageQuality': 80
      }
  }
}"

```

{{< /tab >}} {{< tab tabNum="2" >}}

```html

{
  "pages": null,
  "attachments": [],
  "file": {
    "path": "viewer/with_jpg_image_pptx/with_jpg_image.pdf",
    "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/with_jpg_image_pptx/with_jpg_image.pdf"
  }
}

```

{{< /tab >}} {{< /tabs >}}

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### SDK Examples ###

{{< tabs tabTotal="7" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" tabName7="Android" >}} {{< tab tabNum="1" >}}

```csharp

// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

var configuration = new Configuration(MyClientId, MyClientSecret);
var apiInstance = new ViewApi(configuration);

var viewOptions = new ViewOptions
{
    FileInfo = new FileInfo
    {
        FilePath = "SampleFiles/with_jpg_image.pptx"
    },
    ViewFormat = ViewOptions.ViewFormatEnum.PDF,
    RenderOptions = new PdfOptions
    {
        PdfOptimizationOptions = new PdfOptimizationOptions {
          CompressImages = true,
          ImageQuality = 80
        }
    }
};

var response = apiInstance.CreateView(new CreateViewRequest(viewOptions));

```

{{< /tab >}} {{< tab tabNum="2" >}}

```java

// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

Configuration configuration = new Configuration(MyClientId, MyClientSecret);
ViewApi apiInstance = new ViewApi(configuration);

FileInfo fileInfo = new FileInfo();
fileInfo.setFilePath("SampleFiles/with_jpg_image.pptx");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.PDF);
PdfOptions renderOptions = new PdfOptions();
PdfOptimizationOptions pdfOptimizationOptions = new PdfOptimizationOptions();
pdfOptimizationOptions.setCompressImages(true);
pdfOptimizationOptions.setImageQuality(80);
renderOptions.setPdfOptimizationOptions(pdfOptimizationOptions);
viewOptions.setRenderOptions(renderOptions);

ViewResult response = apiInstance.createView(new CreateViewRequest(viewOptions));

```

{{< /tab >}}  {{< tab tabNum="7" >}}

```java

// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

Configuration configuration = new Configuration(MyClientId, MyClientSecret);
ViewApi apiInstance = new ViewApi(configuration);

FileInfo fileInfo = new FileInfo();
fileInfo.setFilePath("SampleFiles/with_jpg_image.pptx");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.PDF);
PdfOptions renderOptions = new PdfOptions();
PdfOptimizationOptions pdfOptimizationOptions = new PdfOptimizationOptions();
pdfOptimizationOptions.setCompressImages(true);
pdfOptimizationOptions.setImageQuality(80);
renderOptions.setPdfOptimizationOptions(pdfOptimizationOptions);
viewOptions.setRenderOptions(renderOptions);

ViewResult response = apiInstance.createView(new CreateViewRequest(viewOptions));

```

{{< /tab >}} {{< tab tabNum="3" >}}

```php

// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php-samples
use GroupDocs\Viewer\Model;
use GroupDocs\Viewer\Model\Requests;

$ClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
$ClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

$configuration = new GroupDocs\Viewer\Configuration();
$configuration->setAppSid($ClientId);
$configuration->setAppKey($ClientSecret);

$apiInstance = new GroupDocs\Viewer\ViewApi($configuration);

$viewOptions = new Model\ViewOptions();
$fileInfo = new Model\FileInfo();
$fileInfo->setFilePath("SampleFiles/with_jpg_image.pptx");
$viewOptions->setFileInfo($fileInfo);
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_PDF);
$renderOptions = new Model\PdfOptions();

$pdfOptimizationOptions = new Model\PdfOptimizationOptions();
$pdfOptimizationOptions->setCompressImages(true);
$pdfOptimizationOptions->setImageQuality(80);
$renderOptions->setPdfOptimizationOptions($pdfOptimizationOptions);

$viewOptions->setRenderOptions($renderOptions);

$request = new Requests\CreateViewRequest($viewOptions);
$response = $apiInstance->createView($request);

```

{{< /tab >}} {{< tab tabNum="4" >}}

```javascript

// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer# require("groupdocs-viewer-cloud");

global.clientId = "XXXX-XXXX-XXXX-XXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
global.clientSecret = "XXXXXXXXXXXXXXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

global.viewApi = viewer_cloud.ViewApi.fromKeys(clientId, clientSecret);

let fileInfo = new viewer_cloud.FileInfo();
fileInfo.filePath = "SampleFiles/with_jpg_image.pptx";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;
viewOptions.viewFormat = viewer_cloud.ViewOptions.ViewFormatEnum.PDF;
viewOptions.renderOptions = new viewer_cloud.PdfOptions();
viewOptions.renderOptions.pdfOptimizationOptions = new viewer_cloud.PdfOptimizationOptions();
viewOptions.renderOptions.pdfOptimizationOptions.compressImages = true;
viewOptions.renderOptions.pdfOptimizationOptions.imageQuality = 80;

let request = new viewer_cloud.CreateViewRequest(viewOptions);
let response = await viewApi.createView(request);

```

{{< /tab >}} {{< tab tabNum="5" >}}

```python

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud

client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance = groupdocs_viewer_cloud.ViewApi.from_keys(client_id, client_secret)

view_options = groupdocs_viewer_cloud.ViewOptions()
view_options.file_info = groupdocs_viewer_cloud.FileInfo()
view_options.file_info.file_path = "SampleFiles/with_jpg_image.pptx"
view_options.view_format = "PDF"
view_options.render_options = groupdocs_viewer_cloud.PdfOptions()
viewOptions.render_options.pdf_optimization_options = new groupdocs_viewer_cloud.PdfOptimizationOptions()
viewOptions.render_options.pdf_optimization_options.compress_images = True
viewOptions.render_options.pdf_optimization_options.image_quality = 80

request = groupdocs_viewer_cloud.CreateViewRequest(view_options)
response = apiInstance.create_view(request)

```

{{< /tab >}} {{< tab tabNum="6" >}}

```ruby

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'

$client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
$client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance = GroupDocsViewerCloud::ViewApi.from_keys($client_id, $client_secret)

viewOptions = GroupDocsViewerCloud::ViewOptions.new
viewOptions.file_info = GroupDocsViewerCloud::FileInfo.new
viewOptions.file_info.file_path = "SampleFiles/with_jpg_image.pptx"
viewOptions.view_format = "PDF"
viewOptions.render_options = GroupDocsViewerCloud::PdfOptions.new
viewOptions.render_options.pdf_optimization_options = GroupDocsViewerCloud::PdfOptimizationOptions.new
viewOptions.render_options.pdf_optimization_options.compress_images = true
viewOptions.render_options.pdf_optimization_options.image_quality = 80

request = GroupDocsViewerCloud::CreateViewRequest.new(viewOptions)
response = apiInstance.create_view(request)

```

{{< /tab >}} {{< /tabs >}}
