---
id: "metered-consumption"
url: "viewer/metered-consumption"
title: "Getting metered license consumption"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---
### Introduction ###

{{< alert style="info" >}}
This example related to Docker version of GroupDocs.Viewer-Cloud only
{{< /alert >}}

The metered license can be used in Docker version of GroupDocs.Viewer-Cloud.
Here is an example how to retrieve metered license consumption.

You can find more information about Docker version at [How to self-host GroupDocs.Viewer Cloud with Docker]({{< ref "viewer/getting-started/how-to-self-host-groupdocs-viewer-cloud-with-docker.md" >}})

## Resource URI ##

```HTTP GET ~/viewer/consumption```

## cURL Example ##

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html

* cURL example to get metered license consumption
curl -v "http://<base url>/v2.0/viewer/consumption" \
-X GET \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "credit": 487848,
  "quantity": 6061570985.37938
}
{{< /tab >}} {{< /tabs >}}

## Response ##

The response structure contains metered license consumption information:

| Name | Type | Comment
|---|---|---
|Credit|decimal|Amount of used credits.
|Quantity|decimal|Amount of MBs processed.

## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-viewer-cloud) in many development languages in order to make it easier to integrate with us.

### SDK Examples ###

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

```csharp
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet-samples
string MyClientSecret = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
string MyClientId = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
  
var configuration = new Configuration(MyClientId, MyClientSecret);
  
// Create necessary API instances
var apiInstance = new LicenseApi(configuration);

var response = apiInstance.GetConsumptionCredit();

Console.WriteLine($"Credits: {response.Credit}");
Console.WriteLine($"Quantity: {response.Quantity}");
```

{{< /tab >}} {{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
String MyClientSecret = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
String MyClientId = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
  
Configuration configuration = new Configuration(MyClientId, MyClientSecret);
  
// Create API instance
LicenseApi apiInstance = new LicenseApi(configuration);

ConsumptionResult response = apiInstance.getConsumptionCredit();
System.out.println("Credit: " + response.getCredit());
System.out.println("Quantity: " + response.getQuantity());
```

{{< /tab >}} {{< tab tabNum="3" >}}

```php
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php-samples
use GroupDocs\Viewer\Model;
use GroupDocs\Viewer\Model\Requests;

$ClientId = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
$ClientSecret = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
  
$configuration = new GroupDocs\Viewer\Configuration();
$configuration->setAppSid($ClientId);
$configuration->setAppKey($ClientSecret);

$apiInstance = new GroupDocs\Viewer\LicenseApi($configuration);

// Prepare request
$filePath = dirname(realpath(__DIR__)) . '\Resources\WordProcessing\four-pages.docx';
$request = new Requests\ConvertDocumentDirectRequest("pdf", $filePath);

// Get consumption
$result = $apiInstance->getConsumptionCredit();

// Done
echo "Credit: " . $result->getCredit();
```

{{< /tab >}} {{< tab tabNum="4" >}}

```node
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer_cloud = require("groupdocs-viewer-cloud");

global.clientId = "XXXX-XXXX-XXXX-XXXX"; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
global.clientSecret = "XXXXXXXXXXXXXXXX"; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
  
global.licenseApi = viewer_cloud.LicenseApi.fromKeys(clientId, clientSecret);

let response = await licenseApi.getConsumptionCredit();
console.log("GetLicenseConsumption: Credit = " + response.credit);
```

{{< /tab >}} {{< tab tabNum="5" >}}

```python
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud

client_id = "XXXX-XXXX-XXXX-XXXX" # Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
client_secret = "XXXXXXXXXXXXXXXX" # Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
  
# Create necessary API instances
apiInstance = groupdocs_viewer_cloud.LicenseApi.from_keys(Common.client_id, Common.client_secret)

# Get consumption
result = apiInstance.get_consumption_credit()

print("Credit: " + result.credit)
```

{{< /tab >}} {{< tab tabNum="6" >}}

```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'

$client_id = "XXXX-XXXX-XXXX-XXXX" # Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
$client_secret = "XXXXXXXXXXXXXXXX" # Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
  
# Create necessary API instances
apiInstance = GroupDocsViewerCloud::LicenseApi.from_keys($client_id, $client_secret)

# Get consumption
result = apiInstance.get_consumption_credit()

puts("Credit: " + result.credit)
```

{{< /tab >}} {{< /tabs >}}
