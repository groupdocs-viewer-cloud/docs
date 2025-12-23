---
id: "get-supported-file-formats"
url: "viewer/get-supported-file-formats"
title: "Get Supported File Formats"
productName: "GroupDocs.Viewer Cloud"
weight: 4
description: ""
keywords: ""
toc: True
---

GroupDocs.Viewer Cloud REST APIs support to render over 50 file formats to HTML5 or Image formats for the whole document, page by page or custom range of pages. To get list of supported formats, You can use the below API.

The following GroupDocs.Viewer Cloud REST API resource has been used in the [Supported File Formats](https://apireference.groupdocs.cloud/viewer/#/Viewer/GetSupportedFileFormats) example.

## cURL example

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}
```bash
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/formats" \
  -H "accept: application/json" \
  -H "authorization: Bearer $JWT_TOKEN"
```
{{< /tab >}}

{{< tab "Windows PowerShell" >}}
```powershell
curl.exe -X GET "https://api.groupdocs.cloud/v2.0/viewer/formats" `
  -H "accept: application/json" `
  -H "authorization: Bearer $env:JWT_TOKEN"
```
{{< /tab >}}

{{< tab "Windows CMD" >}}
```cmd
curl -X GET "https://api.groupdocs.cloud/v2.0/viewer/formats" ^
  -H "accept: application/json" ^
  -H "authorization: Bearer %JWT_TOKEN%"
```
{{< /tab >}} {{< tab "Response" >}}
```json
{
  "formats": [
    {
      "extension": ".pdf",
      "fileFormat": "Portable Document Format"
    },
    {
      "extension": ".pcl",
      "fileFormat": "Printer Command Language Document"
    },
    {
      "extension": ".doc",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".docx",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".docm",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".dot",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".dotx",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".dotm",
      "fileFormat": "Microsoft Word"
    },
    {
      "extension": ".mobi",
      "fileFormat": "Mobipocket"
    },
    {
      "extension": ".xls",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xlsx",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xlsm",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xltx",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xltm",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".xlsb",
      "fileFormat": "Microsoft Excel"
    },
    {
      "extension": ".ppt",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".pptx",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".pps",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".ppsx",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".potm",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".ppsm",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".potx",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".pptm",
      "fileFormat": "Microsoft PowerPoint"
    },
    {
      "extension": ".vsd",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vdx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vss",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vsx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vst",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vtx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vsdx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vdw",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vssx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vstx",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vstm",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vsdm",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".vssm",
      "fileFormat": "Microsoft Visio"
    },
    {
      "extension": ".mpp",
      "fileFormat": "Microsoft Project"
    },
    {
      "extension": ".mpt",
      "fileFormat": "Microsoft Project"
    },
    {
      "extension": ".msg",
      "fileFormat": "Microsoft Outlook Mail Message"
    },
    {
      "extension": ".eml",
      "fileFormat": "Microsoft Outlook Mail Message"
    },
    {
      "extension": ".ost",
      "fileFormat": "Microsoft Outlook Data Files"
    },
    {
      "extension": ".pst",
      "fileFormat": "Microsoft Outlook Data Files"
    },
    {
      "extension": ".one",
      "fileFormat": "Microsoft OneNote"
    },
    {
      "extension": ".emlx",
      "fileFormat": "Apple Mail"
    },
    {
      "extension": ".odt",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".ott",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".ods",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".odp",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".otp",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".ots",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".odg",
      "fileFormat": "OpenDocument Formats"
    },
    {
      "extension": ".rtf",
      "fileFormat": "Rich Text Format"
    },
    {
      "extension": ".txt",
      "fileFormat": "Plain Text File"
    },
    {
      "extension": ".tex",
      "fileFormat": "LaTeX Scientific document"
    },
    {
      "extension": ".csv",
      "fileFormat": "Comma-Separated Values"
    },
    {
      "extension": ".tsv",
      "fileFormat": "Tab-Separated Values"
    },
    {
      "extension": ".html",
      "fileFormat": "HyperText Markup Language"
    },
    {
      "extension": ".mht",
      "fileFormat": "HyperText Markup Language"
    },
    {
      "extension": ".xml",
      "fileFormat": "Extensible Markup Language"
    },
    {
      "extension": ".xps",
      "fileFormat": "XML Paper Specification"
    },
    {
      "extension": ".bmp",
      "fileFormat": "Image files"
    },
    {
      "extension": ".gif",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpg",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpeg",
      "fileFormat": "Image files"
    },
    {
      "extension": ".png",
      "fileFormat": "Image files"
    },
    {
      "extension": ".tiff",
      "fileFormat": "Image files"
    },
    {
      "extension": ".djvu",
      "fileFormat": "Image files"
    },
    {
      "extension": ".svg",
      "fileFormat": "Image files"
    },
    {
      "extension": ".webp",
      "fileFormat": "Image files"
    },
    {
      "extension": ".dng",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jp2",
      "fileFormat": "Image files"
    },
    {
      "extension": ".j2c",
      "fileFormat": "Image files"
    },
    {
      "extension": ".j2k",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpf",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpx",
      "fileFormat": "Image files"
    },
    {
      "extension": ".jpm",
      "fileFormat": "Image files"
    },
    {
      "extension": ".dcm",
      "fileFormat": "Digital Imaging and Communications in Medicine"
    },
    {
      "extension": ".epub",
      "fileFormat": "Electronic publication"
    },
    {
      "extension": ".ico",
      "fileFormat": "Windows Icon"
    },
    {
      "extension": ".wmf",
      "fileFormat": "Windows Metafile"
    },
    {
      "extension": ".emf",
      "fileFormat": "Windows Metafile"
    },
    {
      "extension": ".psd",
      "fileFormat": "Photoshop"
    },
    {
      "extension": ".cgm",
      "fileFormat": "Computer Graphics Metafile"
    }
  ]
}

```
{{< /tab >}} {{< /tabs >}}

## SDK examples

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

{{< tabs "example1-sdk">}}
{{< tab "C#" >}}

```csharp
using GroupDocs.Viewer.Cloud.Sdk.Api;
using GroupDocs.Viewer.Cloud.Sdk.Client;
using System;

namespace GroupDocs.Viewer.Cloud.Examples.CSharp
{
	// Get All Supported Formats
	class Get_All_Supported_Formats
	{
		public static void Run()
		{
			var configuration = new Configuration(Common.MyAppSid, Common.MyAppKey);

			var apiInstance = new InfoApi(configuration);

			try
			{
				// Get supported file formats
				var response = apiInstance.GetSupportedFileFormats();

				foreach (var entry in response.Formats)
				{
					Console.WriteLine(string.Format("{0}: {1}", entry.FileFormat, string.Join(",", entry.Extension)));
				}
			}
			catch (Exception e)
			{
				Console.WriteLine("Exception while calling InfoApi: " + e.Message);
			}
		}
	}
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
{{< tab "Ruby" >}}

```ruby
# Load the gem
require 'groupdocs_viewer_cloud'
require 'common_utilities/Utils.rb'

class File_Formats
  def self.Get_All_Supported_File_Formats()

    # Getting instance of the API
    api = Common_Utilities.Get_InfoApi_Instance()

    # Retrieve supported file-formats
    response = api.get_supported_file_formats()

    # Print out supported file-formats
    puts("Supported file-formats:")
    response.formats.each do |format|
      puts("#{format.file_format} (#{format.extension})")
    end
  end
end
```

{{< /tab >}} 
{{< tab "Node.js" >}}

```js
"use strict";
class Viewer_Node_Get_All_Supported_Formats {
	static Run() {
		// retrieve supported file-formats
		infoApi.getSupportedFileFormats()
			.then(function (response) {
				console.log("Supported file-formats:");
				response.formats.forEach(function (format) {
					console.log(format.fileFormat + "(" + format.extension + ")");
				});
			})
			.catch(function (error) {
				console.log("Error: " + error.message);
			});
	}
}
module.exports = Viewer_Node_Get_All_Supported_Formats;
```

{{< /tab >}} 
{{< tab "Python" >}}

```python
# Import modules
import groupdocs_viewer_cloud
from Common_Utilities.Utils import Common_Utilities

class Viewer_Python_Get_All_Supported_Formats:
    
    @classmethod
    def Run(self):
        # Create instance of the API
        api = Common_Utilities.Get_InfoApi_Instance()
        
        try:
            # Retrieve supported file-formats
            response = api.get_supported_file_formats()
    
            # Print out supported file-formats
            print("Supported file-formats:")
            for fileformat in response.formats:
                print('{0} ({1})'.format(fileformat.file_format, fileformat.extension))
        except groupdocs_viewer_cloud.ApiException as e:
            print("Exception when calling get_supported_viewer_types: {0}".format(e.message))
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
{{< tab "Go">}}
```go
package basicUsage

import (
	"fmt"

	"github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-go-samples/config"
)

func GetSupportedFormats() {

	response, _, err := config.Client.InfoApi.GetSupportedFileFormats(config.Ctx)

	if err != nil {
		fmt.Printf("GetSupportedViewers error: %v\n", err)
		return
	}

	fmt.Printf("Formats num: %v\n", len(response.Formats))
}

```
{{< /tab >}}
{{< /tabs >}}
