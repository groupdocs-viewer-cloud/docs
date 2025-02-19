---
id: "working-with-files"
url: "viewer/working-with-files"
title: "Working With Files"
productName: "GroupDocs.Viewer Cloud"
weight: 4
description: "GroupDocs.Viewer Cloud Working With Files"
keywords: "GroupDocs.Viewer Cloud, Working With Files"
toc: True
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

{{< tabs "download-file-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/file/one-page.docx?storageName#MyStorage" -H  "accept: multipart/form-data" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}
{{< /tabs >}}

### Download File with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "download-file-with-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using GroupDocs.Viewer.Cloud.Sdk.Model.Requests;
using System;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Download_File
	class Download_File
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
			var apiInstance = new FileApi(configuration);

			try
			{
				var request = new DownloadFileRequest("viewerdocs/one-page.docx", Common.MyStorage);

				var response = apiInstance.DownloadFile(request);
				Console.WriteLine("Expected response type is Stream: " + response.Length.ToString());
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling FileApi: " + e.Message);
			}
		}
	}
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java
package examples.Working_With_Files;

import java.io.File;
import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Java_Download_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {

			DownloadFileRequest request = new DownloadFileRequest("viewers\\one-page.docx", Utils.MYStorage, null);
			File response = apiInstance.downloadFile(request);
			System.err.println("Expected response type is File: " + response.length());
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "PHP" >}}

```php
<?php

include(dirname(__DIR__) . '\CommonUtils.php');

	try {
		$apiInstance = CommonUtils::GetFileApiInstance();

		$request = new GroupDocs\Viewer\Model\Requests\DownloadFileRequest("viewerdocs\\one-page.docx", CommonUtils::$MyStorage, null);
		$response = $apiInstance->downloadFile($request);
		
		echo "Expected response type is File: ", strlen($response);
	} catch (Exception $e) {
		echo "Something went wrong: ", $e->getMessage(), "\n";
	}
?>
```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Download_File {
	static Run() {
		var request = new groupdocs_viewer_cloud_1.DownloadFileRequest("viewerdocs/one-page.docx", myStorage);
		fileApi.downloadFile(request)
			.then(function (response) {
				console.log("Expected response type is Stream: " + response.length);
			})
			.catch(function (error) {
				console.log("Error: " + error.message);
			});
	}
}
module.exports = Viewer_Node_Download_File;

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Download_File:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_FileApi_Instance()
        
        try:
            request = groupdocs_viewer_cloud.DownloadFileRequest("viewerdocs\\one-page.docx", Common_Utilities.myStorage)
            response = api.download_file(request)
            
            print("Expected response type is Stream: " + str(len(response)))
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception while calling API: {0}".format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Files
  def self.Viewer_Ruby_Download_File()

    # Getting instance of the API
    $api = Common_Utilities.Get_FileApi_Instance()

    $request = GroupDocsViewerCloud::DownloadFileRequest.new("viewerdocs/one-page.docx", $myStorage)
    $response = $api.download_file($request)
    
    puts("Expected response type is Stream: " + ($response).to_s)
  end
end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Working_With_Files;

import java.io.File;
import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Android_Download_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {

			DownloadFileRequest request = new DownloadFileRequest("viewers\\one-page.docx", Utils.MYStorage, null);
			File response = apiInstance.downloadFile(request);
			System.err.println("Expected response type is File: " + response.length());
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "Go">}}
```go
package basicUsage

import (
    "fmt"
    "os"

    "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
    viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

func DownloadFile() {
    filePath := "SampleFiles/sample.docx"
    downloadOpts := viewer.FileApiDownloadFileOpts{
        StorageName: optional.NewString("YourStorageName"),
    }

    file, _, err := config.Client.FileApi.DownloadFile(config.Ctx, filePath, &downloadOpts)
    if err != nil {
        fmt.Printf("DownloadFile error: %v\n", err)
        return
    }
    defer file.Close()

    outFile, err := os.Create("downloaded_sample.docx")
    if err != nil {
        fmt.Printf("Error creating file: %v\n", err)
        return
    }
    defer outFile.Close()

    _, err = io.Copy(outFile, file)
    if err != nil {
        fmt.Printf("Error saving file: %v\n", err)
        return
    }

    fmt.Println("File downloaded successfully")
}
```
{{< /tab >}}
{{< /tabs >}}

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


{{< tabs "upload-file-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X POST "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewerdocs%2Fone-page2.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
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
{{< /tab >}}
{{< /tabs >}}

### Upload File with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "upload-file-with-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using GroupDocs.Viewer.Cloud.Sdk.Model.Requests;
using System;
using System.IO;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Upload File
	class Upload_File
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
			var apiInstance = new FileApi(configuration);

			try
			{
				// Open file in IOStream from local/disc.
				var fileStream = File.Open("..\\..\\..\\Data\\viewerdocs\\one-page.docx", FileMode.Open);

				var request = new UploadFileRequest("viewerdocs/one-page1.docx", fileStream, Common.MyStorage);

				var response = apiInstance.UploadFile(request);
				Console.WriteLine("Expected response type is FilesUploadResult: " + response.Uploaded.Count.ToString());
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling FileApi: " + e.Message);
			}
		}
	}
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java
package examples.Working_With_Files;

import java.io.File;
import java.nio.file.Paths;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Java_Upload_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {
			File fileStream = new File(
					Paths.get("src\\main\\resources").toAbsolutePath().toString() + "\\viewers\\one-page.docx");
			UploadFileRequest request = new UploadFileRequest("viewers\\one-page1.docx", fileStream,
					Utils.MYStorage);
			FilesUploadResult response = apiInstance.uploadFile(request);
			System.out.println("Expected response type is FilesUploadResult: " + response.getUploaded().size());
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "PHP" >}}

```php
<?php

include(dirname(__DIR__) . '\CommonUtils.php');

	try {
		$apiInstance = CommonUtils::GetFileApiInstance();

		$fileStream = readfile("..\\resources\\viewerdocs\\one-page.docx");
		$request = new GroupDocs\Conversion\Model\Requests\UploadFileRequest("viewerdocs\\one-page1.docx", $fileStream, CommonUtils::$MyStorage, null);
		$response = $apiInstance->downloadFile($request);
		
		echo "Expected response type is FilesUploadResult: ", $response;
	} catch (Exception $e) {
		echo "Something went wrong: ", $e->getMessage(), "\n";
	}
?>
```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Upload_File {
	static Run() {

		// Open file in IOStream from local/disc.
		var resourcesFolder = './Resources/viewerdocs/one-page.docx';
		fs.readFile(resourcesFolder, (err, fileStream) => {

			var request = new groupdocs_viewer_cloud_1.UploadFileRequest("viewerdocs/one-page1.docx", fileStream, myStorage);
			fileApi.uploadFile(request)
				.then(function (response) {
					console.log("Expected response type is FilesUploadResult: " + response.uploaded.length);
				})
				.catch(function (error) {
					console.log("Error: " + error.message);
				});
		});
	}
}
module.exports = Viewer_Node_Upload_File;

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Upload_File:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_FileApi_Instance()
        
        try:
            request = groupdocs_viewer_cloud.UploadFileRequest("viewerdocs\\one-page.docx", "D:\\ewspace\\GroupDocs.Viewer.Cloud.Python.Examples\\src\\Resources\\viewerdocs\\one-page.docx", Common_Utilities.myStorage)
            response = api.upload_file(request)
            
            print("Expected response type is FilesUploadResult: " + str(response))
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception while calling API: {0}".format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Files
  def self.Viewer_Ruby_Upload_File()

    # Getting instance of the API
    $api = Common_Utilities.Get_FileApi_Instance()
   
    $fileStream = File.new("..\\Resources\\viewerdocs\\one-page.docx", "r")
    
    $request = GroupDocsViewerCloud::UploadFileRequest.new("viewerdocs/one-page1.docx", $fileStream, $myStorage)
    $response = $api.upload_file($request)
    
    $fileStream.close()

    puts("Expected response type is FilesUploadResult: " + ($response).to_s)
  end
end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Working_With_Files;

import java.io.File;
import java.nio.file.Paths;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Android_Upload_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {
			File fileStream = new File(
					Paths.get("src\\main\\resources").toAbsolutePath().toString() + "\\viewers\\one-page.docx");
			UploadFileRequest request = new UploadFileRequest("viewers\\one-page1.docx", fileStream,
					Utils.MYStorage);
			FilesUploadResult response = apiInstance.uploadFile(request);
			System.out.println("Expected response type is FilesUploadResult: " + response.getUploaded().size());
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "Go">}}
```go
package basicUsage

import (
    "fmt"
    "os"

    "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
    viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

func UploadFile() {
    filePath := "SampleFiles/sample.docx"
    file, err := os.Open(filePath)
    if err != nil {
        fmt.Printf("Error opening file: %v\n", err)
        return
    }
    defer file.Close()

    uploadOpts := viewer.FileApiUploadFileOpts{
        StorageName: optional.NewString("YourStorageName"),
    }

    uploadResult, _, err := config.Client.FileApi.UploadFile(config.Ctx, "uploaded_sample.docx", file, &uploadOpts)
    if err != nil {
        fmt.Printf("UploadFile error: %v\n", err)
        return
    }

    fmt.Printf("File uploaded successfully: %v\n", uploadResult.Uploaded)
}

```
{{< /tab >}}

{{< /tabs >}}

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

{{< tabs "delete-file-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X DELETE "https://api.groupdocs.cloud/v2.0/viewer/storage/file/viewerdocs1%2Fone-page1.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}
{{< /tabs >}}

### Delete File with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "delete-file-with-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using GroupDocs.Viewer.Cloud.Sdk.Model.Requests;
using System;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Delete File
	class Delete_File
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
			var apiInstance = new FileApi(configuration);

			try
			{
				var request = new DeleteFileRequest("viewerdocs1/one-page1.docx", Common.MyStorage);

				apiInstance.DeleteFile(request);
				Console.WriteLine("Expected response type is Void: 'viewerdocs1/one-page1.docx' deleted.");
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling FileApi: " + e.Message);
			}
		}
	}
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java
package examples.Working_With_Files;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Java_Delete_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {

			DeleteFileRequest request = new DeleteFileRequest("viewers1\\one-page1.docx", Utils.MYStorage, null);
			apiInstance.deleteFile(request);
			System.out.println("Expected response type is Void: 'viewers1/one-page1.docx' deleted.");
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "PHP" >}}

```php
<?php

include(dirname(__DIR__) . '\CommonUtils.php');

	try {
		$apiInstance = CommonUtils::GetFileApiInstance();

		$request = new GroupDocs\Viewer\Model\Requests\DeleteFileRequest("viewerdocs1\\one-page-copied.docx", CommonUtils::$MyStorage);
		$apiInstance->deleteFile($request);
		
		echo "Expected response type is Void: 'viewerdocs1/one-page-copied.docx' file deleted.";
	} catch (Exception $e) {
		echo "Something went wrong: ", $e->getMessage(), "\n";
	}
?>
```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Delete_File {
	static Run() {
		var request = new groupdocs_viewer_cloud_1.DeleteFileRequest("viewerdocs1/one-page1.docx", myStorage);
		fileApi.deleteFile(request)
			.then(function (response) {
				console.log("Expected response type is Void: 'viewerdocs1/one-page1.docx' deleted.");
			})
			.catch(function (error) {
				console.log("Error: " + error.message);
			});
	}
}
module.exports = Viewer_Node_Delete_File;

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Delete_File:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_FileApi_Instance()
        
        try:
            request = groupdocs_viewer_cloud.DeleteFileRequest("viewerdocs1\\one-page.docx", Common_Utilities.myStorage)
            api.delete_file(request)
            
            print("Expected response type is Void: 'viewerdocs1/one-page.docx' deleted.")
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception while calling API: {0}".format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Files
  def self.Viewer_Ruby_Delete_File()

    # Getting instance of the API
    $api = Common_Utilities.Get_FileApi_Instance()

    $request = GroupDocsViewerCloud::DeleteFileRequest.new("viewerdocs1/one-page1.docx", $myStorage)
    $response = $api.delete_file($request)

    puts("Expected response type is Void: 'viewerdocs1/one-page1.docx' deleted.")
  end
end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Working_With_Files;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Android_Delete_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {

			DeleteFileRequest request = new DeleteFileRequest("viewers1\\one-page1.docx", Utils.MYStorage, null);
			apiInstance.deleteFile(request);
			System.out.println("Expected response type is Void: 'viewers1/one-page1.docx' deleted.");
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "Go">}}
```go
package basicUsage

import (
    "fmt"

    "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
    viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

func DeleteFile() {
    filePath := "SampleFiles/sample.docx"
    deleteOpts := viewer.FileApiDeleteFileOpts{
        StorageName: optional.NewString("YourStorageName"),
    }

    _, err := config.Client.FileApi.DeleteFile(config.Ctx, filePath, &deleteOpts)
    if err != nil {
        fmt.Printf("DeleteFile error: %v\n", err)
        return
    }

    fmt.Println("File deleted successfully")
}
```
{{< /tab >}}

{{< /tabs >}}

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

{{< tabs "copy-file-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X PUT "https://api.groupdocs.cloud/v2.0/viewer/storage/file/copy/viewerdocs%2Fone-page1.docx?destPath#viewerdocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}
{{< /tabs >}}

### File Copy with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "copy-file-with-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using GroupDocs.Viewer.Cloud.Sdk.Model.Requests;
using System;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Copy File
	class Copy_File
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
			var apiInstance = new FileApi(configuration);

			try
			{
				var request = new CopyFileRequest("viewerdocs/one-page1.docx", "viewerdocs/one-page-copied.docx", Common.MyStorage, Common.MyStorage);

				apiInstance.CopyFile(request);
				Console.WriteLine("Expected response type is Void: 'viewerdocs/one-page1.docx' file copied as 'viewerdocs/one-page-copied.docx'.");
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling FileApi: " + e.Message);
			}
		}
	}
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java
package examples.Working_With_Files;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Java_Copy_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {

			CopyFileRequest request = new CopyFileRequest("viewers\\one-page.docx",
					"viewers\\one-page-copied.docx", Utils.MYStorage, Utils.MYStorage, null);
			apiInstance.copyFile(request);
			System.out.println(
					"Expected response type is Void: 'viewers/one-page1.docx' file copied as 'viewers/one-page-copied.docx'.");
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "PHP" >}}

```php
<?php

include(dirname(__DIR__) . '\CommonUtils.php');

	try {
		$apiInstance = CommonUtils::GetFileApiInstance();

		$request = new GroupDocs\Viewer\Model\Requests\CopyFileRequest("viewerdocs\\one-page.docx", "viewerdocs\\one-page-copied.docx", CommonUtils::$MyStorage, CommonUtils::$MyStorage);
		$apiInstance->copyFile($request);
		
		echo "Expected response type is Void: 'viewerdocs/one-page.docx' file copied as 'viewerdocs/one-page-copied.docx'.";
	} catch (Exception $e) {
		echo "Something went wrong: ", $e->getMessage(), "\n";
	}
?>
```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Copy_File {
	static Run() {
		var request = new groupdocs_viewer_cloud_1.CopyFileRequest("viewerdocs/one-page1.docx", "viewerdocs/one-page-copied.docx", myStorage, myStorage);
		fileApi.copyFile(request)
			.then(function (response) {
				console.log("Expected response type is Void: 'viewerdocs/one-page1.docx' file copied as 'viewerdocs/one-page-copied.docx'.");
			})
			.catch(function (error) {
				console.log("Error: " + error.message);
			});
	}
}
module.exports = Viewer_Node_Copy_File;

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Copy_File:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_FileApi_Instance()
        
        try:
            request = groupdocs_viewer_cloud.CopyFileRequest("viewerdocs\\one-page.docx", "viewerdocs\\one-page-copied.docx", Common_Utilities.myStorage, Common_Utilities.myStorage)
            api.copy_file(request)
            
            print("Expected response type is Void: 'viewerdocs/one-page.docx' file copied as 'viewerdocs/one-page-copied.docx'.")
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception while calling API: {0}".format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Files
  def self.Viewer_Ruby_Copy_File()

    # Getting instance of the API
    $api = Common_Utilities.Get_FileApi_Instance()

    $request = GroupDocsViewerCloud::CopyFileRequest.new("viewerdocs/one-page1.docx", "viewerdocs/one-page-copied.docx", $myStorage, $myStorage)
    $response = $api.copy_file($request)

    puts("Expected response type is Void: 'viewerdocs/one-page1.docx' file copied as 'viewerdocs/one-page-copied.docx'.")
  end
end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Working_With_Files;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Android_Copy_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {

			CopyFileRequest request = new CopyFileRequest("viewers\\one-page.docx",
					"viewers\\one-page-copied.docx", Utils.MYStorage, Utils.MYStorage, null);
			apiInstance.copyFile(request);
			System.out.println(
					"Expected response type is Void: 'viewers/one-page1.docx' file copied as 'viewers/one-page-copied.docx'.");
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "Go">}}
```go
package basicUsage

import (
    "fmt"

    "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
    viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

func DeleteFile() {
    filePath := "SampleFiles/sample.docx"
    deleteOpts := viewer.FileApiDeleteFileOpts{
        StorageName: optional.NewString("YourStorageName"),
    }

    _, err := config.Client.FileApi.DeleteFile(config.Ctx, filePath, &deleteOpts)
    if err != nil {
        fmt.Printf("DeleteFile error: %v\n", err)
        return
    }

    fmt.Println("File deleted successfully")
}
```
{{< /tab >}}

{{< /tabs >}}

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

{{< tabs "move-file-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X PUT "https://api.groupdocs.cloud/v2.0/viewer/storage/file/move/viewerdocs%2Fone-page1.docx?destPath#viewerdocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}
{{< /tabs >}}

### File Move with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [File API](https://apireference.groupdocs.cloud/viewer/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "move-file-with-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using GroupDocs.Viewer.Cloud.Sdk.Model.Requests;
using System;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Move File
	class Move_File
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
			var apiInstance = new FileApi(configuration);

			try
			{
				var request = new MoveFileRequest("viewerdocs/one-page1.docx", "viewerdocs1/one-page1.docx", Common.MyStorage, Common.MyStorage);

				apiInstance.MoveFile(request);
				Console.WriteLine("Expected response type is Void: 'viewerdocs/one-page1.docx' file moved to 'viewerdocs1/one-page1.docx'.");
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling FileApi: " + e.Message);
			}
		}
	}
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java
package examples.Working_With_Files;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Java_Move_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {

			MoveFileRequest request = new MoveFileRequest("viewers\\one-page1.docx", "viewers1\\one-page1.docx",
					Utils.MYStorage, Utils.MYStorage, null);
			apiInstance.moveFile(request);
			System.out.println(
					"Expected response type is Void: 'viewers/one-page1.docx' file moved to 'viewers1/one-page1.docx'.");
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "PHP" >}}

```php
<?php

include(dirname(__DIR__) . '\CommonUtils.php');

	try {
		$apiInstance = CommonUtils::GetFileApiInstance();

		$request = new GroupDocs\Viewer\Model\Requests\MoveFileRequest("viewerdocs\\one-page.docx", "viewerdocs1\\one-page-copied.docx", CommonUtils::$MyStorage, CommonUtils::$MyStorage);
		$apiInstance->moveFile($request);
		
		echo "Expected response type is Void: 'viewerdocs/one-page.docx' file moved as 'viewerdocs1/one-page-copied.docx'.";
	} catch (Exception $e) {
		echo "Something went wrong: ", $e->getMessage(), "\n";
	}
?>
```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Move_File {
	static Run() {
		var request = new groupdocs_viewer_cloud_1.MoveFileRequest("viewerdocs/one-page1.docx", "viewerdocs1/one-page1.docx", myStorage, myStorage);
		fileApi.moveFile(request)
			.then(function (response) {
				console.log("Expected response type is Void: 'viewerdocs/one-page1.docx' file moved to 'viewerdocs1/one-page1.docx'.");
			})
			.catch(function (error) {
				console.log("Error: " + error.message);
			});
	}
}
module.exports = Viewer_Node_Move_File;

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Move_File:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_FileApi_Instance()
        
        try:
            request = groupdocs_viewer_cloud.MoveFileRequest("viewerdocs\\one-page.docx", "viewerdocs1\\one-page.docx", Common_Utilities.myStorage, Common_Utilities.myStorage)
            api.move_file(request)
            
            print("Expected response type is Void: 'viewerdocs/one-page.docx' file moved to 'viewerdocs1/one-page.docx'.")
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception while calling API: {0}".format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Files
  def self.Viewer_Ruby_Move_File()

    # Getting instance of the API
    $api = Common_Utilities.Get_FileApi_Instance()

    $request = GroupDocsViewerCloud::MoveFileRequest.new("viewerdocs/one-page1.docx", "viewerdocs1/one-page1.docx", $myStorage, $myStorage)
    $response = $api.move_file($request)

    puts("Expected response type is Void: 'viewerdocs/one-page1.docx' file moved to 'viewerdocs1/one-page1.docx'.")
  end
end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Working_With_Files;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Android_Move_File {

	public static void main(String[] args) {

		FileApi apiInstance = new FileApi(Utils.AppSID, Utils.AppKey);
		try {

			MoveFileRequest request = new MoveFileRequest("viewers\\one-page1.docx", "viewers1\\one-page1.docx",
					Utils.MYStorage, Utils.MYStorage, null);
			apiInstance.moveFile(request);
			System.out.println(
					"Expected response type is Void: 'viewers/one-page1.docx' file moved to 'viewers1/one-page1.docx'.");
		} catch (ApiException e) {
			System.err.println("Exception while calling FileApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< tab "Go">}}
```go
package basicUsage

import (
    "fmt"

    "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
    viewer "github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go/models"
)

func MoveFile() {
    srcPath := "SampleFiles/sample.docx"
    destPath := "SampleFiles/moved_sample.docx"
    moveOpts := viewer.FileApiMoveFileOpts{
        SrcStorageName:  optional.NewString("YourStorageName"),
        DestStorageName: optional.NewString("YourStorageName"),
    }

    _, err := config.Client.FileApi.MoveFile(config.Ctx, srcPath, destPath, &moveOpts)
    if err != nil {
        fmt.Printf("MoveFile error: %v\n", err)
        return
    }

    fmt.Println("File moved successfully")
}
```
{{< /tab >}}
{{< /tabs >}}
