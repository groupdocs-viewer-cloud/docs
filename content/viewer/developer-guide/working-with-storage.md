---
id: "working-with-storage"
url: "viewer/working-with-storage"
title: "Working With Storage"
productName: "GroupDocs.Viewer Cloud"
weight: 6
description: "GroupDocs.Viewer Cloud Working With Storage"
keywords: "GroupDocs.Viewer Cloud, Working With Storage"
toc: True
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


{{< tabs "check-storage-exist-wit-curl">}}
{{< tab "Request" >}}
```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/MyStorage/exist" -H  "accept: application/json" -H  "authorization: Bearer  [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "exists": true
}
```
{{< /tab >}}
{{< /tabs >}}

### Check Storage Exist with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Storage existence](https://apireference.groupdocs.cloud/viewer/#/Storage/StorageExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "check-storage-exist-with-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using GroupDocs.Viewer.Cloud.Sdk.Model.Requests;
using System;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Is Storage Exist
	class Storage_Exist
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
			var apiInstance = new StorageApi(configuration);

			try
			{
				var request = new StorageExistsRequest(Common.MyStorage);

				var response = apiInstance.StorageExists(request);
				Console.WriteLine("Expected response type is StorageExist: " + response.Exists.Value.ToString());
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling StorageApi: " + e.Message);
			}
		}
	}
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java
package examples.Working_With_Storage;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Java_Storage_Exist {

	public static void main(String[] args) {

		StorageApi apiInstance = new StorageApi(Utils.AppSID, Utils.AppKey);
		try {
			StorageExistsRequest request = new StorageExistsRequest(Utils.MYStorage);
			StorageExist response = apiInstance.storageExists(request);
			System.out.println("Expected response type is StorageExist: " + response.getExists());
		} catch (ApiException e) {
			System.err.println("Exception while calling StorageApi:");
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
    $apiInstance = CommonUtils::GetStorageApiInstance();

	$request = new GroupDocs\Viewer\Model\Requests\StorageExistsRequest(CommonUtils::$MyStorage);
		$response = $apiInstance->storageExists($request);
		
		echo "Expected response type is StorageExist: ", $response;
} catch (Exception $e) {
    echo "Something went wrong: ", $e->getMessage(), "\n";
}
?>
```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Storage_Exist {
	static Run() {
		// retrieve supported file-formats
		var request = new groupdocs_viewer_cloud_1.StorageExistsRequest(myStorage);
		storageApi.storageExists(request)
			.then(function (response) {
				console.log("Expected response type is StorageExist: " + response.exists);
			})
			.catch(function (error) {
				console.log("Error: " + error.message);
			});
	}
}
module.exports = Viewer_Node_Storage_Exist;

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Storage_Exist:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_StorageApi_Instance()
        
        try:
            request = groupdocs_viewer_cloud.StorageExistsRequest(Common_Utilities.myStorage)
            response = api.storage_exists(request)
            
            print("Expected response type is StorageExist: " + str(response))
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception while calling API: {0}".format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Storage
  def self.Viewer_Ruby_Storage_Exist()

    # Getting instance of the API
    $api = Common_Utilities.Get_StorageApi_Instance()
    
    $request = GroupDocsViewerCloud::StorageExistsRequest.new($myStorage)
    $response = $api.storage_exists($request)

    puts("Expected response type is StorageExist: " + ($response).to_s)
  end
end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Working_With_Storage;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Android_Storage_Exist {

	public static void main(String[] args) {

		StorageApi apiInstance = new StorageApi(Utils.AppSID, Utils.AppKey);
		try {
			StorageExistsRequest request = new StorageExistsRequest(Utils.MYStorage);
			StorageExist response = apiInstance.storageExists(request);
			System.out.println("Expected response type is StorageExist: " + response.getExists());
		} catch (ApiException e) {
			System.err.println("Exception while calling StorageApi:");
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

func CheckStorageExists() {
    storageName := "YourStorageName"

    storageExist, _, err := config.Client.StorageApi.StorageExists(config.Ctx, storageName)
    if err != nil {
        fmt.Printf("StorageExists error: %v\n", err)
        return
    }

    if storageExist.Exists {
        fmt.Println("Storage exists")
    } else {
        fmt.Println("Storage does not exist")
    }
}
```
{{< /tab >}}
{{< /tabs >}}

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

{{< tabs "check-storage-object-exist-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/exist/viewerdocs?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "exists": true,
  "isFolder": true
}
```
{{< /tab >}}
{{< /tabs >}}

### Check Storage Object Exist with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Storage Object existence](https://apireference.groupdocs.cloud/viewer/#/Storage/ObjectExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "check-storage-object-exits-with-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using GroupDocs.Viewer.Cloud.Sdk.Model.Requests;
using System;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Is Object Exists
	class Object_Exists
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
			var apiInstance = new StorageApi(configuration);

			try
			{
				var request = new ObjectExistsRequest("viewerdocs/one-page.docx", Common.MyStorage);

				var response = apiInstance.ObjectExists(request);
				Console.WriteLine("Expected response type is ObjectExist: " + response.Exists.Value.ToString());
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling StorageApi: " + e.Message);
			}
		}
	}
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java
package examples.Working_With_Storage;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Java_Object_Exists {

	public static void main(String[] args) {

		StorageApi apiInstance = new StorageApi(Utils.AppSID, Utils.AppKey);
		try {
			ObjectExistsRequest request = new ObjectExistsRequest("viewers\\one-page.docx", Utils.MYStorage, null);
			ObjectExist response = apiInstance.objectExists(request);
			System.out.println("Expected response type is ObjectExist: " + response.getExists());
		} catch (ApiException e) {
			System.err.println("Exception while calling StorageApi:");
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
		$apiInstance = CommonUtils::GetStorageApiInstance();

		$request = new GroupDocs\Viewer\Model\Requests\ObjectExistsRequest("viewerdocs\one-page.docx", CommonUtils::$MyStorage);
		$response = $apiInstance->objectExists($request);
		
		echo "Expected response type is ObjectExist: ", $response;
	} catch (Exception $e) {
		echo "Something went wrong: ", $e->getMessage(), "\n";
	}
?>
```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Object_Exists {
	static Run() {
		// retrieve supported file-formats
		var request = new groupdocs_viewer_cloud_1.ObjectExistsRequest("viewerdocs/one-page.docx", myStorage);
		storageApi.objectExists(request)
			.then(function (response) {
				console.log("Expected response type is ObjectExist: " + response.exists);
			})
			.catch(function (error) {
				console.log("Error: " + error.message);
			});
	}
}
module.exports = Viewer_Node_Object_Exists;

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Object_Exists:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_StorageApi_Instance()
        
        try:
            request = groupdocs_viewer_cloud.ObjectExistsRequest("viewerdocs\\one-page.docx", Common_Utilities.myStorage)
            response = api.object_exists(request)
            
            print("Expected response type is ObjectExist: " + str(response))
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception while calling API: {0}".format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Storage
  def self.Viewer_Ruby_Object_Exists()

    # Getting instance of the API
    $api = Common_Utilities.Get_StorageApi_Instance()
    
    $request = GroupDocsViewerCloud::ObjectExistsRequest.new("viewerdocs/one-page.docx", $myStorage)
    $response = $api.object_exists($request)

    puts("Expected response type is ObjectExist: " + ($response).to_s)
  end
end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Working_With_Storage;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Android_Object_Exists {

	public static void main(String[] args) {

		StorageApi apiInstance = new StorageApi(Utils.AppSID, Utils.AppKey);
		try {
			ObjectExistsRequest request = new ObjectExistsRequest("viewers\\one-page.docx", Utils.MYStorage, null);
			ObjectExist response = apiInstance.objectExists(request);
			System.out.println("Expected response type is ObjectExist: " + response.getExists());
		} catch (ApiException e) {
			System.err.println("Exception while calling StorageApi:");
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

func ObjectExists() {
    objectPath := "SampleFiles/sample.docx"
    existsOpts := viewer.StorageApiObjectExistsOpts{
        StorageName: optional.NewString("YourStorageName"),
    }

    objectExist, _, err := config.Client.StorageApi.ObjectExists(config.Ctx, objectPath, &existsOpts)
    if err != nil {
        fmt.Printf("ObjectExists error: %v\n", err)
        return
    }

    if objectExist.Exists {
        fmt.Println("Object exists")
    } else {
        fmt.Println("Object does not exist")
    }
}
```
{{< /tab >}}
{{< /tabs >}}

## Storage Space Usage API

This API intended for getting total and used space of the[ GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### Storage Space Usage with API Explorer

[GroupDocs.Viewer Cloud API Reference](https://apireference.groupdocs.cloud/viewer/#/) lets you try out [storage space usage API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetDiscUsage) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Storage Space Usage Request parameters

|Parameter|Description
|---|---
|storageName|Name of the storage. If not set, then default storage used

### Storage Space Usage with cURL

{{< tabs "storage-space-usage-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/disc?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}
```json
{
  "usedSize": 31032368,
  "totalSize": 3221225472
}
```
{{< /tab >}}
{{< /tabs >}}

### Storage Space Usage with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [storage space usage API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetDiscUsage) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "storage-space-usage-with-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using GroupDocs.Viewer.Cloud.Sdk.Model.Requests;
using System;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Get Get Disc Usage
	class Get_Disc_Usage
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
			var apiInstance = new StorageApi(configuration);

			try
			{
				var request = new GetDiscUsageRequest(Common.MyStorage);

				var response = apiInstance.GetDiscUsage(request);
				Console.WriteLine("Expected response type is DiscUsage: " + response.UsedSize.ToString());
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling StorageApi: " + e.Message);
			}
		}
	}
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java
package examples.Working_With_Storage;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Java_Get_Disc_Usage {

	public static void main(String[] args) {

		StorageApi apiInstance = new StorageApi(Utils.AppSID, Utils.AppKey);
		try {
			GetDiscUsageRequest request = new GetDiscUsageRequest(Utils.MYStorage);
			DiscUsage response = apiInstance.getDiscUsage(request);
			System.out.println("Expected response type is DiscUsage: " + response.getUsedSize());
		} catch (ApiException e) {
			System.err.println("Exception while calling StorageApi:");
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
		$apiInstance = CommonUtils::GetStorageApiInstance();

		$request = new GroupDocs\Viewer\Model\Requests\GetDiscUsageRequest(CommonUtils::$MyStorage);
		$response = $apiInstance->getDiscUsage($request);
			
		echo "Expected response type is DiscUsage: ", $response;
	} catch (Exception $e) {
		echo "Something went wrong: ", $e->getMessage(), "\n";
	}
?>
```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Get_Disc_Usage {
	static Run() {
		// retrieve supported file-formats
		var request = new groupdocs_viewer_cloud_1.GetDiscUsageRequest(myStorage);
		storageApi.getDiscUsage(request)
			.then(function (response) {
				console.log("Expected response type is DiscUsage: " + response.usedSize);
			})
			.catch(function (error) {
				console.log("Error: " + error.message);
			});
	}
}
module.exports = Viewer_Node_Get_Disc_Usage;

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Get_Disc_Usage:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_StorageApi_Instance()
        
        try:
            request = groupdocs_viewer_cloud.GetDiscUsageRequest(Common_Utilities.myStorage)
            response = api.get_disc_usage(request)
            
            print("Expected response type is DiscUsage: " + str(response))
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception while calling API: {0}".format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Storage
  def self.Viewer_Ruby_Get_Disc_Usage()

    # Getting instance of the API
    $api = Common_Utilities.Get_StorageApi_Instance()
    
    $request = GroupDocsViewerCloud::GetDiscUsageRequest.new($myStorage)
    $response = $api.get_disc_usage($request)

    puts("Expected response type is DiscUsage: " + ($response).to_s)
  end
end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Working_With_Storage;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Android_Get_Disc_Usage {

	public static void main(String[] args) {

		StorageApi apiInstance = new StorageApi(Utils.AppSID, Utils.AppKey);
		try {
			GetDiscUsageRequest request = new GetDiscUsageRequest(Utils.MYStorage);
			DiscUsage response = apiInstance.getDiscUsage(request);
			System.out.println("Expected response type is DiscUsage: " + response.getUsedSize());
		} catch (ApiException e) {
			System.err.println("Exception while calling StorageApi:");
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

func GetDiskUsage() {
    usageOpts := viewer.StorageApiGetDiscUsageOpts{
        StorageName: optional.NewString("YourStorageName"),
    }

    diskUsage, _, err := config.Client.StorageApi.GetDiscUsage(config.Ctx, &usageOpts)
    if err != nil {
        fmt.Printf("GetDiskUsage error: %v\n", err)
        return
    }

    fmt.Printf("Total Size: %v\n", diskUsage.TotalSize)
    fmt.Printf("Used Size: %v\n", diskUsage.UsedSize)
}
```
{{< /tab >}}
{{< /tabs >}}

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

{{< tabs "storage-file-version-with-curl">}}
{{< tab "Request" >}}
```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/storage/version/one-page.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
```
{{< /tab >}}
{{< tab "Resonse" >}}

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
{{< /tab >}}
{{< /tabs >}}

### Storage File Versions with SDK

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-viewer-cloud), it hides the [Storage File Versions API](https://apireference.groupdocs.cloud/viewer/#/Storage/GetFileVersions) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "storage-file-versions-with-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using GroupDocs.Viewer.Cloud.Sdk.Model.Requests;
using System;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Get File Versions
	class Get_File_Versions
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);
			var apiInstance = new StorageApi(configuration);

			try
			{
				var request = new GetFileVersionsRequest("one-page.docx", Common.MyStorage);

				var response = apiInstance.GetFileVersions(request);
				Console.WriteLine("Expected response type is FileVersions: " + response.Value.Count.ToString());
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling StorageApi: " + e.Message);
			}
		}
	}
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java
package examples.Working_With_Storage;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Java_Get_File_Versions {

	public static void main(String[] args) {

		StorageApi apiInstance = new StorageApi(Utils.AppSID, Utils.AppKey);
		try {
			GetFileVersionsRequest request = new GetFileVersionsRequest("viewers\\one-page.docx", Utils.MYStorage);
			FileVersions response = apiInstance.getFileVersions(request);
			System.out.println("Expected response type is FileVersions: " + response.getValue().size());
		} catch (ApiException e) {
			System.err.println("Exception while calling StorageApi:");
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
		$apiInstance = CommonUtils::GetStorageApiInstance();

		$request = new GroupDocs\Viewer\Model\Requests\GetFileVersionsRequest("viewerdocs\one-page.docx", CommonUtils::$MyStorage);
		$response = $apiInstance->getFileVersions($request);
		
		echo "Expected response type is FileVersions: ", $response;
	} catch (Exception $e) {
		echo "Something went wrong: ", $e->getMessage(), "\n";
	}
?>
```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Get_File_Versions {
	static Run() {
		// retrieve supported file-formats
		var request = new groupdocs_viewer_cloud_1.GetFileVersionsRequest("viewerdocs/one-page.docx", myStorage);
		storageApi.getFileVersions(request)
			.then(function (response) {
				console.log("Expected response type is FileVersions: " + response.value.length);
			})
			.catch(function (error) {
				console.log("Error: " + error.message);
			});
	}
}
module.exports = Viewer_Node_Get_File_Versions;

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Get_File_Versions:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_StorageApi_Instance()
        
        try:
            request = groupdocs_viewer_cloud.GetFileVersionsRequest("viewerdocs\\one-page.docx", Common_Utilities.myStorage)
            response = api.get_file_versions(request)
            
            print("Expected response type is FileVersions: " + str(response))
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception while calling API: {0}".format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class Working_With_Storage
  def self.Viewer_Ruby_Get_File_Versions()

    # Getting instance of the API
    $api = Common_Utilities.Get_StorageApi_Instance()
    
    $request = GroupDocsViewerCloud::GetFileVersionsRequest.new("viewerdocs/one-page.docx", $myStorage)
    $response = $api.get_file_versions($request)

    puts("Expected response type is FileVersions: " + ($response).to_s)
  end
end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Working_With_Storage;

import com.groupdocs.cloud.viewer.api.*;
import com.groupdocs.cloud.viewer.client.ApiException;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.model.requests.*;
import examples.Utils;

public class Viewer_Android_Get_File_Versions {

	public static void main(String[] args) {

		StorageApi apiInstance = new StorageApi(Utils.AppSID, Utils.AppKey);
		try {
			GetFileVersionsRequest request = new GetFileVersionsRequest("viewers\\one-page.docx", Utils.MYStorage);
			FileVersions response = apiInstance.getFileVersions(request);
			System.out.println("Expected response type is FileVersions: " + response.getValue().size());
		} catch (ApiException e) {
			System.err.println("Exception while calling StorageApi:");
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

func GetFileVersions() {
    filePath := "SampleFiles/sample.docx"
    versionsOpts := viewer.StorageApiGetFileVersionsOpts{
        StorageName: optional.NewString("YourStorageName"),
    }

    fileVersions, _, err := config.Client.StorageApi.GetFileVersions(config.Ctx, filePath, &versionsOpts)
    if err != nil {
        fmt.Printf("GetFileVersions error: %v\n", err)
        return
    }

    for _, version := range fileVersions.Value {
        fmt.Printf("Version ID: %v, Size: %v\n", version.VersionId, version.Size)
    }
}
```
{{< /tab >}}
{{< /tabs >}}
