---
id: "skip-rendering-of-empty-columns"
url: "viewer/skip-rendering-of-empty-columns"
title: "Skip rendering of empty columns"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

# Introduction #

Sometimes Excel document contains information at the beginning of the worksheet and after that, it contains some count of empty (blank) columns. In case, if the number of empty columns is considerably huge, the rendering time increases and hence, it affects the performance.

To skip rendering of empty columns GroupDocs.Viewer Cloud provides RenderEmptyColumns property, which allows omitting to render empty columns as shown in the sample below.

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
    'FilePath': 'SampleFiles/with_empty_column.xlsx'
  },
  'ViewFormat': 'HTML',
  'RenderOptions': {
    'SpreadsheetOptions': {
      'RenderEmptyColumns' : false
    }
  }
}"

```

{{< /tab >}} {{< tab tabNum="2" >}}

```html

{
  "pages": [
    {
      "number": 1,
      "resources": null,
      "path": "viewer/with_empty_column_xlsx/with_empty_column_page_1.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/with_empty_column_xlsx/with_empty_column_page_1.html"
    }
  ],
  "attachments": [],
  "file": null
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
        FilePath = "SampleFiles/with_empty_column.xlsx"
    },
    ViewFormat = ViewOptions.ViewFormatEnum.HTML,
    RenderOptions = new HtmlOptions
    {
        SpreadsheetOptions = new SpreadsheetOptions
        {
            RenderEmptyColumns = false
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
fileInfo.setFilePath("SampleFiles/with_empty_column.xlsx");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.HTML);
HtmlOptions renderOptions = new HtmlOptions();
SpreadsheetOptions spreadsheetOptions = new SpreadsheetOptions();
spreadsheetOptions.setRenderEmptyColumns(false);
renderOptions.setSpreadsheetOptions(spreadsheetOptions);
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
fileInfo.setFilePath("SampleFiles/with_empty_column.xlsx");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.HTML);
HtmlOptions renderOptions = new HtmlOptions();
SpreadsheetOptions spreadsheetOptions = new SpreadsheetOptions();
spreadsheetOptions.setRenderEmptyColumns(false);
renderOptions.setSpreadsheetOptions(spreadsheetOptions);
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
$fileInfo->setFilePath("SampleFiles/with_empty_column.xlsx");
$viewOptions->setFileInfo($fileInfo);
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_HTML);
$renderOptions = new Model\HtmlOptions();
$spreadsheetOptions = new Model\SpreadsheetOptions();
$spreadsheetOptions->setRenderEmptyColumns(false);
$renderOptions->setSpreadsheetOptions($spreadsheetOptions);
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
fileInfo.filePath = "SampleFiles/with_empty_column.xlsx";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;
viewOptions.viewFormat = viewer_cloud.ViewOptions.ViewFormatEnum.HTML;
viewOptions.renderOptions = new viewer_cloud.HtmlOptions();
viewOptions.renderOptions.spreadsheetOptions = new viewer_cloud.SpreadsheetOptions();
viewOptions.renderOptions.spreadsheetOptions.renderEmptyColumns = false;

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
view_options.file_info.file_path = "SampleFiles/with_empty_column.xlsx"
view_options.view_format = "HTML"
view_options.render_options = groupdocs_viewer_cloud.HtmlOptions()
view_options.render_options.spreadsheet_options = groupdocs_viewer_cloud.SpreadsheetOptions()
view_options.render_options.spreadsheet_options.render_empty_columns = False

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
viewOptions.file_info.file_path = "SampleFiles/with_empty_column.xlsx"
viewOptions.view_format = "HTML"
viewOptions.render_options = GroupDocsViewerCloud::HtmlOptions.new
viewOptions.render_options.spreadsheet_options = GroupDocsViewerCloud::SpreadsheetOptions.new
viewOptions.render_options.spreadsheet_options.render_empty_columns = false

request = GroupDocsViewerCloud::CreateViewRequest.new(viewOptions)
response = apiInstance.create_view(request)

```

{{< /tab >}} {{< /tabs >}}

