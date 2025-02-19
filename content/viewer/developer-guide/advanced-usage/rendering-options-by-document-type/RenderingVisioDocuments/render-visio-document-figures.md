---
id: "render-visio-document-figures"
url: "viewer/render-visio-document-figures"
title: "Render Visio Document Figures"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
toc: True
---

When you are converting Visio files, you can choose what you want to render: Visio scheme pages or figures of Visio scheme. If Visio scheme does not contain pages - only figures will be rendered.

![](/viewer/images/figures-in-visio.jpg)

To force render Visio figures please set RenderFiguresOnly property to true in VisioRenderingOptions. You can set width of each figure, height will be calculated by proportions automatically.

## API Usage

There are steps that usage of GroupDocs.Viewer Cloud consists of:

1. Upload input document into cloud storage
1. Render document or get document info
1. Download rendered document from storage

Steps 1 and 3 are storage operations, please refer to this [File API documentation]({{< ref "viewer/developer-guide/working-with-files.md" >}}) for usage details.

[Swagger UI](https://apireference.groupdocs.cloud/viewer/) lets you call this REST API directly from the browser.

## cURL example

{{< tabs "example1">}}
{{< tab "Request" >}}
```bash

# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type=client_credentials&client_id=xxxx&client_secret=xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

# cURL example to get document information
curl -v "https://api.groupdocs.cloud/v2.0/viewer/view" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{
  'FileInfo': {
    'FilePath': 'SampleFiles/sample.vssx'
  },
  'ViewFormat': 'PNG',
  'RenderOptions': {
    'VisioRenderingOptions': {
      'RenderFiguresOnly' : true,
      'FigureWidth' : 250
    }
  }
}"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "pages": [
    {
      "number": 1,
      "resources": null,
      "path": "viewer/sample_vssx/sample_page_1.png",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_vssx/sample_page_1.png"
    }
  ],
  "attachments": [],
  "file": null
}

```
{{< /tab >}} {{< /tabs >}}

## SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### SDK Examples ###

{{< tabs "example1-sdk">}}
{{< tab "C#" >}}
```cs
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

var configuration = new Configuration(MyClientId, MyClientSecret);
var apiInstance = new ViewApi(configuration);

var viewOptions = new ViewOptions
{
    FileInfo = new FileInfo
    {
        FilePath = "SampleFiles/sample.vssx"
    },
    ViewFormat = ViewOptions.ViewFormatEnum.PNG,
    RenderOptions = new ImageOptions()
    {
        VisioRenderingOptions = new VisioRenderingOptions
        {
            RenderFiguresOnly = true,
            FigureWidth = 250
        }
    }
};

var response = apiInstance.CreateView(new CreateViewRequest(viewOptions));
```
{{< /tab >}} 
{{< tab "PHP">}}
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

$fileInfo = new Model\FileInfo();
$fileInfo->setFilePath("SampleFiles/sample.vssx");
$viewOptions->setFileInfo($fileInfo);
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_PNG);
$renderOptions = new Model\ImageOptions();
$visioRenderingOptions = new Model\VisioRenderingOptions();
$visioRenderingOptions->setRenderFiguresOnly(true);
$visioRenderingOptions->setFigureWidth(250);
$renderOptions->setVisioRenderingOptions($visioRenderingOptions);
$viewOptions->setRenderOptions($renderOptions);

$request = new Requests\CreateViewRequest($viewOptions);
$response = $apiInstance->createView($request);
```
{{< /tab >}} 
{{< tab "Java">}}
```java
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

Configuration configuration = new Configuration(MyClientId, MyClientSecret);
ViewApi apiInstance = new ViewApi(configuration);

FileInfo fileInfo = new FileInfo();
fileInfo.setFilePath("SampleFiles/sample.vssx");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.PNG);
ImageOptions renderOptions = new ImageOptions();            
VisioRenderingOptions visioRenderingOptions = new VisioRenderingOptions();
visioRenderingOptions.setRenderFiguresOnly(true);
visioRenderingOptions.setFigureWidth(250);
renderOptions.setVisioRenderingOptions(visioRenderingOptions);
viewOptions.setRenderOptions(renderOptions);

ViewResult response = apiInstance.createView(new CreateViewRequest(viewOptions));
```
{{< /tab >}} 
{{< tab "Ruby">}}
```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'

$client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
$client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance = GroupDocsViewerCloud::ViewApi.from_keys($client_id, $client_secret)

viewOptions = GroupDocsViewerCloud::ViewOptions.new
viewOptions.file_info = GroupDocsViewerCloud::FileInfo.new
viewOptions.file_info.file_path = "SampleFiles/sample.vssx"
viewOptions.view_format = "PNG"
viewOptions.render_options = GroupDocsViewerCloud::ImageOptions.new
viewOptions.render_options.visio_rendering_options = GroupDocsViewerCloud::VisioRenderingOptions.new
viewOptions.render_options.visio_rendering_options.render_figures_only = true
viewOptions.render_options.visio_rendering_options.figure_width = 250

request = GroupDocsViewerCloud::CreateViewRequest.new(viewOptions)
response = apiInstance.create_view(request)
```
{{< /tab >}} 
{{< tab "Node.js">}}
```js
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer# require("groupdocs-viewer-cloud");

global.clientId = "XXXX-XXXX-XXXX-XXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
global.clientSecret = "XXXXXXXXXXXXXXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

global.viewApi = viewer_cloud.ViewApi.fromKeys(clientId, clientSecret);

let fileInfo = new viewer_cloud.FileInfo();
fileInfo.filePath = "SampleFiles/sample.vssx";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;
viewOptions.viewFormat = viewer_cloud.ViewOptions.ViewFormatEnum.PNG;
viewOptions.renderOptions = new viewer_cloud.ImageOptions();
viewOptions.renderOptions.visioRenderingOptions = new viewer_cloud.VisioRenderingOptions();
viewOptions.renderOptions.visioRenderingOptions.renderFiguresOnly = true;
viewOptions.renderOptions.visioRenderingOptions.figureWidth = 250;

let request = new viewer_cloud.CreateViewRequest(viewOptions);
let response = await viewApi.createView(request);
```
{{< /tab >}} 
{{< tab "Python">}}
```py
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud

client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance = groupdocs_viewer_cloud.ViewApi.from_keys(client_id, client_secret)

view_options = groupdocs_viewer_cloud.ViewOptions()
view_options.file_info = groupdocs_viewer_cloud.FileInfo()
view_options.file_info.file_path = "SampleFiles/sample.vssx"
view_options.view_format = "PNG"
view_options.render_options = groupdocs_viewer_cloud.ImageOptions()
view_options.render_options.visio_rendering_options = groupdocs_viewer_cloud.VisioRenderingOptions()
view_options.render_options.visio_rendering_options.render_figures_only = True
view_options.render_options.visio_rendering_options.figure_width = 250

request = groupdocs_viewer_cloud.CreateViewRequest(view_options)
response = apiInstance.create_view(request)
```
{{< /tab >}} 
{{< tab "Go">}}
```go
package RenderingVisioDocuments

import (
    "fmt"

    "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
    viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

// This example demonstrates how to render Visio documents figures
func RenderVisioDocumentFigures() {
    viewOptions := viewer.ViewOptions{
        FileInfo: &viewer.FileInfo{
            FilePath: "SampleFiles/sample.vssx",
        },
        ViewFormat: viewer.ViewFormatPng,
        RenderOptions: &viewer.ImageOptions{
            VisioRenderingOptions: &viewer.VisioRenderingOptions{
                RenderFiguresOnly: true,
                FigureWidth:       250,
            },
        },
    }

    response, _, err := config.Client.ViewApi.CreateView(config.Ctx, viewOptions)
    if err != nil {
        fmt.Printf("Exception: %v\n", err)
        return
    }

    fmt.Printf("RenderVisioDocumentFigures completed: %v pages\n", len(response.Pages))
}
```
{{< /tab >}}
{{< /tabs >}}
