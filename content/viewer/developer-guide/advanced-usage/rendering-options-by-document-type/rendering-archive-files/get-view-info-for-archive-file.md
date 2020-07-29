---
id: "get-view-info-for-archive-file"
url: "viewer/get-view-info-for-archive-file"
title: "Get View Info for Archive File"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

 






# Introduction #

GroupDocs.Viewer Cloud provides additional information such as list of folders when calling Info method. To retrieve view information for Archive File call Info method and cast output result to ArchiveViewInfo type.

Following example demonstrates how to print out archive contents.

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
    'FilePath': 'SampleFiles/with_folders.zip'
  }
}"

 ```


 Response
```html 

{
  "formatExtension": ".zip",
  "format": "Zipped File",
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
      "name": "file (12).txt"
    },
    {
      "name": "file (13).txt"
    },
    {
      "name": "file (14).txt"
    },
    {
      "name": "file (15).txt"
    },
    {
      "name": "file (16).txt"
    },
    {
      "name": "file (17).txt"
    },
    {
      "name": "file (18).txt"
    },
    {
      "name": "sample-inside-folder.txt"
    },
    {
      "name": "file (1).txt"
    },
    {
      "name": "file (2).txt"
    },
    {
      "name": "file (3).txt"
    },
    {
      "name": "file (4).txt"
    },
    {
      "name": "file (5).txt"
    },
    {
      "name": "file (6).txt"
    },
    {
      "name": "file (7).txt"
    },
    {
      "name": "file (8).txt"
    },
    {
      "name": "file (9).txt"
    },
    {
      "name": "file (10).txt"
    },
    {
      "name": "file (11).txt"
    }
  ],
  "archiveViewInfo": {
    "folders": [
      "FirstFolderName",
      "SecondFolder",
      "ThirdFolderWithItems"
    ]
  },
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
        FilePath # "SampleFiles/with_folders.zip"
    }
};
 
var response # apiInstance.GetInfo(new GetInfoRequest(viewOptions));
foreach (var folder in response.ArchiveViewInfo.Folders)
    Console.WriteLine(folder);

 ```


 Java
```java 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
String MyAppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
String MyAppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
Configuration configuration # new Configuration(MyAppSid, MyAppKey); 
InfoApi apiInstance # new InfoApi(configuration); 
 
FileInfo fileInfo # new FileInfo();
fileInfo.setFilePath("SampleFiles/with_folders.zip");
ViewOptions viewOptions # new ViewOptions();
viewOptions.setFileInfo(fileInfo);
 
InfoResult response # apiInstance.getInfo(new GetInfoRequest(viewOptions));
List<String> folders # response.getArchiveViewInfo().getFolders();
for(int i # 0; i < folders.size(); i++)
    System.out.println(folders.get(i));

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
$fileInfo->setFilePath("SampleFiles/with_folders.zip");             
$viewOptions->setFileInfo($fileInfo);
 
$request # new Requests\GetInfoRequest($viewOptions);
$response # $apiInstance->getInfo($request);
foreach ($response->getArchiveViewInfo()->getFolders() as $folder) {
    echo $folder, "\n";
}

 ```


 Node
```html 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer# require("groupdocs-viewer-cloud");
 
global.appSid # "XXXX-XXXX-XXXX-XXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
global.appKey # "XXXXXXXXXXXXXXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
global.infoApi # viewer_cloud.InfoApi.fromKeys(appSid, appKey);
 
let fileInfo # new viewer_cloud.FileInfo();
fileInfo.filePath # "SampleFiles/with_folders.zip";
let viewOptions # new viewer_cloud.ViewOptions();
viewOptions.fileInfo # fileInfo;
viewOptions.viewFormat # viewer_cloud.ViewOptions.ViewFormatEnum.HTML;
 
let request # new viewer_cloud.GetInfoRequest(viewOptions);     
let response # await infoApi.getInfo(request);
let folders # response.archiveViewInfo.folders;
for (let i # 0; i < folders.length; i++) {            
    console.log(folders[i]);
}

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
view_options.file_info.file_path # "SampleFiles/with_folders.zip"
view_options.view_format # "HTML"
 
request # groupdocs_viewer_cloud.GetInfoRequest(view_options)
response # apiInstance.get_info(request)
folders # response.archive_view_info.folders
for folder in folders:
    print(folder)

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
viewOptions.file_info.file_path # "SampleFiles/with_folders.zip"
viewOptions.view_format # "HTML"
 
request # GroupDocsViewerCloud::GetInfoRequest.new(viewOptions)    
response # infoApi.get_info(request)
for folder in response.archive_view_info.folders do
    puts(" " + folder)
end

 ```

