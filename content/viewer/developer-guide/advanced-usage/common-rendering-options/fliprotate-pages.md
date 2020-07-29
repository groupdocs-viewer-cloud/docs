---
id: "fliprotate-pages"
url: "viewer/fliprotate-pages"
title: "Flip/rotate pages"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

 






# Introduction #

![](viewer/images/image-1.png)

The GroupDocs.Viewer Cloud enables you to rotate individual pages when viewing documents in HTML/PDF/JPG/PNG formats. To flip/rotate pages use the PageRotations property of ViewOptions class. There are three options that you can pass:

* On90Degree - instructs to rotate page on 90-degree clockwise; 
* On180Degree - instructs to rotate page on 180-degree clockwise;
* On270Degree - instructs to rotate page on 270-degree clockwise;

The following code snippet shows how to rotate output pages when viewing a document as PDF

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
curl -v "https://api.groupdocs.cloud/v2.0/viewer/view" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{
  'FileInfo': {
    'FilePath': 'SampleFiles/sample.docx'
  },
  'ViewFormat': 'PDF',
  'RenderOptions': {
     'PageRotations': [
       {
         'PageNumber': 1,
         'RotationAngle': 'On90Degree'
       }
     ]
  }
}"

 ```


 Response
```html 

{
  "pages": null,
  "attachments": [],
  "file": {
    "path": "viewer/sample_docx/sample.pdf",
    "downloadUrl": "https://api-qa.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_docx/sample.pdf"
  }
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
var apiInstance # new ViewApi(configuration);
 
var viewOptions # new ViewOptions
{
    FileInfo # new FileInfo
    {
        FilePath # "SampleFiles/sample.docx"
    },
    ViewFormat # ViewOptions.ViewFormatEnum.PDF,
 
    RenderOptions # new RenderOptions
    {
        PageRotations # new List<PageRotation>
        {
            new PageRotation
            {
                PageNumber # 1,
                RotationAngle # PageRotation.RotationAngleEnum.On90Degree
            }
        }
    }
};
 
var response # apiInstance.CreateView(new CreateViewRequest(viewOptions));

 ```


 Java
```java 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
String MyAppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
String MyAppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
Configuration configuration # new Configuration(MyAppSid, MyAppKey); 
ViewApi apiInstance # new ViewApi(configuration); 
 
FileInfo fileInfo # new FileInfo();
fileInfo.setFilePath("SampleFiles/sample.docx");
ViewOptions viewOptions # new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.PDF);
RenderOptions renderOptions # new RenderOptions();
PageRotation pageRotation # new PageRotation();
pageRotation.setPageNumber(1);
pageRotation.setRotationAngle(RotationAngleEnum.ON90DEGREE);
renderOptions.addPageRotationsItem(pageRotation);
viewOptions.setRenderOptions(renderOptions);
 
ViewResult response # apiInstance.createView(new CreateViewRequest(viewOptions));

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
 
$apiInstance# new GroupDocs\Viewer\ViewApi($configuration);
 
$viewOptions # new Model\ViewOptions();
$fileInfo # new Model\FileInfo();
$fileInfo->setFilePath("SampleFiles/sample.docx");              
$viewOptions->setFileInfo($fileInfo);
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_PDF);
$renderOptions # new Model\PdfOptions();
$pageRotation # new Model\PageRotation();
$pageRotation->setPageNumber(1);
$pageRotation->setRotationAngle(Model\PageRotation::ROTATION_ANGLE_ON90_DEGREE);
$renderOptions->setPageRotations([$pageRotation]);
$viewOptions->setRenderOptions($renderOptions);
 
$request # new Requests\CreateViewRequest($viewOptions);
$response # $apiInstance->createView($request);

 ```


 Node
```html 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer# require("groupdocs-viewer-cloud");
 
global.appSid # "XXXX-XXXX-XXXX-XXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
global.appKey # "XXXXXXXXXXXXXXXX"; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
global.viewApi # viewer_cloud.ViewApi.fromKeys(appSid, appKey);
 
let fileInfo # new viewer_cloud.FileInfo();
fileInfo.filePath # "SampleFiles/sample.docx";
let viewOptions # new viewer_cloud.ViewOptions();
viewOptions.fileInfo # fileInfo;
viewOptions.viewFormat # viewer_cloud.ViewOptions.ViewFormatEnum.PDF;
viewOptions.renderOptions # new viewer_cloud.PdfOptions();
let pageRotation # new viewer_cloud.PageRotation();
pageRotation.pageNumber # 1;
pageRotation.rotationAngle # viewer_cloud.PageRotation.RotationAngleEnum.On90Degree;
viewOptions.renderOptions.pageRotations # [pageRotation];
 
let request # new viewer_cloud.CreateViewRequest(viewOptions);      
let response # await viewApi.createView(request);

 ```


 Python
```python 

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud
 
app_sid # "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
app_key # "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
apiInstance# groupdocs_viewer_cloud.ViewApi.from_keys(app_sid, app_key)
 
view_options # groupdocs_viewer_cloud.ViewOptions()
view_options.file_info # groupdocs_viewer_cloud.FileInfo()
view_options.file_info.file_path # "SampleFiles/sample.docx"
view_options.view_format # "PDF"
view_options.render_options # groupdocs_viewer_cloud.PdfOptions()
page_rotation # groupdocs_viewer_cloud.PageRotation()
page_rotation.page_number # 1
page_rotation.rotation_angle # "On90Degree"
view_options.render_options.page_rotations # [page_rotation]
 
request # groupdocs_viewer_cloud.CreateViewRequest(view_options)
response # apiInstance.create_view(request)

 ```


 Ruby
```ruby 

# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'
 
$app_sid # "XXXX-XXXX-XXXX-XXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
$app_key # "XXXXXXXXXXXXXXXX" # Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
apiInstance # GroupDocsViewerCloud::ViewApi.from_keys($app_sid, $app_key)
 
viewOptions # GroupDocsViewerCloud::ViewOptions.new
viewOptions.file_info # GroupDocsViewerCloud::FileInfo.new
viewOptions.file_info.file_path # "SampleFiles/sample.docx"
viewOptions.view_format # "PDF"
viewOptions.render_options # GroupDocsViewerCloud::PdfOptions.new
page_rotation # GroupDocsViewerCloud::PageRotation.new
page_rotation.page_number # 1
page_rotation.rotation_angle # "On90Degree"
viewOptions.render_options.page_rotations # [page_rotation]
 
request # GroupDocsViewerCloud::CreateViewRequest.new(viewOptions)    
response # apiInstance.create_view(request)

 ```

