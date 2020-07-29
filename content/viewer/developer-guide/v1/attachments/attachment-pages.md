---
id: "attachment-pages"
url: "viewer/attachment-pages"
title: "Attachment Pages"
productName: "GroupDocs.Viewer Cloud"
weight: 3
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}










# Get Email Attachment Pages List for HTML Rrepresentation #

Sometimes, it is required to get email attachments as pages. You can retrieve list of attachment pages for HTML representation using following API. It returns object with list of attachment pages or ZIP archive with actual pages as HTML when "application/zip" accept header specified.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used in [retrieving pages list of email attachment (HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetAttachmentPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
{
  "fileName": "Test.msg",
  "folder": null,
  "attachmentName": "Freescale OSC.pdf",
  "pages": [
    {
      "number": 1,
      "resources": [
        {
          "name": "font.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/font.woff"
        },
        {
          "name": "font1.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/font1.woff"
        },
        {
          "name": "font2.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/font2.woff"
        },
        {
          "name": "image.png",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1/resources/styles.css"
        }
      ],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1"
    },
    {
      "number": 2,
      "resources": [
        {
          "name": "font.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/font.woff"
        },
        {
          "name": "font1.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/font1.woff"
        },
        {
          "name": "font2.woff",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/font2.woff"
        },
        {
          "name": "image.png",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/image.png"
        },
        {
          "name": "styles.css",
          "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2/resources/styles.css"
        }
      ],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Pages List of Attachments for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Pages_Html.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Pages_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Pages_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Pages_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachment_Pages_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Pages_HTML.py >}}









# Get Email Attachment Pages List for Image Representation #

GroupDocs.Viewer Cloud also supports to get email attachments pages list for  Image representation. You can retrieve list of attachment pages as image using following API. It returns object with list of attachment pages or ZIP archive with actual pages as Image when "application/zip" accept header specified.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used in the [retrieving pages list of email attachment (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetAttachmentPages).

## cURL Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
{
  "fileName": "Test.msg",
  "folder": null,
  "attachmentName": "Test.pdf",
  "pages": [
    {
      "number": 1,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/1"
    },
    {
      "number": 2,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/2"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Pages List of Attachments for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Pages_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Pages_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Pages_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Pages_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachment_Pages_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Pages_Image.py >}}









# Download ZIP Archive of Email Attachment Pages for HTML Representation #

You can download ZIP archive of email attachments pages for HTML representation using following API. Please check [ZIP Archive structure]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/zip-file-structure/) for more details.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to [download ZIP archive of attachment pages (HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetZipWithAttachmentPages).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/zip" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
ZIP Archive with document pages as HTML
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download Zip Archive of Attachment Pages for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Pages_ZIP_Html.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Pages_Zip_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Pages_ZIP_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Pages_Zip_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachment_Pages_Zip_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Pages_Zip_HTML.py >}}









# Download ZIP Archive of Email Attachment Pages for Image Representation #

You can download ZIP archive of email attachments pages for Image representation using following API. Please check [ZIP Archive structure]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/zip-file-structure/) for more details.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used in the [download ZIP archive of page attachments (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetZipWithAttachmentPages).

## cURL Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/zip" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
ZIP Archive with document pages as Image
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Download Zip Archive of Attachment Pages for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Pages_ZIP_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Pages_Zip_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Pages_ZIP_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Pages_Zip_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachment_Pages_Zip_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Pages_Zip_Image.py >}}







 

# Get Email Attachment Page for HTML Representation #

You can download a specific page of an email attachment, following API is used to get specific page of email attachment as HTML. It returns actual contents of the page.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used [to retrieve specific page of email attachment (HTML Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlGetAttachmentPage).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
Contents of Page as HTML
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get specific Page of Attachments for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Page_Html.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Page_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Page_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Page_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachment_Page_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Page_HTML.py >}}









# Get Email Attachment Page for Image Representation #

You can download a specific page of an email attachment, following API is used to get specific page of email attachment for Image Representation. It returns actual contents of the page.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used [to retrieve specific page of email attachment as Image](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageGetAttachmentPage).

## cURL Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/1" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9TdwZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
page Contents as Image
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Specific Page of Attachments for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Attachment_Page_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Attachment_Page_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_Attachment_Page_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Attachment_Page_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Attachment_Page_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Attachment_Page_Image.py >}}









# Create Email Attachment Pages Cache for HTML Representation #

You can create email attachment pages cache for HTML representation using following API. It expects [HtmlOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HHtmlOptionsObject||style#"background-color: transparent;" shape#"rect")  object data in request body and returns an object which contains list of links to attachment pages or ZIP archive with actual pages as HTML when "application/zip" accept header specified.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used [to create cache of email attachment pages( HTML Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlCreateAttachmentPagesCache).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"resourcePath": "page/1/resource/styles.css","embedResources": true,"startPageNumber": 1,"countPages": 3,"renderComments": false}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-
LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9Td
wZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-
6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-
vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
{
  "fileName": "Test.msg",
  "folder": null,
  "attachmentName": "Test.pdf",
  "pages": [
    {
      "number": 1,
      "resources": [],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/1"
    },
    {
      "number": 2,
      "resources": [],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/2"
    },
    {
      "number": 3,
      "resources": [],
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/3"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Attachments Pages Cache for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Attachment_Pages_Cache_Html.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Create_Attachment_Pages_Cache_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Attachment_Pages_Cache_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Attachment_Pages_Cache_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Attachment_Pages_Cache_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Attachment_Pages_Cache_HTML.py >}}









# Create Email Attachment Pages Cache for Image Representation #

You can create email attachment pages cache for Image representation using following API. It expects [ImageOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HHtmlOptionsObject) object data in request body and returns an object which contains list of links to attachment pages or ZIP archive with actual pages as HTML when "application/zip" accept header specified.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used [to create cache of email attachment pages (Image Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageCreateAttachmentPagesCache).

## cURL Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"ExtractText":true,"startPageNumber":1,"countPages":3}" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-
LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9Td
wZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-
6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-
vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
{
  "fileName": "Test.msg",
  "folder": null,
  "attachmentName": "Test.pdf",
  "pages": [
    {
      "number": 1,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/1"
    },
    {
      "number": 2,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/2"
    },
    {
      "number": 3,
      "url": "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/3"
    }
  ]
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Create Attachments Pages Cache for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Attachment_Pages_Cache_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Create_Attachment_Pages_Cache_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Create_Attachment_Pages_Cache_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Create_Attachment_Pages_Cache_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Create_Attachment_Pages_Cache_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Create_Attachment_Pages_Cache_Image.py >}}









# Remove Email Attachment Pages Cache #

You can delete email attachment pages cache for HTML presentation using following API. An empty response with '204 No Content' status will be returned to confirm deletion.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used [to remove email attachment pages cache (HTML Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/HtmlDeleteAttachmentPagesCache).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Test.pdf/pages/cache" \
-X DELETE \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-
LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9Td
wZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-
6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-
vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
Empty response with '204 No Content' status.
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Remove Attachments Pages Cache for Html Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Delete_Attachment_Pages_Cache_Html.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Delete_Attachment_Pages_Cache_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Delete_Attachment_Pages_Cache_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Delete_Attachment_Pages_Cache_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Delete_Attachment_Pages_Cache_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Delete_Attachment_Pages_Cache_HTML.py >}}









# Remove Email Attachment Pages Cache for Image Representation #

You can delete email attachment pages cache for Image Representation using following API. An empty response with '204 No Content' status will be returned to confirm deletion.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used [to delete cache of email attachment pages (Image Representation)](https://apireference.groupdocs.cloud/viewer/#!/Attachments/ImageDeleteAttachmentPagesCache).

## cURL Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/image/attachments/Test.pdf/pages/cache" \
-X DELETE \
-H "Content-Type: application/json" \
-H "authorization: Bearer pTPAHbcNbrMcerjvtBpYgfkSh44oB9uWBEhoLNLiJ3KYWTZ-
LjDK1OhIiSkiFnpwEDvAENURIo6NndadzqbW7Di4ZKIKC6DOlEGoFI2hfiNBaXEAGDE00knZePkCNsupU48qe1N_eGluq4urBAX3VBFiIdwz1yEPlPrqWG1DOAWYglUo5Nc9Td
wZroBiDJ00A0oKjWoEJ_mRsI_VYK-NnZlNqrUiPGd6918ivV-vTtN2VvqGGUAosz26F7NZe0uEDf5GZszp-bxQ4_-JimHUgOD3z2M4gldo58oYp-
6NBGCEjA312kqpxYZs22MJ_Ma-fSgT8yMDqgixItd0JxciHUCmSR8XVG803g1UgUF3-rfoWOn0FJAYLkZ3SFrjqMwjcJAsxcpWc-
vm2eLneOPAh8R08ATyhemGBNCh3Ke3jJhaMf92"


 ```




 Response

```html 
Empty response with '204 No Content' status.
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Remove Attachments Pages Cache for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Delete_Attachment_Pages_Cache_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Delete_Attachment_Pages_Cache_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Delete_Attachment_Pages_Cache_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Delete_Attachment_Pages_Cache_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Delete_Attachment_Pages_Cache_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Delete_Attachment_Pages_Cache_Image.py >}}







 

 