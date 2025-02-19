---
id: "get-document-information"
url: "viewer/get-document-information"
title: "Get Document Information"
productName: "GroupDocs.Viewer Cloud"
weight: 8
description: ""
keywords: ""
toc: True
---

This REST API allows to obtain basic information about the document and it's properties.

It returns *[InfoResult]({{< ref "viewer/developer-guide/data-structures/inforesult.md" >}})* data structure, which contains the list of properties:

* Document file format
* Pages count, size and visibility
* Text coordinates
* Attachments count and names
* other properties, by document type

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information](https://apireference.groupdocs.cloud/viewer/#/Viewer/GetInfo).

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
         'FilePath': 'SampleFiles/sample.docx'
      },
      'ViewFormat': 'JPG'
}"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
{
  "formatExtension": ".docx",
  "format": "Microsoft Word Open XML Document",
  "pages": [
    {
      "number": 1,
      "width": 595,
      "height": 841,
      "visible": true,
      "lines": []
    },
    {
      "number": 2,
      "width": 595,
      "height": 841,
      "visible": true,
      "lines": []
    },
    {
      "number": 3,
      "width": 595,
      "height": 841,
      "visible": true,
      "lines": []
    }
  ],
  "attachments": [],
  "archiveViewInfo": null,
  "cadViewInfo": null,
  "projectManagementViewInfo": null,
  "outlookViewInfo": null,
  "pdfViewInfo": null
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
        FilePath = "SampleFiles/sample.docx"
    }
};
var response = apiInstance.GetInfo(new GetInfoRequest(viewOptions));
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
$fileInfo->setFilePath("SampleFiles/sample.docx");
$viewOptions->setFileInfo($fileInfo);
$request = new Requests\GetInfoRequest($viewOptions);
$response = $apiInstance->getInfo($request);
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
fileInfo.setFilePath("SampleFiles/sample.docx");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);
InfoResult response = apiInstance.getInfo(new GetInfoRequest(viewOptions));
```
{{< /tab >}} 
{{< tab "Ruby">}}
```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'

$client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
$client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

infoApi = GroupDocsViewerCloud::InfoApi.from_keys($client_id, $client_secret)

viewOptions = GroupDocsViewerCloud::ViewOptions.new
viewOptions.file_info = GroupDocsViewerCloud::FileInfo.new
viewOptions.file_info.file_path = "SampleFiles/sample.docx"
request = GroupDocsViewerCloud::GetInfoRequest.new(viewOptions)
response = infoApi.get_info(request)
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
fileInfo.filePath = "SampleFiles/sample.docx";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;
let request = new viewer_cloud.GetInfoRequest(viewOptions);
let response = await infoApi.getInfo(request);
```
{{< /tab >}} 
{{< tab "Python">}}
```py
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud

client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

infoApi = groupdocs_viewer_cloud.InfoApi.from_keys(client_id, client_secret)

view_options = groupdocs_viewer_cloud.ViewOptions()
view_options.file_info = groupdocs_viewer_cloud.FileInfo()
view_options.file_info.file_path = "SampleFiles/sample.docx"
request = groupdocs_viewer_cloud.GetInfoRequest(view_options)
result = infoApi.get_info(request)
```
{{< /tab >}} 
{{< tab "Go">}}
```go
package basicUsage

import (
	"fmt"

	"github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
	viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

func GetDocumentInformation() {

	opts := viewer.ViewOptions{
		FileInfo: &viewer.FileInfo{
			FilePath: "SampleFiles/sample.docx",
		},
	}

	info, _, err := config.Client.InfoApi.GetInfo(config.Ctx, opts)

	if err != nil {
		fmt.Printf("GetInfo error: %v\n", err)
		return
	}

	fmt.Printf("Page count: %v\n", len(info.Pages))
}

```
{{< /tab >}}
{{< /tabs >}}
