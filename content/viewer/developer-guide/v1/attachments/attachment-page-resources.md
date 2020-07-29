---
id: "attachment-page-resources"
url: "viewer/attachment-page-resources"
title: "Attachment Page Resources"
productName: "GroupDocs.Viewer Cloud"
weight: 4
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}










# Download Resource of Email Attachments Page for HTML Representation #

You can download the resource of a specific email attachment page for HTML representation, [that is already created]({{< ref "viewer/developer-guide/_index.md" >}})attachments/attachment-pages/#HGetEmailAttachmentPagesListforHTMLRrepresentation). Following API helps to download HTML page resource (image, style, graphics or font), it returns actual data of HTML page resource.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download resource of Email attachment page(HTML Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetAttachmentPageResource).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/styles.css" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-
LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9Td
wZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-
6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-
vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
Contents of styles.css
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Resource of Email Attachment Page for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Page_Resource_Html.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Page_Resource_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Page_Resource_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Page_Resource_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachment_Page_Resource_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Page_Resource_HTML.py >}}







