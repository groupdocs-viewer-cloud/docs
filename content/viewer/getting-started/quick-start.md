---
id: "quick-start"
url: "viewer/quick-start"
title: "Quick Start"
productName: "GroupDocs.Viewer Cloud"
weight: 3
description: "GroupDocs.Viewer Cloud Quick Start"
keywords: "GroupDocs.Viewer Cloud, Quick Start"
toc: True
---

## Create an account

Sign up at <https://id.containerize.com/signup> to create a free account.

## Create an API client app

Before you can make any requests to GroupDocs Cloud API you need to get Client Id and Client Secret. That will be used to invoke the GroupDocs Cloud API.

You can get it from existing Application or create new Application from [Applications View of GroupDocs Cloud Dashboard]({{< ref "total/ui-topics/creating-and-managing-application.md" >}}).

## Install the SDK of your choice

GroupDocs.Viewer Cloud SDK is written in different languages, all you need to get started is adding our [SDK]({{< ref "viewer/getting-started/available-sdks.md" >}}) to your project.

## Make an API request

Use the **Client Id** and **Client Secret** from the API app client you created in step one and replace in the corresponding code. Below is an example demonstrating how to preview document using GroupDocs.Viewer Cloud.

{{< alert style="info" >}}The GitHub repository for [GroupDocs.Viewer Cloud](https://github.com/groupdocs-viewer-cloud) has a complete set of examples, demonstrating our API capabilities.{{< /alert >}}

{{< tabs "example1-sdk">}}
{{< tab "C#" >}}
```cs
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

var configuration = new Configuration(MyClientId, MyClientSecret);
var apiInstance = new ViewApi(configuration);

var format = "jpg";
var request = new ConvertAndDownloadRequest(format, File.OpenRead("myfile.txt"));
var result = apiInstance.ConvertAndDownload(request);
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

$format ="jpg";
$path = __DIR__ . 'myfile.txt';

$request = new Requests\convertAndDownloadRequest($format, $path);

$result = $apiInstance->convertAndDownload($request);
```
{{< /tab >}} 
{{< tab "Java">}}
```java

// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
string MyClientSecret = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

Configuration configuration = new Configuration(MyClientId, MyClientSecret);
ViewApi apiInstance = new ViewApi(configuration);

String format = "pdf";
File fileObj = new File("myfile.txt");

ConvertAndDownloadRequest request = new ConvertAndDownloadRequest(format, fileObj, null, null);

File file = apiInstance.convertAndDownload(request);
```
{{< /tab >}} 
{{< tab "Ruby">}}
```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'

$client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
$client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance = GroupDocsViewerCloud::ViewApi.from_keys($client_id, $client_secret)

format = "jpg"      
file = File.open("myfile.txt", "r")

request = ConvertAndDownloadRequest.new format, file

response = apiInstance.convert_and_download(request)
```
{{< /tab >}} 
{{< tab "Node.js">}}
```js
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer# require("groupdocs-viewer-cloud");

global.clientId = "XXXX-XXXX-XXXX-XXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
global.clientSecret = "XXXXXXXXXXXXXXXX"; // Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

global.viewApi = viewer_cloud.ViewApi.fromKeys(clientId, clientSecret);

var format = "jpg";
let filebuf = fs.readFileSync("myfile.txt");

var request = new ConvertAndDownloadRequest(format, filebuf);
let response = await viewApi.convertAndDownload(request);
```
{{< /tab >}} 
{{< tab "Python">}}
```py
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud

client_id = "XXXX-XXXX-XXXX-XXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
client_secret = "XXXXXXXXXXXXXXXX" # Get Client Id and Client Secret from https://dashboard.groupdocs.cloud

apiInstance = groupdocs_viewer_cloud.ViewApi.from_keys(client_id, client_secret)

format = "jpg"      
file = File.open("myfile.txt", "r")

request = ConvertAndDownloadRequest.new format, file

response = apiInstance.convert_and_download(request)
```
{{< /tab >}}
{{< tab "Go">}}
```go
package basicUsage

import (
	"fmt"
	"os"

	"github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
)

func ConvertAndDownload() {
	// Open the file to be converted
	file, err := os.Open("Resources/SampleFiles/sample.docx")
	if err != nil {
		fmt.Printf("Exception: %v\n", err)
		return
	}
	defer file.Close()

	// Call the API
	response, _, err := config.Client.ViewApi.ConvertAndDownload(config.Ctx, "jpg", file, nil)
	if err != nil {
		fmt.Printf("Exception: %v\n", err)
		return
	}

	fileInfo, err := response.Stat()
	if err != nil {
		fmt.Printf("Exception: %v\n", err)
		return
	}
	fmt.Printf("ConvertAndDownload completed: %v bytes received\n", fileInfo.Size())
}
```
{{< /tab >}}
{{< /tabs >}}