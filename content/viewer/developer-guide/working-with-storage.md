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

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/MyStorage/exist" -H  "accept: application/json" -H  "authorization: Bearer  [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "exists": true
}
```

{{< /tab >}} {{< /tabs >}}

### Check Storage Exist with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Storage existence](https://apireference.groupdocs.cloud/viewer/#/Storage/StorageExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs tabTotal="7" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" tabName7="Android" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Storage_Exist.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Storage_Exist.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Storage_Exist.java >}}

{{< /tab >}}  {{< tab tabNum="7" >}}

{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Storage_Exist.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Storage_Exist.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Storage_Exist.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Storage_Exist.py >}}

{{< /tab >}} {{< /tabs >}}

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

{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/exist/viewerdocs?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "exists": true,
  "isFolder": true
}
```

{{< /tab >}} {{< /tabs >}}

### Check Storage Object Exist with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Storage Object existence](https://apireference.groupdocs.cloud/viewer/#/Storage/ObjectExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs tabTotal="7" tabID="11" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" tabName7="Android" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Object_Exists.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Object_Exists.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Object_Exists.java >}}

{{< /tab >}} {{< tab tabNum="7" >}}

{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Object_Exists.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Object_Exists.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Object_Exists.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Object_Exists.py >}}

{{< /tab >}} {{< /tabs >}}

## Storage Space Usage API

This API intended for getting total and used space of the[ GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### Storage Space Usage with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you try out [storage space usage API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetDiscUsage) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Storage Space Usage Request parameters

|Parameter|Description
|---|---
|storageName|Name of the storage. If not set, then default storage used

### Storage Space Usage with cURL

{{< tabs tabTotal="2" tabID="3" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/disc?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```json
{
  "usedSize": 31032368,
  "totalSize": 3221225472
}
```

{{< /tab >}} {{< /tabs >}}

### Storage Space Usage with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [storage space usage API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetDiscUsage) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs tabTotal="7" tabID="12" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" tabName7="Android" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_Disc_Usage.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Get_Disc_Usage.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Get_Disc_Usage.java >}}

{{< /tab >}}  {{< tab tabNum="7" >}}

{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Get_Disc_Usage.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Get_Disc_Usage.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_Disc_Usage.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Get_Disc_Usage.py >}}

{{< /tab >}} {{< /tabs >}}

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

{{< tabs tabTotal="2" tabID="4" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/version/one-page.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```

{{< /tab >}} {{< tab tabNum="2" >}}

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

{{< /tab >}} {{< /tabs >}}

### Storage File Versions with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Storage File Versions API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetFileVersions) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs tabTotal="7" tabID="13" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" tabName7="Android" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_File_Versions.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 5fd8210b5b3e38cfaffee952036b264a Viewer_Php_Get_File_Versions.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Get_File_Versions.java >}}

{{< /tab >}}  {{< tab tabNum="7" >}}

{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Get_File_Versions.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud cb1b9fbd2cc419d83ca2c2dd1d7fcfc5 Viewer_Ruby_Get_File_Versions.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_File_Versions.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 46af986198f1d3f84ef2db07ef9a56f9 Viewer_Python_Get_File_Versions.py >}}

{{< /tab >}} {{< /tabs >}}
