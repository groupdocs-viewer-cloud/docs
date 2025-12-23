---
id: "render-with-custom-fonts"
url: "viewer/render-with-custom-fonts"
title: "Render with custom fonts"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
toc: True
---

GroupDocs.Viewer Cloud provides the feature to add custom font sources.

Following code snippet shows how to set custom font source.

## API Usage

There are steps that usage of GroupDocs.Viewer Cloud consists of:

1. Upload input document into cloud storage
1. Render document or get document info
1. Download rendered document from storage

Steps 1 and 3 are storage operations, please refer to this [File API documentation]({{< ref "viewer/developer-guide/working-with-files.md" >}}) for usage details.

[Swagger UI](https://apireference.groupdocs.cloud/viewer/) lets you call this REST API directly from the browser.

## cURL example

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}
```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v 'https://api.groupdocs.cloud/connect/token' \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Accept: application/json'

# cURL example to get document information
curl -v 'https://api.groupdocs.cloud/v2.0/viewer/view' \
  -X POST \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
      "FilePath": "SampleFiles/with_missing_font.odg"
    },
    "ViewFormat": "HTML",
    "FontsPath": "Fonts"
  }'
```
{{< /tab >}}

{{< tab "Windows PowerShell" >}}
```powershell
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl.exe -v 'https://api.groupdocs.cloud/connect/token' `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to get document information
curl.exe -v 'https://api.groupdocs.cloud/v2.0/viewer/view' `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{
    'FileInfo': {
      'FilePath': 'SampleFiles/with_missing_font.odg'
    },
    'ViewFormat': 'HTML',
    'FontsPath': 'Fonts'
  }"
```
{{< /tab >}}

{{< tab "Windows CMD" >}}
```cmd
:: First get JSON Web Token
:: Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

:: cURL example to get document information
curl -v "https://api.groupdocs.cloud/v2.0/viewer/view" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FileInfo\":{\"FilePath\":\"SampleFiles/with_missing_font.odg\"},\"ViewFormat\":\"HTML\",\"FontsPath\":\"Fonts\"}"
```
{{< /tab >}} {{< tab "Response" >}}
```json
{
  "pages": [
    {
      "number": 1,
      "resources": null,
      "path": "viewer/with_missing_font_odg/with_missing_font_page_1.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/with_missing_font_odg/with_missing_font_page_1.html"
    }
  ],
  "attachments": [],
  "file": null
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
var apiInstance = new ViewApi(configuration);

var viewOptions = new ViewOptions
{
    FileInfo = new FileInfo
    {
        FilePath = "SampleFiles/with_missing_font.odg"
    },
    ViewFormat = ViewOptions.ViewFormatEnum.HTML,

    // NOTE: Upload fonts to the folder using storage API before rendering
    FontsPath = "Fonts"
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

$viewOptions = new Model\ViewOptions();
$fileInfo = new Model\FileInfo();
$fileInfo->setFilePath("SampleFiles/with_missing_font.odg");
$viewOptions->setFileInfo($fileInfo);
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_HTML);

// NOTE: Upload fonts to the folder using storage API before rendering
$viewOptions->setFontsPath("Fonts");

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
fileInfo.setFilePath("SampleFiles/with_missing_font.odg");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.HTML);

// NOTE: Upload fonts to the folder using storage API before rendering
viewOptions.setFontsPath("Fonts");

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
viewOptions.file_info.file_path = "SampleFiles/with_missing_font.odg"
viewOptions.view_format = "HTML"
# NOTE: Upload fonts to the folder using storage API before rendering
viewOptions.fonts_path = "Fonts"

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
fileInfo.filePath = "SampleFiles/with_missing_font.odg";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;
viewOptions.viewFormat = viewer_cloud.ViewOptions.ViewFormatEnum.HTML;
// NOTE: Upload fonts to the folder using storage API before rendering
viewOptions.fontsPath = "Fonts";

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
view_options.file_info.file_path = "SampleFiles/with_missing_font.odg"
view_options.view_format = "HTML"
# NOTE: Upload fonts to the folder using storage API before rendering
view_options.fonts_path = "Fonts"

request = groupdocs_viewer_cloud.CreateViewRequest(view_options)
response = apiInstance.create_view(request)
```
{{< /tab >}} 
{{< tab "Go">}}
```go
package CommonRenderingOptions

import (
	"fmt"

	"github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
	viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

// This example demonstrates how to set a custom font source when rendering documents
func RenderWithCustomFonts() {
	viewOptions := viewer.ViewOptions{
		FileInfo: &viewer.FileInfo{
			FilePath: "SampleFiles/with_missing_font.odg",
		},
		ViewFormat: viewer.ViewFormatHtml,
		FontsPath:  "Fonts", // NOTE: Upload fonts to the folder using storage API before rendering
	}

	response, _, err := config.Client.ViewApi.CreateView(config.Ctx, viewOptions)
	if err != nil {
		fmt.Printf("Exception: %v\n", err)
		return
	}

	fmt.Printf("RenderWithCustomFonts completed: %v pages\n", len(response.Pages))
}

```
{{< /tab >}}
{{< /tabs >}}
