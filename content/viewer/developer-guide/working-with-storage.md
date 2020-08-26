---
id: "working-with-storage"
url: "viewer/working-with-storage"
title: "Working With Storage"
productName: "GroupDocs.Viewer Cloud"
weight: 6
description: "GroupDocs.Viewer Cloud Working With Storage"
keywords: "GroupDocs.Viewer Cloud, Working With Storage"
---

## Check Storage Exist API

This API intended for checking the existence of cloud storage with a given name from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### Check Storage Exist with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/viewer/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### Check Storage Exist Request Parameters

|Parameter|Description
|---|---
|**storageName**|Storage name

### Check Storage Exist with cURL

Request

```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/MyStorage/exist" -H  "accept: application/json" -H  "authorization: Bearer  [Access Token]"
```

Response

```json
{
  "exists": true
}
```

### Check Storage Exist with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Storage existence](https://apireference.groupdocs.cloud/viewer/#/Storage/StorageExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### Check Storage Exist with C# SDK

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Storage_Exist.cs >}}

#### Check Storage Exist with PHP SDK

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Storage_Exist.php >}}

#### Check Storage Exist with Java SDK

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Storage_Exist.java >}}

#### Check Storage Exist with Ruby SDK

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Storage_Exist.rb >}}

#### Check Storage Exist with Node.js SDK

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Storage_Exist.js >}}

#### Check Storage Exist with Python SDK

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Storage_Exist.py >}}

## Check Storage Object Exist API

This API intended for checking existence of file or folder in [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### Check Storage Object Exist with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/viewer/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Check Storage Object Exist Request Parameters

|Parameter|Description
|---|---
|**path**|Path of the file or folder Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### Check Storage Object Exist with cURL

Request

```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/exist/viewerdocs?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

Response

```json
{
  "exists": true,
  "isFolder": true
}
```

### Check Storage Object Exist with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Storage Object existence](https://apireference.groupdocs.cloud/viewer/#/Storage/ObjectExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### Check Storage Object Exist with C# SDK

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Object_Exists.cs >}}

#### Check Storage Object Exist with PHP SDK

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Object_Exists.php >}}

#### Check Storage Object Exist with Java SDK

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Object_Exists.java >}}

#### Check Storage Object Exist with Ruby SDK

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Object_Exists.rb >}}

#### Check Storage Object Exist with Node.js SDK

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Object_Exists.js >}}

#### Check Storage Object Exist with Python SDK

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Object_Exists.py >}}

## Storage Space Usage API

This API intended for getting total and used space of the[ GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### Storage Space Usage with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you try out [storage space usage API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetDiscUsage) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Storage Space Usage Request parameters

|Parameter|Description
|---|---
|storageName|Name of the storage. If not set, then default storage used

### Storage Space Usage with cURL

Request

```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/disc?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

Response

```json
{
  "usedSize": 31032368,
  "totalSize": 3221225472
}
```

### Storage Space Usage with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [storage space usage API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetDiscUsage) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### Storage Space Usage with C# SDK

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Disc_Usage.cs >}}

#### Storage Space Usage with PHP SDK

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Get_Disc_Usage.php >}}

#### Storage Space Usage with Java SDK

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Get_Disc_Usage.java >}}

#### Storage Space Usage with Ruby SDK

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Get_Disc_Usage.rb >}}

#### Storage Space Usage with Node.js SDK

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Disc_Usage.js >}}

#### Storage Space Usage with Python SDK

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Get_Disc_Usage.py >}}

## Storage File Versions API

This API intended for getting the list of file versions, stored in the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### Storage File Versions with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you try out [Storage File Versions API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetFileVersions) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Storage File Versions Request parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### Storage File Versions with cURL

Request

```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/version/one-page.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

Response

```json
{
  "value": [
    {
      "versionId": "null",
      "isLatest": true,
      "name": "one-page.docx",
      "isFolder": false,
      "modifiedDate": "2018-08-16T19:45:05+00:00",
      "size": 347612,
      "path": "/one-page.docx"
    }
  ]
}
```

### Storage File Versions with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Storage File Versions API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetFileVersions) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### Storage File Versions with C# SDK

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_File_Versions.cs >}}

#### Storage File Versions with PHP SDK

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Get_File_Versions.php >}}

#### Storage File Versions with Java SDK

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Get_File_Versions.java >}}

#### Storage File Versions with Ruby SDK

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Get_File_Versions.rb >}}

#### Storage File Versions with Node.js SDK

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_File_Versions.js >}}

#### Storage File Versions with Python SDK

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Get_File_Versions.py >}}
