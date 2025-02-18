---
id: "quick-start"
url: "viewer/quick-start"
title: "Quick Start"
productName: "GroupDocs.Viewer Cloud"
weight: 3
description: "GroupDocs.Viewer Cloud Quick Start"
keywords: "GroupDocs.Viewer Cloud, Quick Start"
toc: True
---

## Create an account

Sign up at <https://id.containerize.com/signup> to create a free account.

## Create an API client app

Before you can make any requests to GroupDocs Cloud API you need to get Client Id and Client Secret. That will be used to invoke the GroupDocs Cloud API.

You can get it from existing Application or create new Application from [Applications View of GroupDocs Cloud Dashboard]({{< ref "total/ui-topics/creating-and-managing-application.md" >}}).

## Install the SDK of your choice

GroupDocs.Viewer Cloud SDK is written in different languages, all you need to get started is adding our [SDK]({{< ref "viewer/getting-started/available-sdks.md" >}}) to your project.

## Make an API request

Use the **Client Id** and **Client Secret** from the API app client you created in step one and replace in the corresponding code. Below is an example demonstrating using Formats API to get all supported file formats in GroupDocs.Viewer Cloud.

{{< alert style="info" >}}The GitHub repository for [GroupDocs.Viewer Cloud](https://github.com/groupdocs-viewer-cloud) has a complete set of examples, demonstrating our API capabilities.{{< /alert >}}

{{< tabs "example1">}}
{{< tab "C#" >}}

```csharp
//TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud (free registration is required).
var configuration = new Configuration
{
           AppSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
           AppKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
};
 
var apiInstance = new ViewerApi(configuration);
 
try
{
          var request = new GetSupportedFileFormatsRequest();
 
          // Get supported file formats
          var response = apiInstance.GetSupportedFileFormats(request);
 
          foreach (var format in response.Formats)
          {
          Debug.Print(format.ToString());
          }
}
catch (Exception e)
{
           Debug.Print("Exception when calling ViewerApi.DeleteFontsCache: " + e.Message);
}
```

{{< /tab >}}
{{< tab "Java" >}}

```java

// TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud (free registration is required).
String appSid = "xxxx";
String appKey = "xxx-xx";

ViewerApi apiInstance = new ViewerApi(appSid, appKey);
try {
	FormatCollection response = apiInstance.getSupportedFileFormats();

	if (response.getFormats().size() > 0) {
		for (Format format : response.getFormats()) {
			System.out.println("Format: " + format.toString());
		}
	}
	System.out.println("Executed Successfully");
} catch (ApiException e) {
	System.err.println("Exception when calling ViewerApi");
	e.printStackTrace();
}
```

{{< /tab >}}
{{< tab "PHP" >}}

```php
//TODO: Get your AppSID and AppKey at https://dashboard.groupdocs.cloud (free registration is required).
$configuration = new GroupDocs\Viewer\Configuration();
$configuration->setAppSid($sid);
$configuration->setAppKey($key);

$viewerApi = new GroupDocs\Viewer\ViewerApi($configuration); 

try {
    $request = new GroupDocs\Viewer\Model\Requests\GetSupportedFileFormatsRequest();
    $response = $viewerApi->getSupportedFileFormats($request);

    foreach ($response->getFormats() as $key => $format) {
        echo $format->getFileFormat() . " - " .  $format->getExtension(), "\n";
    }
} catch (Exception $e) {
    echo  "Something went wrong: ",  $e->getMessage(), "\n";    
}

```

{{< /tab >}}
{{< tab "Node.js" >}}

```js
"use strict";
exports.__esModule = true;
// load the module
var groupdocs_viewer_cloud_1 = require("groupdocs-viewer-cloud");
// get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
var appSid = "XXXX-XXXX-XXXXX";
var appKey = "XXXXXXXXXX";
// construct ViewerApi
var viewerApi = groupdocs_viewer_cloud_1.ViewerApi.fromKeys(appSid, appKey);
// retrieve supported file-formats
viewerApi.getSupportedFileFormats()
    .then(function (result) {
    console.log("Supported file-formats:");
    result.formats.forEach(function (format) {
        console.log(format.fileFormat + " (" + format.extension + ")");
    });
})["catch"](function (error) {
    console.log("Error: " + error.message);
});

```

{{< /tab >}}
{{< tab "Python" >}}

```python
# Import module
import groupdocs_viewer_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXX-XXXXXXX-XXXX"
app_key = "XXXXXXXXXXXXX"

# Create instance of the GroupDocs Viewer APIapi = groupdocs_viewer_cloud.ViewerApi.from_keys(app_sid, app_key)

try:

    response = api.get_supported_file_formats()
    print('Response:')

    for format in response.formats:
        print('{0} ({1})'.format(format.file_format, format.extension)) 

except groupdocs_viewer_cloud.ApiException as e:
    print('Exception while calling Viewer API: {0}'.format(e.message))
```

{{< /tab >}}
{{< tab "Ruby" >}}

```ruby
	# Load the gem
	require 'groupdocs_viewer_cloud'
	require '..\lib\groupdocs_viewer_cloud\api\viewer_api'

	# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
	app_sid = "XXX-XXXXXXX-XXXX"
	app_key = "XXXXXXXXXXXXX"

	# Create instance of the API class
	api = GroupDocsViewerCloud.from_keys(app_sid, app_key)

	# Retrieve supported file-formats
	response = api.get_supported_file_formats

	# Print out supported file-formats
	puts("Supported file-formats:")
	response.formats.each do |format|
	  puts("#{format.file_format} (#{format.extension})") 
	end
```

{{< /tab >}}
{{< tab "Android" >}}

```java
package examples.Supported_File_Formats;

import com.groupdocs.cloud.viewer.client.*;
import com.groupdocs.cloud.viewer.model.*;
import com.groupdocs.cloud.viewer.api.InfoApi;
import examples.Utils;

public class Viewer_Android_Get_Supported_Formats {

	public static void main(String[] args) {

		InfoApi apiInstance = new InfoApi(Utils.AppSID, Utils.AppKey);
		try {
			FormatsResult response = apiInstance.getSupportedFileFormats();

			for (Format format : response.getFormats()) {
				System.out.println(format.getFileFormat());
			}
		} catch (ApiException e) {
			System.err.println("Exception while calling InfoApi:");
			e.printStackTrace();
		}
	}
}
```

{{< /tab >}}
{{< /tabs >}}