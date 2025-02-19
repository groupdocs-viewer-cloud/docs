---
id: "get-view-info-for-pdf-document"
url: "viewer/get-view-info-for-pdf-document"
title: "Get View Info for PDF Document"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
toc: True
---

GroupDocs.Viewer Cloud provides additional information for PDF documents when calling *Info* method.

Following example demonstrates how to retrieve view information for PDF document.

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
curl -v "https://api.groupdocs.cloud/v2.0/viewer/info" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{
  'FileInfo': {
    'FilePath': 'SampleFiles/sample.pdf'
  }
}"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "formatExtension": ".pdf",
  "format": "Portable Document Format File",
  "pages": [
    {
      "number": 1,
      "width": 0,
      "height": 0,
      "visible": true,
      "lines": []
    },
    {
      "number": 2,
      "width": 0,
      "height": 0,
      "visible": true,
      "lines": []
    }
  ],
  "attachments": [],
  "archiveViewInfo": null,
  "cadViewInfo": null,
  "projectManagementViewInfo": null,
  "outlookViewInfo": null,
  "pdfViewInfo": {
    "printingAllowed": true
  }
}

```
{{< /tab >}} {{< /tabs >}}

## SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example1-sdk">}}
{{< tab "C#" >}}
```cs
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

var configuration = new Configuration(MyClientId, MyClientSecret);
var apiInstance = new InfoApi(configuration);

var viewOptions = new ViewOptions
{
    FileInfo = new FileInfo
    {
        FilePath = "SampleFiles/sample.pdf"
    }
};

var response = apiInstance.GetInfo(new GetInfoRequest(viewOptions));
Console.WriteLine(" PrintingAllowed: " + response.PdfViewInfo.PrintingAllowed);
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

$apiInstance# new GroupDocs\Viewer\InfoApi($configuration);

$viewOptions = new Model\ViewOptions();

$fileInfo = new Model\FileInfo();
$fileInfo->setFilePath("SampleFiles/sample.pdf");
$viewOptions->setFileInfo($fileInfo);

$request = new Requests\GetInfoRequest($viewOptions);
$response = $apiInstance->getInfo($request);

echo " PrintingAllowed: ", $response->getPdfViewInfo()->getPrintingAllowed(), "\n";
```
{{< /tab >}} 
{{< tab "Java">}}
```java
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

Configuration configuration = new Configuration(MyClientId, MyClientSecret);
InfoApi apiInstance = new InfoApi(configuration);

FileInfo fileInfo = new FileInfo();
fileInfo.setFilePath("SampleFiles/sample.pdf");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);

InfoResult response = apiInstance.getInfo(new GetInfoRequest(viewOptions));

PdfViewInfo pdfViewInfo = response.getPdfViewInfo();

System.out.println(" PrintingAllowed: " + pdfViewInfo.getPrintingAllowed());
```
{{< /tab >}} 
{{< tab "Ruby">}}
```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'

$client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
$client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance = GroupDocsViewerCloud::InfoApi.from_keys($client_id, $client_secret)

viewOptions = GroupDocsViewerCloud::ViewOptions.new
viewOptions.file_info = GroupDocsViewerCloud::FileInfo.new
viewOptions.file_info.file_path = "SampleFiles/sample.pdf"
viewOptions.view_format = "HTML"

request = GroupDocsViewerCloud::GetInfoRequest.new(viewOptions)
response = infoApi.get_info(request)
puts(" PrintingAllowed: " + response.pdf_view_info.printing_allowed.to_s)
```
{{< /tab >}} 
{{< tab "Node.js">}}
```js
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer# require("groupdocs-viewer-cloud");

global.clientId = "XXXX-XXXX-XXXX-XXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
global.clientSecret = "XXXXXXXXXXXXXXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

global.infoApi = viewer_cloud.InfoApi.fromKeys(clientId, clientSecret);

let fileInfo = new viewer_cloud.FileInfo();
fileInfo.filePath = "SampleFiles/sample.pdf";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;

let request = new viewer_cloud.GetInfoRequest(viewOptions);
let response = await infoApi.getInfo(request);
console.log(" PrintingAllowed: " + response.pdfViewInfo.printingAllowed);
```
{{< /tab >}} 
{{< tab "Python">}}
```py
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud

client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance# groupdocs_viewer_cloud.InfoApi.from_keys(client_id, client_secret)

view_options = groupdocs_viewer_cloud.ViewOptions()
view_options.file_info = groupdocs_viewer_cloud.FileInfo()
view_options.file_info.file_path = "SampleFiles/sample.pdf"
view_options.view_format = "HTML"

request = groupdocs_viewer_cloud.GetInfoRequest(view_options)
response = apiInstance.get_info(request)
print(" PrintingAllowed: " + str(response.pdf_view_info.printing_allowed))
```
{{< /tab >}} 
{{< tab "Go">}}
```go
package RenderingPdfDocuments

import (
    "fmt"

    "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
    viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

// This example demonstrates how to retrieve view information for a PDF file
func GetInfoForPdfFile() {
    viewOptions := viewer.ViewOptions{
        FileInfo: &viewer.FileInfo{
            FilePath: "SampleFiles/sample.pdf",
        },
    }

    response, _, err := config.Client.InfoApi.GetInfo(config.Ctx, viewOptions)
    if err != nil {
        fmt.Printf("Exception while calling InfoApi: %v\n", err)
        return
    }

    fmt.Printf("PrintingAllowed: %v\n", response.PdfViewInfo.PrintingAllowed)
    fmt.Printf("GetInfoForPdfFile completed: %v pages\n", len(response.Pages))
}
```
{{< /tab >}}
{{< /tabs >}}
