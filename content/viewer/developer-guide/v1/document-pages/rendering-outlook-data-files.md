---
id: "rendering-outlook-data-files"
url: "viewer/rendering-outlook-data-files"
title: "Rendering Outlook Data Files"
productName: "GroupDocs.Viewer Cloud"
weight: 5
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}






# Render Outlook Data Files as HTML #

GroupDocs.Viewer Cloud allows rendering the items in Outlook Data Files (OST/PST) as HTML. [OutlookOptions]({{< ref "viewer/developer-guide/v1/common-resources/options-objects.md" >}}) is used to set rendering options for OST and PST formats. The API returns object which contains list of links to document pages and if pages already created will be removed from cache.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [Render Outlook Data file as HTML](https://apireference.groupdocs.cloud/viewer/#!/Rendering/HtmlCreatePagesCache).

## cURL REST Example ##





 Request

```html 
### Render Outlook Data file as HTML
curl --request POST \
  --url https://api.groupdocs.cloud/v1/viewer/data.pst/html/pages \
  --header 'authorization: Bearer [Access Token]' \
  --header 'content-type: application/json' \
  --data '{"outlookOptions": {"maxItemsInFolder": "10"}}'
  
### Retrieve created page
curl --request GET \
  --url https://api.groupdocs.cloud/v1/viewer/data.pst/html/pages/1 \
  --header 'authorization: Bearer [Access Token]'
 ```




 Response

```html 
{
  "fileName": "data.pst",
  "pages": [
    {
      "number": 1,
      "resources": [],
      "url": "http://api.groupdocs.cloud/v1/viewer/data.pst/html/pages/1"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Render Outlook Data Files as HTML ###

 





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Render_Outlook_Data_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_Php_Render_Outlook_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Render_Outlook_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Render_Outlook_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Render_Outlook_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Render_Outlook_HTML.py >}}






