---
id: "image-viewer-get-text-coordinates"
url: "viewer/image-viewer-get-text-coordinates"
title: "Image Viewer - Get text coordinates"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

 






# Introduction #

GroupDocs.Viewer Cloud provides the feature of getting text coordinates. This feature is useful if you want to add selectable text over the image or implement a text search in image-based rendering. 

The ExtractText property of ImageOptions* *class* *enables you to get the text contained in a source document with coordinates.

Following code sample shows how to retrieve and print out text (lines / words / characters) of each document page with coordinates.

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
    'FilePath': 'SampleFiles/sample.docx'
  },
  'ViewFormat': 'PNG',
  'RenderOptions': {
     'ExtractText': true
  }
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
      "lines": [
        {
          "words": [
            {
              "characters": [
                {
                  "x": 229.607,
                  "y": 67.8,
                  "width": 10.674,
                  "height": 19.8,
                  "value": "T"
                },
...

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
    },
    ViewFormat # ViewOptions.ViewFormatEnum.PNG,
    RenderOptions # new ImageOptions
    {
        ExtractText # true
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
viewOptions.setViewFormat(ViewFormatEnum.PNG);
ImageOptions renderOptions # new ImageOptions();
renderOptions.setExtractText(true);
viewOptions.setRenderOptions(renderOptions);
 
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
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_PNG);
$renderOptions # new Model\ImageOptions();
$renderOptions->setExtractText(true);
$viewOptions->setRenderOptions($renderOptions);
 
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
viewOptions.viewFormat # viewer_cloud.ViewOptions.ViewFormatEnum.PNG;
viewOptions.renderOptions # new viewer_cloud.ImageOptions();
viewOptions.renderOptions.extractText # true;    
 
let request # new viewer_cloud.GetInfoRequest(viewOptions);     
let response # await infoApi.getInfo(request);

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
view_options.file_info.file_path # "SampleFiles/sample.docx"
view_options.view_format # "PNG"
view_options.render_options # groupdocs_viewer_cloud.ImageOptions()
view_options.render_options.extract_text # True      
 
request # groupdocs_viewer_cloud.GetInfoRequest(view_options)

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
viewOptions.file_info.file_path # "SampleFiles/sample.docx"
viewOptions.view_format # "PNG"
viewOptions.render_options # GroupDocsViewerCloud::ImageOptions.new
viewOptions.render_options.extract_text # true
 
request # GroupDocsViewerCloud::GetInfoRequest.new(viewOptions)

 ```

