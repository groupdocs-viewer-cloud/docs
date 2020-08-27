---
id: "working-with-files"
url: "viewer/working-with-files"
title: "Working With Files"
productName: "GroupDocs.Viewer Cloud"
weight: 4
description: "GroupDocs.Viewer Cloud Working With Files"
keywords: "GroupDocs.Viewer Cloud, Working With Files"
---

## Download File API

This API allows you to download a file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### Download File with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you to try out [Download a File API](https://apireference.groupdocs.cloud/viewer/#/File/DownloadFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### Download File Request Parameters

|Parameter|Description
|---|---
|**Path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### Download File with cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/file/one-page.docx?storageName#MyStorage" -H  "accept: multipart/form-data" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### Download File with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### Download File with C\# SDK

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Download_File.cs >}}

#### Download File with PHP SDK

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Download_File.php >}}

#### Download File with Java SDK

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Download_File.java >}}

#### Download File with Ruby SDK

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Download_File.rb >}}

#### Download File with Node.js SDK

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Download_File.js >}}

#### Download File with Python SDK

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Download_File.py >}}

## Upload File API

This API allows you to upload files to the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### Upload File with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you try out [Upload a File API](https://apireference.groupdocs.cloud/viewer/#/File/UploadFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### Upload File Request Body Parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|File|File content

### Upload File with cURL

{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewerdocs%2Fone-page2.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
HTTP status code: 200
```

{{< /tab >}} {{< /tabs >}}

```json
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2019-02-27T06:10:08.884Z"
      }
    }
  ]
}
```

### Upload File with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

#### Upload File with C# SDK

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Upload_File.cs >}}

#### Upload File with PHP SDK

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Upload_File.php >}}

#### Upload File with Java SDK

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Upload_File.java >}}

#### Upload File with Ruby SDK

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Upload_File.rb >}}

#### Upload File with Node.js SDK

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Upload_File.js >}}

#### Upload File with Python SDK

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Upload_File.py >}}

## Delete File API

This API allows you to delete specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### Delete File with API Explorer

[GroupDocs.Viewer for Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you to try out [Delete a File](https://apireference.groupdocs.cloud/viewer/#/File/DeleteFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### Delete File Request Parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### Delete File with cURL

{{< tabs tabTotal="2" tabID="3" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewerdocs1%2Fone-page1.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### Delete File with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

#### Delete File with C# SDK

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Delete_File.cs >}}

#### Delete File with PHP SDK

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Delete_File.php >}}

#### Delete File with Java SDK

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Delete_File.java >}}

#### Delete File with Ruby SDK

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Delete_File.rb >}}

#### Delete File with Node.js SDK

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Delete_File.js >}}

#### Delete File with Python SDK

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Delete_File.py >}}

## File Copy API

This API allows you to copy specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### File Copy with API Explorer

[GroupDocs.Viewer for Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you to try out [Copy File](https://apireference.groupdocs.cloud/viewer/#/File/CopyFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### File Copy Request Parameters

|Parameter|Description
|---|---
|**srcPath**|Path of the source file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|**destPath**|Path of the destination file. Required.
|srcStorageName|Name of the storage of source file. If not set, then default storage used
|destStorageName|Name of the storage of destination file. If not set, then default storage used
|versionId|Source file version id

### File Copy with cURL

{{< tabs tabTotal="2" tabID="4" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.groupdocs.cloud/v2.0/viewer/storage/file/copy/viewerdocs%2Fone-page1.docx?destPath#viewerdocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### File Copy with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### File Copy with C# SDK

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Copy_File.cs >}}

#### File Copy with PHP SDK

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Copy_File.php >}}

#### File Copy with Java SDK

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Copy_File.java >}}

#### File Copy with Ruby SDK

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Copy_File.rb >}}

#### File Copy with Node.js SDK

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Copy_File.js >}}

##### File Copy with Python SDK

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Copy_File.py >}}

## File Move API

This API allows you to copy specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### File Move with API Explorer

[GroupDocs.Viewer for Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you to try out [Move File](https://apireference.groupdocs.cloud/viewer/#/File/MoveFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### File Move Request Parameters

|Parameter|Description
|---|---
|**srcPath**|Path of the source file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|**destPath**|Path of the destination file. Required.
|srcStorageName|Name of the storage of source file. If not set, then default storage used
|destStorageName|Name of the storage of destination file. If not set, then default storage used
|versionId|Source file version id

### File Move with cURL

{{< tabs tabTotal="2" tabID="5" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.groupdocs.cloud/v2.0/viewer/storage/file/move/viewerdocs%2Fone-page1.docx?destPath#viewerdocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}} {{< /tabs >}}

### File Move with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

#### File Move with C# SDK

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Move_File.cs >}}

#### File Move with PHP SDK

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Move_File.php >}}

#### File Move with Java SDK

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Move_File.java >}}

#### File Move with Ruby SDK

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Move_File.rb >}}

#### File Move with Node.js SDK

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Move_File.js >}}

#### File Move with Python SDK

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Move_File.py >}}
