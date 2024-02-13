---
id: "working-with-folder"
url: "viewer/working-with-folder"
title: "Working With Folder"
productName: "GroupDocs.Viewer Cloud"
weight: 5
description: "GroupDocs.Viewer Cloud Working With Folder"
keywords: "GroupDocs.Viewer Cloud, Working With Folder"
toc: True
---

## List Files

This API allows you to get a list of all files of a specific folder from the specified Cloud Storage. If you do not pass storage name API will find folder in GroupDocs Cloud Storage.

### List Files with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/) lets you to try out [List Files in a Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder/GetFilesList) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### List Files Request Parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### List Files with cURL

{{< tabs "list-files-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/folder/viewerdocs?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "value": [
    {
      "name": "four-pages.docx",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:35:38+00:00",
      "size": 8651,
      "path": "/viewerdocs/four-pages.docx"
    },
    ...
  ]
}
```
{{< /tab >}}
{{< /tabs >}}

### List Files with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-storage-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "list-files-with-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Files_List.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Get_Files_List.java >}}
{{< /tab >}}
{{< tab "PHP" >}}
{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Get_Files_List.php >}}
{{< /tab >}}
{{< tab "Node.js" >}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Files_List.js >}}
{{< /tab >}}
{{< tab "Python" >}}
{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Get_Files_List.py >}}
{{< /tab >}}
{{< tab "Ruby" >}}
{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Get_Files_List.rb >}}
{{< /tab >}}
{{< tab "Android" >}}
{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Get_Files_List.java >}}
{{< /tab >}}
{{< /tabs >}}

## Create New Folder

This API allows you to create a new Folder in the specified Cloud Storage. If you do not pass storage name API will create new Folder in default Cloud Storage.

### Create New Folder with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/) lets you to try out [Create Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder/CreateFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### Create New Folder Request Parameters

|Parameter|Description
|---|---
|**path**|Target folder’s path e.g. Folder1/Folder2/. The folders will be created recursively Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### Create New Folder with cURL

{{< tabs "create-folder-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X POST "https://api.groupdocs.cloud/v2.0/viewer/storage/folder/viewerdocs3?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "code": 200,
  "status": "OK"
}
```
{{< /tab >}}
{{< /tabs >}}

### Create New Folder with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-storage-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder/) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "create-folder-with-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Create_Folder.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Create_Folder.java >}}
{{< /tab >}}
{{< tab "PHP" >}}
{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Create_Folder.php >}}
{{< /tab >}}
{{< tab "Node.js" >}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Create_Folder.js >}}
{{< /tab >}}
{{< tab "Python" >}}
{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Create_Folder.py >}}
{{< /tab >}}
{{< tab "Ruby" >}}
{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Create_Folder.rb >}}
{{< /tab >}}
{{< tab "Android" >}}
{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Create_Folder.java >}}
{{< /tab >}}
{{< /tabs >}}

## Delete Folder

This API allows you to delete a particular Folder in the specified Cloud Storage. If you do not pass storage name API will create new Folder in default Cloud Storage. To remove recursively inner folder/files you need to pass true value to recursive parameter in Request. If it is set to false and folder contains data then API throws the exception.

### Delete Folder with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you to try out [Delete a Particular Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder/DeleteFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### Delete Folder Request Parameters

|Parameter|Description
|---|---
|**path**|Folder path e.g. /Folder1 Required. Can be passed as query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### Delete Folder with cURL

{{< tabs "delete-folder-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X DELETE "https://api.groupdocs.cloud/v2.0/viewer/storage/folder/viewerdocs3?storageName#MyStorage&#x26;recursive#true" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "code": 200,
  "status": "OK"
}
```
{{< /tab >}}
{{< /tabs >}}

### Delete Folder with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Delete Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder/DeleteFolder) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "delete-folder-with-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Delete_Folder.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Delete_Folder.java >}}
{{< /tab >}}
{{< tab "PHP" >}}
{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Delete_Folder.php >}}
{{< /tab >}}
{{< tab "Node.js" >}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Delete_Folder.js >}}
{{< /tab >}}
{{< tab "Python" >}}
{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Delete_Folder.py >}}
{{< /tab >}}
{{< tab "Ruby" >}}
{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Delete_Folder.rb >}}
{{< /tab >}}
{{< tab "Android" >}}
{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Delete_Folder.java >}}
{{< /tab >}}
{{< /tabs >}}

## Copy Folder

This API allows you to copy a Folder to another location in the GroupDocs Cloud Storage. If you do not pass source and destination storage names API will copy Folder within default Cloud Storage.

### Copy Folder with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you to try out [Copy Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder/CopyFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### Request parameters

|Parameter|Description
|---|---
|**srcPath**|Source folder path e.g. /Folder1 Required. Can be passed as query string parameter or as part of the URL
|**destPath**|Destination folder path. Required
|srcStorageName|Name of the storage of source folder. If not set, then default storage used
|destStorageName|Name of the storage of destination folder. If not set, then default storage used

### Copy Folder with cURL

{{< tabs "copy-folder-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X PUT "https://api.groupdocs.cloud/v2.0/viewer/storage/folder/copy/viewerdocs?destPath#viewerdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "code": 200,
  "status": "OK"
}
```
{{< /tab >}}
{{< /tabs >}}

### Copy Folder with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Copy Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder/CopyFolder) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "copy-folder-with-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Copy_Folder.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Copy_Folder.java >}}
{{< /tab >}}
{{< tab "PHP" >}}
{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Copy_Folder.php >}}
{{< /tab >}}
{{< tab "Node.js" >}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Copy_Folder.js >}}
{{< /tab >}}
{{< tab "Python" >}}
{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Copy_Folder.py >}}
{{< /tab >}}
{{< tab "Ruby" >}}
{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Copy_Folder.rb >}}
{{< /tab >}}
{{< tab "Android" >}}
{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Copy_Folder.java >}}
{{< /tab >}}
{{< /tabs >}}

## Move Folder

This API allows you to move a Folder to another location in the GroupDocs Cloud Storage. If you do not pass source and destination storage names API will move Folder within default Cloud Storage.

### Move Folder with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you to try out [Move a Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder/MoveFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs exposes.

### Move Folder Request Parameters

|Parameter|Description
|---|---
|**srcPath**|Source folder path e.g. /Folder1 Required. Can be passed as query string parameter or as part of the URL
|**destPath**|Destination folder path. Required
|srcStorageName|Name of the storage of source folder. If not set, then default storage used
|destStorageName|Name of the storage of destination folder. If not set, then default storage used

### Move Folder with cURL

{{< tabs "move-folder-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X PUT "https://api.groupdocs.cloud/v2.0/viewer/storage/folder/move/viewerdocs?destPath#viewerdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "code": 200,
  "status": "OK"
}
```
{{< /tab >}}
{{< /tabs >}}


### Move Folder with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Move Folder API](https://apireference.groupdocs.cloud/viewer/#/Folder/MoveFolder) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "move-folder-with-sdk">}}
{{< tab "C#" >}}
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Move_Folder.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Move_Folder.java >}}
{{< /tab >}}
{{< tab "PHP" >}}
{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Move_Folder.php >}}
{{< /tab >}}
{{< tab "Node.js" >}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Move_Folder.js >}}
{{< /tab >}}
{{< tab "Python" >}}
{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Move_Folder.py >}}
{{< /tab >}}
{{< tab "Ruby" >}}
{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Move_Folder.rb >}}
{{< /tab >}}
{{< tab "Android" >}}
{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Move_Folder.java >}}
{{< /tab >}}
{{< /tabs >}}
