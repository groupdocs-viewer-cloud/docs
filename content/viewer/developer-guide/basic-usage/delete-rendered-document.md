---
id: "delete-rendered-document"
url: "viewer/delete-rendered-document"
title: "Delete rendered document"
productName: "GroupDocs.Viewer Cloud"
weight: 5
description: ""
keywords: ""
toc: True
---

After rendering various types of documents into HTML, Image, or Pdf, you may clean (delete) rendered pages from cloud storage using special method.
Note: This method deletes only output files, the input file remains in the storage.

Following example demonstrates on how to delete rendered document results.

## API Usage

[Swagger UI](https://apireference.groupdocs.cloud/viewer/) lets you call this REST API directly from the browser.

## cURL example

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}
```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The credentials are read from environment variables CLIENT_ID and CLIENT_SECRET.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to delete rendered document files
# The JWT token is read from the environment variable JWT_TOKEN.
curl -v "https://api.groupdocs.cloud/v2.0/viewer/view" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
      "FilePath": "SampleFiles/sample.docx"
    }
  }'
```
{{< /tab >}}

{{< tab "Windows PowerShell" >}}
```powershell
# First get JSON Web Token
# Client credentials are read from environment variables CLIENT_ID and CLIENT_SECRET.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to delete rendered document files
# JWT token is read from the environment variable JWT_TOKEN.
curl.exe -v "https://api.groupdocs.cloud/v2.0/viewer/view" `
  -X DELETE `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{ 'FileInfo': { 'FilePath': 'SampleFiles/sample.docx' } }"
```
{{< /tab >}}

{{< tab "Windows CMD" >}}
```cmd
:: First get JSON Web Token
:: Client credentials are read from environment variables CLIENT_ID and CLIENT_SECRET.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

:: cURL example to delete rendered document files
:: JWT token is read from the environment variable JWT_TOKEN.
curl -v "https://api.groupdocs.cloud/v2.0/viewer/view" ^
  -X DELETE ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FileInfo\":{\"FilePath\":\"SampleFiles/sample.docx\"}}"
```
{{< /tab >}} {{< tab "Response" >}}
```log
An empty response with status '204 No Content' is returned to confirm deletion.

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
        FilePath = "SampleFiles/sample.docx"
    }
};

// Create view
var response = apiInstance.CreateView(new CreateViewRequest(viewOptions));

// Delete view
var deleteOptions = new DeleteViewOptions
{
    FileInfo = new FileInfo
    {
        FilePath = "SampleFiles/sample.docx"
    }
};

apiInstance.DeleteView(new DeleteViewRequest(deleteOptions));
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

// Create view
$viewOptions = new Model\ViewOptions();
$fileInfo = new Model\FileInfo();
$fileInfo->setFilePath("SampleFiles/sample.docx");
$viewOptions->setFileInfo($fileInfo);

$request = new Requests\CreateViewRequest($viewOptions);
$response = $apiInstance->createView($request);

// Delete view
$deleteOptions = new DeleteViewOptions();
$deleteOptions->setFileInfo($fileInfo);
$deleteRequest = new Requests\deleteViewRequest($deleteOptions);

$apiInstance->deleteView($deleteRequest); 
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
fileInfo.setFilePath("SampleFiles/sample.docx");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);

// Create view
ViewResult response = apiInstance.createView(new CreateViewRequest(viewOptions));

// Delete view                           
DeleteViewOptions deleteViewOptions = new DeleteViewOptions();
fileInfo.setFilePath("SampleFiles/sample.docx");
DeleteViewRequest dRequest = new DeleteViewRequest(deleteViewOptions);        
apiInstance.deleteView(dRequest);   
```
{{< /tab >}} 
{{< tab "Ruby">}}
```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'

$client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
$client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance = GroupDocsViewerCloud::ViewApi.from_keys($client_id, $client_secret)

# Create view
viewOptions = GroupDocsViewerCloud::ViewOptions.new
viewOptions.file_info = GroupDocsViewerCloud::FileInfo.new
viewOptions.file_info.file_path = "SampleFiles/sample.docx"

request = GroupDocsViewerCloud::CreateViewRequest.new(viewOptions)
response = apiInstance.create_view(request)

# Delete view
dViewOptions = GroupDocsViewerCloud::DeleteViewOptions.new
dViewOptions.file_info = viewOptions.file_info
dRequest = GroupDocsViewerCloud::DeleteViewRequest.new(dViewOptions)
apiInstance.delete_view(dRequest)
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
fileInfo.filePath = "SampleFiles/sample.docx";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;

// Create view
let request = new viewer_cloud.CreateViewRequest(viewOptions);
let response = await viewApi.createView(request);

// Delete view
let dvOptions = new DeleteViewOptions();
dvOptions.fileInfo = fileInfo;
const delRequest = new DeleteViewRequest(dvOptions);
await viewApi.deleteView(delRequest);
```
{{< /tab >}} 
{{< tab "Python">}}
```py
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud

client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance = groupdocs_viewer_cloud.ViewApi.from_keys(client_id, client_secret)

# Create view
view_options = groupdocs_viewer_cloud.ViewOptions()
view_options.file_info = groupdocs_viewer_cloud.FileInfo()
view_options.file_info.file_path = "SampleFiles/sample.docx"

request = groupdocs_viewer_cloud.CreateViewRequest(view_options)
response = apiInstance.create_view(request)

# Delete view
d_view_options = groupdocs_viewer_cloud.DeleteViewOptions()
d_view_options.file_info = view_options.file_info
d_request = groupdocs_viewer_cloud.DeleteViewRequest(d_view_options)
apiInstance.delete_view(d_request)
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

func DeleteViewExample() {

	// Create view
    opts := viewer.ViewOptions{
		FileInfo: &viewer.FileInfo{
			FilePath: "SampleFiles/sample.docx",
		},
	}
    
	response, _, err := config.Client.ViewApi.CreateView(config.Ctx, opts)
	if err != nil {
		fmt.Printf("Exception: %v\n", err)
		return
	}

    // Delete view
	delOpts := viewer.DeleteViewOptions{
		FileInfo: &viewer.FileInfo{
			FilePath: "SampleFiles/sample.docx",
		},
	}

	delResponse, _, err := config.Client.ViewApi.DeleteView(config.Ctx, delOpts)
	if err != nil {
		fmt.Printf("Exception: %v\n", err)
		return
	}    
}

```
{{< /tab >}}
{{< /tabs >}}

