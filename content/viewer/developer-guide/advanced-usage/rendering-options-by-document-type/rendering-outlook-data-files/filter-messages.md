---
id: "filter-messages"
url: "viewer/filter-messages"
title: "Filter messages"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

 






# Introduction #

MS Outlook allows to filter messages inside folders by some text value from message content and by part of the sender's or recipient's address.


![](viewer/images/filter.png)
GroupDocs.Viewer Cloud also allows filtering the rendered messages using the following filters:


* Filter by subject and content using OutlookOptions.TextFilter*;*
* Filter by the sender's and recipient's email addresses using OutlookOptions.[AddressFilter](https://apireference.groupdocs.com/net/viewer/groupdocs.viewer.options/outlookoptions/properties/addressfilter)*;*


As an example, when setting OutlookOptions.TextFilter** **as 'Microsoft'  the API will render all messages that contain the text 'Microsoft' in the message's subject or body. Whereas, setting OutlookOptions.[AddressFilter](https://apireference.groupdocs.com/net/viewer/groupdocs.viewer.options/outlookoptions/properties/addressfilter)* *as 'susan' will filter messages that contain 'susan' as a part of the sender's or recipient's address. The following code samples show how to filter the messages.

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
    'FilePath': 'SampleFiles/sample.ost'
  },  
  'ViewFormat': 'HTML',
  'RenderOptions': {
    'OutlookOptions': {
      'TextFilter' : 'Microsoft',
      'AddressFilter' : 'susan'
    }
  }
}"

 ```


 Response
```html 

{
  "pages": [
    {
      "number": 1,
      "resources": null,
      "path": "viewer/sample_ost/sample_page_1.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_ost/sample_page_1.html"
    }
  ],
  "attachments": [
    {
      "name": "(Inbox)0.msg",
      "path": "viewer/sample_ost/attachments/(Inbox)0.msg",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_ost/attachments/(Inbox)0.msg"
    },
    {
      "name": "(Inbox)1.msg",
      "path": "viewer/sample_ost/attachments/(Inbox)1.msg",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_ost/attachments/(Inbox)1.msg"
    },
    {
      "name": "(Inbox)2.msg",
      "path": "viewer/sample_ost/attachments/(Inbox)2.msg",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_ost/attachments/(Inbox)2.msg"
    }
  ],
  "file": null
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
        FilePath # "SampleFiles/sample.ost"
    },
    ViewFormat # ViewOptions.ViewFormatEnum.HTML,
    RenderOptions # new HtmlOptions
    {
        OutlookOptions # new OutlookOptions
        {
            TextFilter # "Microsoft",
            AddressFilter # "susan"
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
fileInfo.setFilePath("SampleFiles/sample.ost");
ViewOptions viewOptions # new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.HTML);
HtmlOptions renderOptions # new HtmlOptions();            
OutlookOptions outlookOptions # new OutlookOptions();
outlookOptions.setTextFilter("Microsoft");
outlookOptions.setAddressFilter("susan");
renderOptions.setOutlookOptions(outlookOptions);
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
$fileInfo->setFilePath("SampleFiles/sample.ost");               
$viewOptions->setFileInfo($fileInfo);
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_HTML);
$renderOptions # new Model\HtmlOptions();
$outlookOptions # new Model\OutlookOptions();
$outlookOptions->setTextFilter("Microsoft");
$outlookOptions->setAddressFilter("susan");
$renderOptions->setOutlookOptions($outlookOptions);
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
fileInfo.filePath # "SampleFiles/sample.ost";
let viewOptions # new viewer_cloud.ViewOptions();
viewOptions.fileInfo # fileInfo;
viewOptions.viewFormat # viewer_cloud.ViewOptions.ViewFormatEnum.HTML;
viewOptions.renderOptions # new viewer_cloud.HtmlOptions();
viewOptions.renderOptions.outlookOptions # new viewer_cloud.OutlookOptions();     
viewOptions.renderOptions.outlookOptions.textFilter # "Microsoft";
viewOptions.renderOptions.outlookOptions.addressFilter # "susan";
 
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
view_options.file_info.file_path # "SampleFiles/sample.ost"
view_options.view_format # "HTML"
view_options.render_options # groupdocs_viewer_cloud.HtmlOptions()
view_options.render_options.outlook_options # groupdocs_viewer_cloud.OutlookOptions()    
view_options.render_options.outlook_options.text_filter # "Microsoft"
view_options.render_options.outlook_options.address_filter # "susan"
 
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
viewOptions.file_info.file_path # "SampleFiles/sample.ost"
viewOptions.view_format # "HTML"
viewOptions.render_options # GroupDocsViewerCloud::HtmlOptions.new
viewOptions.render_options.outlook_options # GroupDocsViewerCloud::OutlookOptions.new
viewOptions.render_options.outlook_options.text_filter # "Microsoft"
viewOptions.render_options.outlook_options.address_filter # "susan"
 
request # GroupDocsViewerCloud::CreateViewRequest.new(viewOptions)    
response # apiInstance.create_view(request)

 ```

