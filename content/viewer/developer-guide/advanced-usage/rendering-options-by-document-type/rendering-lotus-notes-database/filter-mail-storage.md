---
id: "filter-mail-storage"
url: "viewer/filter-mail-storage"
title: "Filter mail storage"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
toc: True
---

Lotus Notes allows filtering messages inside folders by some text value from message content and by part of the sender’s or recipient’s address.

![](/viewer/images/filter-nsf-messages.jpg)

GroupDocs.Viewer also allows filtering the rendered messages using the following filters:

+ Filter by subject and content using LotusNotesOptions.TextFilter;
+ Filter by the sender’s and recipient’s email addresses using LotusNotesOptions.AddressFilter;

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
      "FilePath": "SampleFiles/sample.nsf"
    },
    "ViewFormat": "HTML",
    "RenderOptions": {
      "MailStorageOptions": {
        "TextFilter": "April 2015",
        "AddressFilter": "test@test.com"
      }
    }
  }'
```
{{< /tab >}}

{{< tab "Windows PowerShell" >}}
```powershell
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
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
  -d '{ 
    "FileInfo": { 
      "FilePath": "SampleFiles/sample.nsf" 
    }, 
    "ViewFormat": "HTML", 
    "RenderOptions": { 
      "MailStorageOptions": { 
        "TextFilter": "April 2015", 
        "AddressFilter": "test@test.com" 
      } 
    } 
  }'
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
  -d "{\"FileInfo\":{\"FilePath\":\"SampleFiles/sample.nsf\"},\"ViewFormat\":\"HTML\",\"RenderOptions\":{\"MailStorageOptions\":{\"TextFilter\":\"April 2015\",\"AddressFilter\":\"test@test.com\"}}}"
```
{{< /tab >}} {{< tab "Response" >}}
```json
{
  "pages": [
    {
      "number": 1,
      "resources": null,
      "path": "viewer/sample_nsf/sample_page_1.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_nsf/sample_page_1.html"
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
        FilePath = "SampleFiles/sample.nsf"
    },
    ViewFormat = ViewOptions.ViewFormatEnum.HTML,
    RenderOptions = new HtmlOptions
    {
        MailStorageOptions = new MailStorageOptions
        {
            TextFilter = "April 2015",
            AddressFilter = "test@test.com"
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
$fileInfo->setFilePath("SampleFiles/sample.nsf");
$viewOptions->setFileInfo($fileInfo);
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_HTML);
$renderOptions = new Model\HtmlOptions();
$mailStorageOptions = new Model\MailStorageOptions();
$mailStorageOptions->setTextFilter("April 2015");
$mailStorageOptions->setAddressFilter("test@test.com");
$renderOptions->setMailStorageOptions($mailStorageOptions);
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
fileInfo.setFilePath("SampleFiles/sample.nsf");
ViewOptions viewOptions = new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.HTML);
HtmlOptions renderOptions = new HtmlOptions();            
MailStorageOptions mailStorageOptions = new MailStorageOptions();
mailStorageOptions.setTextFilter("April 2015");
mailStorageOptions.setAddressFilter("test@test.com");
renderOptions.setMailStorageOptions(mailStorageOptions);
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
viewOptions.file_info.file_path = "SampleFiles/sample.nsf"
viewOptions.view_format = "HTML"
viewOptions.render_options = GroupDocsViewerCloud::HtmlOptions.new
viewOptions.render_options.mail_storage_options = GroupDocsViewerCloud::MailStorageOptions.new
viewOptions.render_options.mail_storage_options.text_filter = "April 2015"
viewOptions.render_options.mail_storage_options.address_filter = "test@test.com"

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
fileInfo.filePath = "SampleFiles/sample.nsf";
let viewOptions = new viewer_cloud.ViewOptions();
viewOptions.fileInfo = fileInfo;
viewOptions.viewFormat = viewer_cloud.ViewOptions.ViewFormatEnum.HTML;
viewOptions.renderOptions = new viewer_cloud.HtmlOptions();
viewOptions.renderOptions.mailStorageOptions = new viewer_cloud.MailStorageOptions();     
viewOptions.renderOptions.mailStorageOptions.textFilter = "April 2015";
viewOptions.renderOptions.mailStorageOptions.addressFilter = "test@test.com";

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
view_options.file_info.file_path = "SampleFiles/sample.nsf"
view_options.view_format = "HTML"
view_options.render_options = groupdocs_viewer_cloud.HtmlOptions()
view_options.render_options.mail_storage_options = groupdocs_viewer_cloud.MailStorageOptions()    
view_options.render_options.mail_storage_options.text_filter = "April 2015"
view_options.render_options.mail_storage_options.address_filter = "test@test.com"

request = groupdocs_viewer_cloud.CreateViewRequest(view_options)
response = apiInstance.create_view(request)
```
{{< /tab >}} 
{{< tab "Go">}}
```go
package RenderingLotusNotesDatabase

import (
    "fmt"

    "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
    viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

// This example demonstrates how to filter Lotus Notes database messages
func FilterMailStorage() {
    viewOptions := viewer.ViewOptions{
        FileInfo: &viewer.FileInfo{
            FilePath: "SampleFiles/sample.nsf",
        },
        ViewFormat: viewer.ViewFormatHtml,
        RenderOptions: &viewer.HtmlOptions{
            MailStorageOptions: &viewer.MailStorageOptions{
                TextFilter:    "April 2015",
                AddressFilter: "test@test.com",
            },
        },
    }

    response, _, err := config.Client.ViewApi.CreateView(config.Ctx, viewOptions)
    if err != nil {
        fmt.Printf("Exception: %v\n", err)
        return
    }

    fmt.Printf("FilterMailStorage completed: %v pages\n", len(response.Pages))
}
```
{{< /tab >}}
{{< /tabs >}}

