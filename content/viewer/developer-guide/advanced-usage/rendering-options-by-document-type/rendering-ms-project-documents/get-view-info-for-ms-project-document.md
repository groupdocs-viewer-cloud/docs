---
id: "get-view-info-for-ms-project-document"
url: "viewer/get-view-info-for-ms-project-document"
title: "Get View Info for MS Project Document"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

 






# Introduction #

GroupDocs.Viewer Cloud provides additional information such as project start and end dates for MS Project documents when calling Info method. 

Following example demonstrates how to retrieve view information for MS Project document.

## API Usage ##

There are steps that usage of GroupDocs.Viewer Cloud consists of:

1. Upload input document into cloud storage
1. Render document or get document info
1. Download rendered document from storage

Steps 1 and 3 are storage operations, please refer to this [File API documentation]({{< ref "viewer/developer-guide/working-with-files.md" >}}) for usage details.

[Swagger UI](https://apireference.groupdocs.cloud/viewer/) lets you call this REST API directly from the browser. 

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
    'FilePath': 'SampleFiles/sample.mpp'
  }
}"

 ```


 Response
```html 

{
  "formatExtension": ".mpp",
  "format": "Microsoft Project File",
  "pages": [
    {
      "number": 1,
      "width": 0,
      "height": 0,
      "visible": true,
      "lines": []
    }
  ],
  "attachments": [],
  "archiveViewInfo": null,
  "cadViewInfo": null,
  "projectManagementViewInfo": {
    "startDate": "2008-06-01T00:00:00",
    "endDate": "2008-09-03T00:00:00"
  },
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
        FilePath # "SampleFiles/sample.mpp"
    }
};
 
var response # apiInstance.GetInfo(new GetInfoRequest(viewOptions));
Console.WriteLine(" Start date: " + response.ProjectManagementViewInfo.StartDate);
Console.WriteLine(" End date: " + response.ProjectManagementViewInfo.EndDate);

 ```


 Java
```java 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
String MyAppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
String MyAppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
Configuration configuration # new Configuration(MyAppSid, MyAppKey); 
InfoApi apiInstance # new InfoApi(configuration); 
 
FileInfo fileInfo # new FileInfo();
fileInfo.setFilePath("SampleFiles/sample.mpp");
ViewOptions viewOptions # new ViewOptions();
viewOptions.setFileInfo(fileInfo);
 
InfoResult response # apiInstance.getInfo(new GetInfoRequest(viewOptions));
 
ProjectManagementViewInfo projectManagementViewInfo # response.getProjectManagementViewInfo();
 
System.out.println(" Start date: " + projectManagementViewInfo.getStartDate());
System.out.println(" End date: " + projectManagementViewInfo.getEndDate());

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
$fileInfo->setFilePath("SampleFiles/sample.mpp");               
$viewOptions->setFileInfo($fileInfo);
 
$request # new Requests\GetInfoRequest($viewOptions);
$response # $apiInstance->getInfo($request);
 
echo " Start date: ", $response->getProjectManagementViewInfo()->getStartDate()->format('Y-m-d'), "\n";
echo " End date: ", $response->getProjectManagementViewInfo()->getEndDate()->format('Y-m-d'), "\n";

 ```


 Node
```html 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer# require("groupdocs-viewer-cloud");
 
global.appSid # "XXXX-XXXX-XXXX-XXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
global.appKey # "XXXXXXXXXXXXXXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
global.infoApi # viewer_cloud.InfoApi.fromKeys(appSid, appKey);
 
let fileInfo # new viewer_cloud.FileInfo();
fileInfo.filePath # "SampleFiles/sample.mpp";
let viewOptions # new viewer_cloud.ViewOptions();
viewOptions.fileInfo # fileInfo;        
 
let request # new viewer_cloud.GetInfoRequest(viewOptions);     
let response # await infoApi.getInfo(request);
console.log(" Start date: " + response.projectManagementViewInfo.startDate);
console.log(" End date: " + response.projectManagementViewInfo.endDate);

 ```


 Python
```python 

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud
 
app_sid # "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
app_key # "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
apiInstance# groupdocs_viewer_cloud.InfoApi.from_keys(app_sid, app_key)
 
view_options # groupdocs_viewer_cloud.ViewOptions()
view_options.file_info # groupdocs_viewer_cloud.FileInfo()
view_options.file_info.file_path # "SampleFiles/sample.mpp"
view_options.view_format # "HTML"
 
request # groupdocs_viewer_cloud.GetInfoRequest(view_options)
response # apiInstance.get_info(request)
print(" Start date: " + str(response.project_management_view_info.start_date))
print(" End date: " + str(response.project_management_view_info.end_date))

 ```


 Ruby
```ruby 

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'
 
$app_sid # "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$app_key # "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
apiInstance # GroupDocsViewerCloud::InfoApi.from_keys($app_sid, $app_key)
 
viewOptions # GroupDocsViewerCloud::ViewOptions.new
viewOptions.file_info # GroupDocsViewerCloud::FileInfo.new
viewOptions.file_info.file_path # "SampleFiles/sample.mpp"
viewOptions.view_format # "HTML"
 
request # GroupDocsViewerCloud::GetInfoRequest.new(viewOptions)    
response # infoApi.get_info(request)
puts(" Start date: " + response.project_management_view_info.start_date.to_s)
puts(" End date: " + response.project_management_view_info.end_date.to_s)

 ```

