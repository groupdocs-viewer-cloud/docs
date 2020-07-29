---
id: "rename-email-fields"
url: "viewer/rename-email-fields"
title: "Rename email fields"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

 






# Introduction #

When rendering email messages, by default the API uses the English language to render field labels such as *From*, *To*, *Subject* etc. There might be the case when you want to change the label of the fields in email message's header.
GroupDocs.Viewer Cloud is flexible enough to allow you to use the custom field labels for email header. The API provides a new property FieldLabels in EmailOptions* *class to change the field labels.
\\Following code sample shows how to use custom field labels.

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
    'FilePath': 'SampleFiles/sample.msg'
  },  
  'ViewFormat': 'HTML',
  'RenderOptions': {
    'EmailOptions': {
      'FieldLabels': [
        {
          'Field': 'From',
          'Label': 'Sender'
        },
        {
          'Field': 'To',
          'Label': 'Receiver'
        }
      ]
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
      "path": "viewer/sample_msg/sample_page_1.html",
      "downloadUrl": "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewer/sample_msg/sample_page_1.html"
    }
  ],
  "attachments": [],
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
        FilePath # "SampleFiles/sample.msg"
    },
    ViewFormat # ViewOptions.ViewFormatEnum.HTML,
    RenderOptions # new HtmlOptions
    {
        EmailOptions # new EmailOptions
        {
            FieldLabels # new List<FieldLabel>
            {
                new FieldLabel {Field # "From", Label # "Sender"},
                new FieldLabel {Field # "To", Label # "Receiver"}
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
fileInfo.setFilePath("SampleFiles/sample.msg");
ViewOptions viewOptions # new ViewOptions();
viewOptions.setFileInfo(fileInfo);
viewOptions.setViewFormat(ViewFormatEnum.HTML);
HtmlOptions renderOptions # new HtmlOptions();            
EmailOptions emailOptions # new EmailOptions();
emailOptions.addFieldLabelsItem(GetFieldLabel("From", "Sender"));
emailOptions.addFieldLabelsItem(GetFieldLabel("To", "Receiver"));
renderOptions.setEmailOptions(emailOptions);
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
$fileInfo->setFilePath("SampleFiles/sample.msg");               
$viewOptions->setFileInfo($fileInfo);
$viewOptions->setViewFormat(Model\ViewOptions::VIEW_FORMAT_HTML);
$renderOptions # new Model\HtmlOptions();
$emailOptions # new Model\EmailOptions();
$emailOptions->setFieldLabels([
    self::GetFieldLabel("From", "Sender"),
    self::GetFieldLabel("To", "Receiver")
    ]);
$renderOptions->setEmailOptions($emailOptions);
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
fileInfo.filePath # "SampleFiles/sample.msg";
let viewOptions # new viewer_cloud.ViewOptions();
viewOptions.fileInfo # fileInfo;
viewOptions.viewFormat # viewer_cloud.ViewOptions.ViewFormatEnum.HTML;
viewOptions.renderOptions # new viewer_cloud.HtmlOptions();
viewOptions.renderOptions.emailOptions # new viewer_cloud.EmailOptions();
let fieldLabel1 # new viewer_cloud.FieldLabel();
fieldLabel1.field # "From";
fieldLabel1.label # "Sender";
let fieldLabel2 # new viewer_cloud.FieldLabel();
fieldLabel2.field # "To";
fieldLabel2.label # "Receiver";        
viewOptions.renderOptions.emailOptions.fieldLabels # [fieldLabel1, fieldLabel2];
 
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
view_options.file_info.file_path # "SampleFiles/sample.msg"
view_options.view_format # "HTML"
view_options.render_options # groupdocs_viewer_cloud.HtmlOptions()
view_options.render_options.email_options # groupdocs_viewer_cloud.EmailOptions()
field_label1 # groupdocs_viewer_cloud.FieldLabel()
field_label1.field # "From"
field_label1.label # "Sender"
field_label2 # groupdocs_viewer_cloud.FieldLabel()
field_label2.field # "To"
field_label2.label # "Receiver"       
view_options.render_options.email_options.field_labels # [field_label1, field_label2]
 
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
viewOptions.file_info.file_path # "SampleFiles/sample.msg"
viewOptions.view_format # "HTML"
viewOptions.render_options # GroupDocsViewerCloud::HtmlOptions.new
viewOptions.render_options.email_options # GroupDocsViewerCloud::EmailOptions.new
field_label1 # GroupDocsViewerCloud::FieldLabel.new
field_label1.field # "From"
field_label1.label # "Sender"
field_label2 # GroupDocsViewerCloud::FieldLabel.new
field_label2.field # "To"
field_label2.label # "Receiver"       
viewOptions.render_options.email_options.field_labels # [field_label1, field_label2]
 
request # GroupDocsViewerCloud::CreateViewRequest.new(viewOptions)    
response # apiInstance.create_view(request)

 ```

