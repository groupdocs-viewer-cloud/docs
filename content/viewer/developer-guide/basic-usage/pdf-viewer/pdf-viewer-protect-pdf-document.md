---
id: "pdf-viewer-protect-pdf-document"
url: "viewer/pdf-viewer-protect-pdf-document"
title: "PDF Viewer - Protect PDF document"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

 






# Introduction #

GroupDocs.Viewer Cloud enables you to protect output PDF document by setting permissions, password for opening and password for changing permissions.

Following example demonstrates how to protect output PDF document.

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
     'Permissions': 'DenyModification',
     'PermissionsPassword': 'p123',
     'DocumentOpenPassword': 'o123'
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
    "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_docx/sample.pdf"
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
    RenderOptions # new PdfOptions
    {
        Permissions # PdfOptions.PermissionsEnum.DenyModification,
        PermissionsPassword # "p123",
        DocumentOpenPassword # "o123"
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
PdfOptions renderOptions # new PdfOptions();
renderOptions.setPermissions(PermissionsEnum.DENYMODIFICATION);
renderOptions.setPermissionsPassword("p123");
renderOptions.setDocumentOpenPassword("o123");
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
$renderOptions->setPermissions(Model\PdfOptions::PERMISSIONS_DENY_MODIFICATION);
$renderOptions->setPermissionsPassword("p123");
$renderOptions->setDocumentOpenPassword("o123");
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
fileInfo.filePath # "SampleFiles/with_jpg_image.pptx";
let viewOptions # new viewer_cloud.ViewOptions();
viewOptions.fileInfo # fileInfo;
viewOptions.viewFormat # viewer_cloud.ViewOptions.ViewFormatEnum.PDF;
viewOptions.renderOptions # new viewer_cloud.PdfOptions();
viewOptions.renderOptions.permissions # viewer_cloud.PdfOptions.PermissionsEnum.DenyModification,
viewOptions.renderOptions.permissionsPassword # "p123";
viewOptions.renderOptions.documentOpenPassword # "o123";
 
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
view_options.render_options.permissions # "DenyModification"
view_options.render_options.permissions_password # "p123"
view_options.render_options.document_open_password # "o123"
 
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
viewOptions.render_options.permissions # "DenyModification"
viewOptions.render_options.permissions_password # "p123"
viewOptions.render_options.document_open_password # "o123"
 
request # GroupDocsViewerCloud::CreateViewRequest.new(viewOptions)    
response # apiInstance.create_view(request)

 ```

