---
id: "render-project-time-interval"
url: "viewer/render-project-time-interval"
title: "Render project time interval"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
toc: True
---

There is the possibility that you are required to render a part of the MS Project within the specified time interval. In that case, GroupDocs.Viewer Cloud allows rendering part of MS Project document according to specified StartDate and EndDate properties of ProjectManagementOptions class as shown in code samples below. When only one of these properties is set, rendering starts from the project's start date or ends on the project's end date correspondingly.

The following code samples show how to render MS Project document using StartDate and EndDate.

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
# First, get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to get document information
curl -v "https://api.groupdocs.cloud/v2.0/viewer/view" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
      "FilePath": "SampleFiles/sample.mpp"
    },
    "ViewFormat": "HTML",
    "RenderOptions": {
      "ProjectManagementOptions": {
        "StartDate": "2008-06-01",
        "EndDate": "2008-07-01"
      }
    }
  }'
```
{{< /tab >}}

{{< tab "Windows PowerShell" >}}
```powershell
# First, get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to get document information
curl.exe -v "https://api.groupdocs.cloud/v2.0/viewer/view" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{
    'FileInfo': {
        'FilePath': 'SampleFiles/sample.mpp'
    },
    'ViewFormat': 'HTML',
    'RenderOptions': {
        'ProjectManagementOptions': {
            'StartDate': '2008-06-01',
            'EndDate': '2008-07-01'
        }
    }
}"
```
{{< /tab >}}

{{< tab "Windows CMD" >}}
```cmd
:: First, get JSON Web Token
:: Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
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
  -d "{\"FileInfo\":{\"FilePath\":\"SampleFiles/sample.mpp\"},\"ViewFormat\":\"HTML\",\"RenderOptions\":{\"ProjectManagementOptions\":{\"StartDate\":\"2008-06-01\",\"EndDate\":\"2008-07-01\"}}}"
```
{{< /tab >}} {{< tab "Response" >}}
```json
{
  "pages": [
    {
      "number": 1,
      "resources": null,
      "path": "viewer/sample_mpp/sample_page_1.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_mpp/sample_page_1.html"
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
        FilePath = "SampleFiles/sample.mpp"
    },
    ViewFormat = ViewOptions.ViewFormatEnum.HTML,
    RenderOptions = new HtmlOptions
    {
        ProjectManagementOptions = new ProjectManagementOptions
        {
            StartDate = new DateTime(2008, 6, 1),
            EndDate = new DateTime(2008, 7, 1)
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

$viewOptions = new Model\ViewOptions();
$fileInfo = new Model\FileInfo();
$fileInfo->setFilePath("SampleFiles/sample.mpp");
$viewOptions->setFileInfo($fileInfo);
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_HTML);
$renderOptions = new Model\HtmlOptions();
$projectManagementOptions = new Model\ProjectManagementOptions();
$projectManagementOptions->setStartDate("2008/06/01");
$projectManagementOptions->setEndDate("2008/07/01");
$renderOptions->setProjectManagementOptions($projectManagementOptions);
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
fileInfo.setFilePath("SampleFiles/sample.mpp");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.HTML);
HtmlOptions renderOptions = new HtmlOptions();
ProjectManagementOptions projectManagementOptions = new ProjectManagementOptions();
projectManagementOptions.setStartDate(OffsetDateTime.parse("2008-06-01T00:00:00Z"));
projectManagementOptions.setEndDate(OffsetDateTime.parse("2008-07-01T00:00:00Z"));
renderOptions.setProjectManagementOptions(projectManagementOptions);
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
viewOptions.file_info.file_path = "SampleFiles/sample.mpp"
viewOptions.view_format = "HTML"
viewOptions.render_options = GroupDocsViewerCloud::HtmlOptions.new
viewOptions.render_options.project_management_options = GroupDocsViewerCloud::ProjectManagementOptions.new
viewOptions.render_options.project_management_options.start_date = "2008/06/01"
viewOptions.render_options.project_management_options.end_date = "2008/07/01"

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
fileInfo.filePath = "SampleFiles/sample.mpp";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;
viewOptions.viewFormat = viewer_cloud.ViewOptions.ViewFormatEnum.HTML;
viewOptions.renderOptions = new viewer_cloud.HtmlOptions();
viewOptions.renderOptions.projectManagementOptions = new viewer_cloud.ProjectManagementOptions();
viewOptions.renderOptions.projectManagementOptions.startDate = new Date(Date.UTC(2008, 6, 1, 0, 0, 0));
viewOptions.renderOptions.projectManagementOptions.endDate = new Date(Date.UTC(2008, 7, 1, 0, 0, 0));

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
view_options.file_info.file_path = "SampleFiles/sample.mpp"
view_options.view_format = "HTML"
view_options.render_options = groupdocs_viewer_cloud.HtmlOptions()
view_options.render_options.project_management_options = groupdocs_viewer_cloud.ProjectManagementOptions()
view_options.render_options.project_management_options.start_date = "2008/06/01"
view_options.render_options.project_management_options.end_date = "2008/07/01"

request = groupdocs_viewer_cloud.CreateViewRequest(view_options)
response = apiInstance.create_view(request)
```
{{< /tab >}} 
{{< tab "Go">}}
```go
package RenderingMsProjectDocuments

import (
    "fmt"
    "time"

    "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
    viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

// This example demonstrates how to render MS Project document using StartDate and EndDate
func RenderTimeInterval() {
    viewOptions := viewer.ViewOptions{
        FileInfo: &viewer.FileInfo{
            FilePath: "SampleFiles/sample.mpp",
        },
        ViewFormat: viewer.ViewFormatHtml,
        RenderOptions: &viewer.HtmlOptions{
            ProjectManagementOptions: &viewer.ProjectManagementOptions{
                StartDate: time.Date(2008, 6, 1, 0, 0, 0, 0, time.UTC),
                EndDate:   time.Date(2008, 7, 1, 0, 0, 0, 0, time.UTC),
            },
        },
    }

    response, _, err := config.Client.ViewApi.CreateView(config.Ctx, viewOptions)
    if err != nil {
        fmt.Printf("Exception: %v\n", err)
        return
    }

    fmt.Printf("RenderTimeInterval completed: %v pages\n", len(response.Pages))
}
```
{{< /tab >}}
{{< /tabs >}}
