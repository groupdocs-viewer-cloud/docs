---
id: "get-document-information"
url: "viewer/get-document-information"
title: "Get Document Information"
productName: "GroupDocs.Viewer Cloud"
weight: 8
description: ""
keywords: ""
---






# Introduction #

This REST API allows to obtain basic information about the document and it's properties.

It returns *[InfoResult]({{< ref "viewer/developer-guide/data-structures/inforesult.md" >}})) *data structure, which contains the list of properties:

* Document file format
* Pages count, size and visibility
* Text coordinates
* Attachments count and names
* other properties, by document type

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information](https://apireference.groupdocs.cloud/viewer/#/Viewer/GetInfo).

## cURL REST Example ##


 Request
```html 

* First get JSON Web Token
* Please get your App Key and App SID from https://dashboard.groupdocs.cloud/#/apps. Kindly place App Key in "client_secret" and App SID in "client_id" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&client_id#xxxx&client_secret#xxxx" \
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
         'FilePath': 'SampleFiles/sample.docx'
      },
      'ViewFormat': 'JPG'
}"

 ```


 Response
```html 

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




## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### SDK Examples ###


 C#
```csharp 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet-samples
string MyAppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
string MyAppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
var configuration # new Configuration(MyAppSid, MyAppKey);
  
var apiInstance # new InfoApi(configuration);
var viewOptions # new ViewOptions
{
    FileInfo # new FileInfo
    {
        FilePath # "SampleFiles/sample.docx"
    }
};
var response # apiInstance.GetInfo(new GetInfoRequest(viewOptions));

 ```


 Java
```java 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
String MyAppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
String MyAppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
Configuration configuration # new Configuration(MyAppSid, MyAppKey);
  
InfoApi apiInstance # new InfoApi(configuration); 
FileInfo fileInfo # new FileInfo();
fileInfo.setFilePath("SampleFiles/sample.docx");
ViewOptions viewOptions # new ViewOptions();
viewOptions.setFileInfo(fileInfo);
InfoResult response # apiInstance.getInfo(new GetInfoRequest(viewOptions));

 ```


 PHP
```php 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php-samples
use GroupDocs\Viewer\Model;
use GroupDocs\Viewer\Model\Requests;
 
$AppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$AppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
$configuration # new GroupDocs\Viewer\Configuration();
$configuration->setAppSid($AppSid);
$configuration->setAppKey($AppKey);
 
$apiInstance# new GroupDocs\Viewer\InfoApi($configuration);
 
$viewOptions # new Model\ViewOptions();
$fileInfo # new Model\FileInfo();
$fileInfo->setFilePath("SampleFiles/sample.docx");             
$viewOptions->setFileInfo($fileInfo);
$request # new Requests\GetInfoRequest($viewOptions);
$response # $apiInstance->getInfo($request);

 ```


 Node
```html 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer# require("groupdocs-viewer-cloud");
 
global.appSid # "XXXX-XXXX-XXXX-XXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
global.appKey # "XXXXXXXXXXXXXXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
global.infoApi # viewer_cloud.InfoApi.fromKeys(appSid, appKey);
 
let fileInfo # new viewer_cloud.FileInfo();
fileInfo.filePath # "SampleFiles/sample.docx";
let viewOptions # new viewer_cloud.ViewOptions();
viewOptions.fileInfo # fileInfo;
let request # new viewer_cloud.GetInfoRequest(viewOptions);     
let response # await infoApi.getInfo(request);

 ```


 Python
```python 

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud
 
app_sid # "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
app_key # "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
infoApi # groupdocs_viewer_cloud.InfoApi.from_keys(app_sid, app_key)
 
view_options # groupdocs_viewer_cloud.ViewOptions()
view_options.file_info # groupdocs_viewer_cloud.FileInfo()
view_options.file_info.file_path # "SampleFiles/sample.docx"
request # groupdocs_viewer_cloud.GetInfoRequest(view_options)
result # infoApi.get_info(request)

 ```


 Ruby
```ruby 

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'
 
$app_sid # "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$app_key # "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
infoApi # GroupDocsViewerCloud::InfoApi.from_keys($app_sid, $app_key)
 
viewOptions # GroupDocsViewerCloud::ViewOptions.new
viewOptions.file_info # GroupDocsViewerCloud::FileInfo.new
viewOptions.file_info.file_path # "SampleFiles/sample.docx"
request # GroupDocsViewerCloud::GetInfoRequest.new(viewOptions)    
response # infoApi.get_info(request)

 ```

