---
id: "attachments"
url: "viewer/attachments"
title: "Attachments"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}










# HTML Representation of Email Attachments List #

You can list the email attachments for HTML representation. Attachments API lists the email attachments. It returns an object with list of attachments.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used in the [attachments list (HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetAttachments).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
{
  "fileName": "Test.msg",
  "folder": null,
  "attachments": [
    {
      "name": "Test.pdf",
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Email Attachments for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer-CSharp_Get_Attachments_Html.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachments_Html.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachments_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachments_Html.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachments_Html.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachments_Html.py >}}









# Image Representation of Email Attachments List #

GroupDocs.Viewer Cloud also supports to get email attachments list for Image representation. Attachments API helps to retrieves attachments list. It returns an object that contains list of attachments.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used in the [attachments list(Image representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetAttachments).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
{
  "fileName": "Test.msg",
  "folder": null,
  "attachments": [
    {
      "name": "Test.pdf",
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Email Attachments List for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachments_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachments_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachments_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachments_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachments_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachments_Image.py >}}









# Download Email Attachments for HTML Representation #

You can download actual data of an Email attachment by passing its name. API returns an object with actual data of specified attachment.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used in the [downloading an attachment (HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetAttachment).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
Contents of Test.Pdf attachment
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download an Email Attachment for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_From_Email_Html.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_From_Email_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_From_Email_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_From_Email_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachment_From_Email_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_From_Email_HTML.py >}}









# Download Email Attachments for Image Representation #

You can download actual data of an Email attachment by passing its name for Image representation. API returns an object with actual data of specified attachment.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used in the [downloading an attachment (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetAttachment).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
Contents of Test.Pdf attachment
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download an Email Attachment for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_From_Email_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_From_Email_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_From_Email_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_From_Email_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachment_From_Email_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_From_Email_Image.py >}}







 

 



 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_From_Email_HTML.py >}}





