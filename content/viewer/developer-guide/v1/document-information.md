---
id: "document-information"
url: "viewer/document-information"
title: "Document Information"
productName: "GroupDocs.Viewer Cloud"
weight: 14
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}






# Get Document Information for HTML Representation #

This API retrieves document information. It returns an object that contains information about file format and file size. It also Includes information about document pages and attachments

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information(HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/HtmlGetDocumentInfo).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/info" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
  "fileName": "Test.msg",
  "extension": ".msg",
  "fileFormat": "Microsoft Outlook Mail Message",
  "size": 99840,
  "dateModified": "2018-02-07T05:10:43Z",
  "pages": [
    {
      "number": 1,
      "name": "",
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true
    }
  ],
  "attachments": [
    {
      "name": "password-protected.docx",
      "extension": ".docx",
      "fileFormat": "Microsoft Word"
    }
  ],
  "startDate": "0001-01-01T00:00:00",
  "endDate": "0001-01-01T00:00:00"
}
 
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_Html.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Document_Info_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Document_Info_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Document_Info_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Document_Info_HTML.py >}}









# Get Document Information for Image Representation #

GroupDocs.Viewer Cloud also supports to retrieves document information for Image representation. This API returns an object that contains information about file format and file size. It also Includes information about document pages and attachments.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/ImageGetDocumentInfo).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/one-page.docx/image/info?extractText#true" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"


 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "extension": ".docx",
  "fileFormat": "Microsoft Word",
  "size": 14252,
  "dateModified": "2017-03-28T16:44:52.7520812Z",
  "pages": [
      {
        "number": 1,
        "name": null,
        "width": 612,
        "height": 792,
        "angle": 0,
        "visible": true,
        "rows": [
            {
              "text": "First Page",
              "rowLeft": 85.05,
              "rowTop": 58.033,
              "rowWidth": 43.494,
              "rowHeight": 12.1,
              "textCoordinates": [
                85.05,
                19.404,
                106.94,
                21.604
              ],
              "characterCoordinates": [
                85.05,
                90.099,
                92.629,
                96.468,
                100.769,
                106.94,
                112.616,
                117.885,
                123.066
              ]
            }
         ]
      }
    ]
  },
  "attachments": [],
  "startDate": "0001-01-01T00:00:00",
  "endDate": "0001-01-01T00:00:00"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Document_Info_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Document_Info_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Document_Info_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Document_Info_Image.py >}}









# Get Document Information from URL for HTML Representation #

You can get document information for a document at provided URL for HTML representation. Following API retrieves file from specified URL and tries to detect file type when fileName parameter is not specified. It saves retrieved file in storage, use fileName and folder parameters to specify desired file name and folder to save file.

When file with specified name already exists in storage new unique file name will be used. It also returns object that contains information about file format and file size along with information about document pages and attachments.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information from URL(HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/HtmlGetDocumentInfoFromUrl).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/html/info?url#https%3a%2f%2fwww.dropbox.com%2fs%2fumokluz338w4ng7%2fone-page.docx%3fdl%3d1" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "extension": ".docx",
  "fileFormat": "Microsoft Word",
  "size": 14252,
  "dateModified": "2017-06-15T11:39:25.9611296Z",
  "pages": [
      {
        "number": 1,
        "name": null,
        "width": 612,
        "height": 792,
        "angle": 0,
        "visible": true,
        "rows": null
      }
  ],
  "attachments": [],
  "startDate": "0001-01-01T00:00:00",
  "endDate": "0001-01-01T00:00:00"
} 
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information from URL for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_URL_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Document_Info_URL_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_URL_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Document_Info_URL_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Document_Info_URL_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Document_Info_URL_HTML.py >}}









# Get Document Information from URL for Image Representation #

GroupDocs.Viewer for Cloud also supports to get document information for a document at provided URL as Image representation. Following API retrieves file from specified URL and tries to detect file type when fileName parameter is not specified. It saves retrieved file in storage, use fileName and folder parameters to specify desired file name and folder to save file.

When file with specified name already exists in storage new unique file name will be used. It also returns object that contains information about file format and file size along with information about document pages and attachments.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information from URL (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/ImageGetDocumentInfoFromUrl).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/image/info?url#https%3a%2f%2fwww.dropbox.com%2fs%2fumokluz338w4ng7%2fone-page.docx%3fdl%3d1&#x26;extractText#true&#x26;extractText#true" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer [Access Token]"


 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "folder": null,
  "extension": ".docx",
  "fileFormat": "Microsoft Word",
  "size": 14252,
  "dateModified": "2017-06-15T14:10:59.8956848Z",
  "pages":  [
      {
        "number": 1,
        "name": null,
        "width": 612,
        "height": 792,
        "angle": 0,
        "visible": true,
        "rows": [
            {
              "text": "First Page",
              "rowLeft": 85.05,
              "rowTop": 58.033,
              "rowWidth": 43.494,
              "rowHeight": 12.1,
              "textCoordinates": [
                85.05,
                19.404,
                106.94,
                21.604
              ],
              "characterCoordinates": [
                85.05,
                90.099,
                92.629,
                96.468,
                100.769,
                106.94,
                112.616,
                117.885,
                123.066
              ]
            }
         ]
      }
    ]
  },
  "attachments": [],
  "startDate": "0001-01-01T00:00:00",
  "endDate": "0001-01-01T00:00:00"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information from URL for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_URL_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Document_Info_URL_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_URL_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Document_Info_URL_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Document_Info_URL_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Document_Info_URL_Image.py >}}









# Get Document Information with DocumentInfoOptions for HTML Representation #

You can get document information for a document with specified [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject). API expects [DocumentInfoOptions ]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject)object data in request body. It returns an object that contains information about file format and file size. It also Includes information about document pages and attachments.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information with DocumentInfoOptions(HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/HtmlGetDocumentInfoWithOptions).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/excel.xlsx/html/info" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"cellsOptions":{"renderGridLines":true,"paginateSheets":true,"encoding": null,"internalHyperlinkPrefix":"prefix","countRowsPerPage":60,"textOverflowMode":"HideText","ignoreEmptyRows":false}}" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
  "fileName": "excel.xlsx",
  "extension": ".xlsx",
  "fileFormat": "Microsoft Excel",
  "size": 7825,
  "dateModified": "2017-06-15T11:39:25.9611296Z",
  "pages": [
    {
      "number": 1,
      "name": "Sheet1",
      "width": 342,
      "height": 165,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ],
  "attachments": [],
  "startDate": "0001-01-01T00:00:00",
  "endDate": "0001-01-01T00:00:00"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information with DocumentInfoOptions for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_with_Options_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Document_Info_With_Options_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_with_Options_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Document_Info_With_Options_HTML.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Document_Info_With_Options_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Document_Info_With_Options_HTML.py >}}









# Get Document Information with DocumentInfoOptions for Image Representation #

GroupDocs.Viewer for Cloud also supports to get document information for a document with specified [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject) as Image representation. API expects [DocumentInfoOptions ]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject)object data in request body. It returns an object that contains information about file format and file size. It also Includes information about document pages and attachments.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information with DocumentInfoOptions (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/ImageGetDocumentInfoWithOptions).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/excel.xlsx/image/info" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"cellsOptions":{"renderGridLines":true,"textOverflowMode":"HideText"}}" \
-H "authorization: Bearer [Access Token]"


 ```




 Response

```html 
{
  "fileName": "excel.xlsx",
  "extension": ".xlsx",
  "fileFormat": "Microsoft Excel",
  "size": 7825,
  "dateModified": "2017-06-15T14:10:59.8956848Z",
  "pages": [
    {
      "number": 1,
      "name": "Sheet1",
      "width": 208,
      "height": 21,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ],
  "attachments": [],
  "startDate": "0001-01-01T00:00:00",
  "endDate": "0001-01-01T00:00:00"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information with DocumentInfoOptions for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_with_Options_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Document_Info_With_Options_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_with_Options_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Document_Info_With_Options_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Document_Info_With_Options_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Document_Info_With_Options_Image.py >}}









# Get Document Information for Document Passed in Request Body for HTML Representation #

You can retrieve document information for posted document. API saves file in storage. It uses fileName and folder parameters to specify desired file name and folder to save file. When file with specified name already exists in storage new unique file name will be used for file.

API also returns an object that contains information about file format, file size, information about document pages and attachments. We can pass document content or multipart content where first part is document and second is [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject) object data to request body.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information of document passed in request body(HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/HtmlGetDocumentInfoFromContent).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/html/info?fileName#one-page.docx" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"cellsOptions":{"renderGridLines":true,"paginateSheets":true,"encoding": null,"internalHyperlinkPrefix":"prefix","countRowsPerPage":60,"textOverflowMode":"HideText","ignoreEmptyRows":false}}" \
-H "authorization: Bearer [Access Token]"
 
 ```




 Response

```html 
{
    "fileName": "one-page.docx",
    "folder": null,
    "extension": ".docx",
    "fileFormat": "Microsoft Word",
    "size": 14252,
    "dateModified": "2017-06-15T12:03:04.1474906Z",
    "pages": [
        {
            "number": 1,
            "name": null,
            "width": 612,
            "height": 792,
            "angle": 0,
            "visible": true,
            "rows": null
        }
    ],
    "attachments": [],
  "startDate": "0001-01-01T00:00:00",
  "endDate": "0001-01-01T00:00:00"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information of Document Passed in Request Body for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_From_Request_Html.cs >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_From_Request_Html.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_DocumentInfo_From_Request_Html.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_DocumentInfo_From_Request_Html.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_DocumentInfo_From_Request_Html.py >}}









# Get Document Information for Document Passed in Request Body for Image Representation #

You can retrieve document information for posted document for image representation. API saves file in storage. It uses fileName and folder parameters to specify desired file name and folder to save file. When file with specified name already exists in storage new unique file name will be used for file.

API also returns an object that contains information about file format, file size, information about document pages and attachments. We can pass document content or multipart content where first part is document and second is [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject) object data to request body.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information for document passed in request body (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/ImageGetDocumentInfoFromContent).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/image/info?fileName#one-page.docx" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"wordsOptions":{"renderTrackedChanges":false}}" \
-H "authorization: Bearer [Access Token]"


 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "extension": ".docx",
  "fileFormat": "Microsoft Word",
  "size": 47,
  "dateModified": "2017-06-15T12:03:04.1474906Z",
  "pages": [
    {
      "number": 1,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ],
  "attachments": [],
  "startDate": "0001-01-01T00:00:00",
  "endDate": "0001-01-01T00:00:00"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information of Document Passed in Request Body for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_From_Request_Image.cs >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_From_Request_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_DocumentInfo_From_Request_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_DocumentInfo_From_Request_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_DocumentInfo_From_Request_Image.py >}}









# Get Document Information from URL with DocumentInfoOptions for HTML Representation #

You can retrieve document information for document from provided URL for HTML representation. The API retrieves document information with specified [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject).

It expects [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject) object data in request body.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information from URL with DocumentInfoOptions (HTML representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/HtmlGetDocumentInfoFromUrlWithOptions).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/html/info?url#https%3a%2f%2fwww.dropbox.com%2fs%2fumokluz338w4ng7%2fone-page.docx%3fdl%3d1" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"wordsOptions":{"renderTrackedChanges":false}}" \
-H "authorization: Bearer [Access Token]"

 
 ```




 Response

```html 
{
    "fileName": "one-page.docx",
    "folder": null,
    "extension": ".docx",
    "fileFormat": "Microsoft Word",
    "size": 14252,
    "dateModified": "2017-06-15T12:03:04.1474906Z",
    "pages": [
        {
            "number": 1,
            "name": null,
            "width": 612,
            "height": 792,
            "angle": 0,
            "visible": true,
            "rows": null
        }
    ],
    "attachments": [],
    "startDate": "0001-01-01T00:00:00",
    "endDate": "0001-01-01T00:00:00"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information from URL with DocumentInfoOptions for HTML Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_with_Options_URL_HTML.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Document_Info_WithOptions_URL_HTML.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_with_Options_URL_HTML.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Document_Info_With_Options_HTML.rb
             >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Document_Info_With_Options_HTML.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Document_Info_With_Options_HTML.py >}}









# Get Document Information from URL with DocumentInfoOptions for Image Representation #

You can retrieve document information for document from provided URL for HTML representation. The API retrieves document information with specified [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject).

It expects [DocumentInfoOptions]({{< ref "viewer/developer-guide/_index.md" >}})common-resources/options-objects/#HDocumentInfoOptionsObject) object data in request body.

## Resource ##

The following GroupDocs.Viewer Cloud REST API resource has been used to get [document information from URL with DocumentInfoOptions (Image representation)](https://apireference.groupdocs.cloud/viewer/#!/File_Info/ImageGetDocumentInfoFromUrlWithOptions).

## cURL REST Example ##





 Request

```html 
curl -v "https://api.groupdocs.cloud/v1/viewer/image/info?url#https%3a%2f%2fwww.dropbox.com%2fs%2fumokluz338w4ng7%2fone-page.docx%3fdl%3d1" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-d "{"wordsOptions":{"renderTrackedChanges":false}}" \
-H "authorization: Bearer [Access Token]"


 ```




 Response

```html 
{
  "fileName": "one-page.docx",
  "extension": ".docx",
  "fileFormat": "Microsoft Word",
  "size": 47,
  "dateModified": "2017-06-15T12:03:04.1474906Z",
  "pages": [
    {
      "number": 1,
      "name": null,
      "width": 612,
      "height": 792,
      "angle": 0,
      "visible": true,
      "rows": null
    }
  ],
  "attachments": [],
  "startDate": "0001-01-01T00:00:00",
  "endDate": "0001-01-01T00:00:00"
}
 ```






## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### Get Document Information from URL with DocumentInfoOptions for Image Representation ###





 C#




{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_DocumentInfo_with_Options_URL_Image.cs >}}







 PHP




{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_Document_Info_WithOptions_URL_Image.php >}}







 Java




{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_DocumentInfo_with_Options_URL_Image.java >}}







 Ruby




{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_Document_Info_With_Options_Image.rb >}}







 Node.js




{{< gist groupdocscloud b1f41cc6e7c5c3179441554d37ecbfc9 Viewer_Node_Get_Document_Info_With_Options_Image.js >}}







 Python




{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_Document_Info_With_Options_Image.py >}}







