---
id: "getting-started"
url: "viewer/getting-started"
title: "Getting Started"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

## Overview ##

This section introduces GroupDocs.Viewer Cloud specific Resources & Operations.

#### Base URI ####

```html 

https://api.groupdocs.cloud/v2.0/viewer/

 ```

In the rest of the documentation base, URI presented as '~~' character.

#### Input & Output Format ####

GroupDocs.Viewer cloud supports request body data and response data formatted as JSON.

#### Errors ####

GroupDocs.Viewer Cloud API performs communication errors by using HTTP Status Codes with details passed in JSON or XML objects.

The main patterns are:
2xx - The request was received and accepted.
4xx - Error occurred while processing the request. An invalid parameter or the missing file can cause this error.
5xx - The request was received and accepted, but an error occurred in the GroupDocs.Viewer Cloud service while processing it.

###### HTTP Status Codes ######

|Code|Description
|---|---
|200|The request has succeeded.
|201|The request has been fulfilled and resulted in a new resource being created.
|204|The request has been fulfilled and resource(s) were removed.
|400|Failed to handle the request due to invalid parameters or missing resources.
|401|Authorization failed.
|404|The Requested resource was not found.
|405|The Requested method is not allowed.
|500|Internal server error occurred while processing the request.


###### Example Error Response ######

```html 

Status: 404 Not Found

 ```

```html 

{
  "error": {
    "code": "FileNotFound",
    "message": "Can't find file with given name 'document.doc' and folder 'My Documents'."
  }
}

 ```

###### Error Codes ######

|Error Code|Status Code|Description
|---|---|---
|FileNotFound|Not Found (404) |Indicates that the file was not found. 
|AttachmentNotFound |Not Found (404) |Indicates that the attachment was not found. 
|FontsPathNotFound|Not Found (404) |It Indicates that the specified fonts path can not be found.
|MissingPassword |Forbidden (403)|Indicates that the password was not provided to open the document. 
|IncorrectPassword|Forbidden (403) |It indicates that the provided password is incorrect. 
|FailedToReadFile |Bad Request (400) |It Indicates that the Viewer could not read the file. The File can be corrupted or damaged. 
|UnsupportedFileType |Bad Request (400) |This indicates that the provided file has a format that is not supported. 
|MissingFileInfo|Bad Request (400) |This indicates that the parameter 'FileInfo' was not specified.
|MissingParameters|Bad Request (400)|Indicates that request parameters missing or have the incorrect format.


#### Contents: ####





 
