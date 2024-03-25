---
id: "convert-and-download"
url: "viewer/convert-and-download"
title: "Convert and download document"
productName: "GroupDocs.Viewer Cloud"
weight: 5
description: ""
keywords: ""
toc: True
---

GroupDocs.Viewer Cloud API enables you to to render documents using single API call, passing input file in the request body, and getting result file stream in the response.
This example demonstrates how to render document without using cloud storage.

Method parameters:

|Name|Type|Description|Comment
|---|---|---|---
|format|string|Requested conversion format: HTML, JPG, PNG or PDF|Required.
|File|binary|Input file to convert|Form data, Required
|pages|string|Pages range to render, like "1,2" or "3-5,10"|Default value : all pages
|password|string|Input document password|Required for password-protected documents.

## Resource URI

```HTTP PUT ~/convertAndDownload```

[Swagger UI](https://reference.groupdocs.cloud/viewer/) lets you call this REST API directly from the browser.

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
curl -v "https://api.groupdocs.cloud/v2.0/viewer/convertAndDownload" \
-X PUT \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
--data-binary "@path/to/file"
```
{{< /tab >}} {{< tab "Resonse" >}}
```json
Code 200
<binary file>
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
{{< /tabs >}}
