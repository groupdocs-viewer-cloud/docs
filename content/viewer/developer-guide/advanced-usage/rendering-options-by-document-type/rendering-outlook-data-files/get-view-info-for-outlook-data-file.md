---
id: "get-view-info-for-outlook-data-file"
url: "viewer/get-view-info-for-outlook-data-file"
title: "Get View Info for Outlook Data File"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

# Introduction #

GroupDocs.Viewer Cloud provides additional information for Outlook Data Files when calling *Info* method.

Following example demonstrates how to retrieve view information for Outlook Data File.

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
curl -v "https://api.groupdocs.cloud/v2.0/viewer/info" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{
  'FileInfo': {
    'FilePath': 'SampleFiles/sample.ost'
  }
}"

```

{{< /tab >}} {{< tab tabNum="2" >}}

```html

{
  "formatExtension": ".ost",
  "format": "Outlook Offline Data File",
  "pages": [
    {
      "number": 1,
      "width": 0,
      "height": 0,
      "visible": true,
      "lines": []
    }
  ],
  "attachments": [
    {
      "name": "(Inbox)0.msg"
    },
    {
      "name": "(Inbox)1.msg"
    },
    {
      "name": "(Inbox)2.msg"
    }
  ],
  "archiveViewInfo": null,
  "cadViewInfo": null,
  "projectManagementViewInfo": null,
  "outlookViewInfo": {
    "folders": [
      "Inbox",
      "Recycle",
      "Outbox",
      "Sent",
      "Sync Issues (This computer only)",
      "Sync Issues"
    ]
  },
  "pdfViewInfo": null
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
var apiInstance = new InfoApi(configuration);

var viewOptions = new ViewOptions
{
    FileInfo = new FileInfo
    {
        FilePath = "SampleFiles/sample.ost"
    }
};

var response = apiInstance.GetInfo(new GetInfoRequest(viewOptions));
Console.WriteLine(" Folders count: " + response.OutlookViewInfo.Folders.Count);

```

{{< /tab >}} {{< tab tabNum="2" >}}

```java

// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

Configuration configuration = new Configuration(MyClientId, MyClientSecret);
InfoApi apiInstance = new InfoApi(configuration);

FileInfo fileInfo = new FileInfo();
fileInfo.setFilePath("SampleFiles/sample.ost");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);

InfoResult response = apiInstance.getInfo(new GetInfoRequest(viewOptions));

OutlookViewInfo outlookViewInfo = response.getOutlookViewInfo();

System.out.println(" Folders count: " + outlookViewInfo.getFolders().size());

```

{{< /tab >}} {{< tab tabNum="7" >}}

```java

// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

Configuration configuration = new Configuration(MyClientId, MyClientSecret);
InfoApi apiInstance = new InfoApi(configuration);

FileInfo fileInfo = new FileInfo();
fileInfo.setFilePath("SampleFiles/sample.ost");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);

InfoResult response = apiInstance.getInfo(new GetInfoRequest(viewOptions));

OutlookViewInfo outlookViewInfo = response.getOutlookViewInfo();

System.out.println(" Folders count: " + outlookViewInfo.getFolders().size());

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

$apiInstance# new GroupDocs\Viewer\InfoApi($configuration);

$viewOptions = new Model\ViewOptions();

$fileInfo = new Model\FileInfo();
$fileInfo->setFilePath("SampleFiles/sample.ost");
$viewOptions->setFileInfo($fileInfo);

$request = new Requests\GetInfoRequest($viewOptions);
$response = $apiInstance->getInfo($request);

echo " Folders count: ", count($response->getOutlookViewInfo()->getFolders()), "\n";

```

{{< /tab >}} {{< tab tabNum="4" >}}

```javascript

// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer# require("groupdocs-viewer-cloud");

global.clientId = "XXXX-XXXX-XXXX-XXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
global.clientSecret = "XXXXXXXXXXXXXXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

global.infoApi = viewer_cloud.InfoApi.fromKeys(clientId, clientSecret);

let fileInfo = new viewer_cloud.FileInfo();
fileInfo.filePath = "SampleFiles/sample.ost";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;

let request = new viewer_cloud.GetInfoRequest(viewOptions);
let response = await infoApi.getInfo(request);
console.log(" Folders count: " + response.outlookViewInfo.folders.length);

```

{{< /tab >}} {{< tab tabNum="5" >}}

```python

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud

client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance# groupdocs_viewer_cloud.InfoApi.from_keys(client_id, client_secret)

view_options = groupdocs_viewer_cloud.ViewOptions()
view_options.file_info = groupdocs_viewer_cloud.FileInfo()
view_options.file_info.file_path = "SampleFiles/sample.ost"
view_options.view_format = "HTML"

request = groupdocs_viewer_cloud.GetInfoRequest(view_options)
response = apiInstance.get_info(request)
print(" Folders count: " + str(len(response.outlook_view_info.folders

```

{{< /tab >}} {{< tab tabNum="6" >}}

```ruby

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'

$client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
$client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

viewOptions = GroupDocsViewerCloud::ViewOptions.new
viewOptions.file_info = GroupDocsViewerCloud::FileInfo.new
viewOptions.file_info.file_path = "SampleFiles/sample.ost"
viewOptions.view_format = "HTML"

request = GroupDocsViewerCloud::GetInfoRequest.new(viewOptions)
response = infoApi.get_info(request)
puts(" Folders count: " + response.outlook_view_info.folders.length.to_s)

```

{{< /tab >}} {{< /tabs >}}

