---
id: "self-host-groupdocs-viewer-cloud-with-docker"
url: "viewer/self-host-groupdocs-viewer-cloud-with-docker"
title: "Self-host GroupDocs.Viewer Cloud with Docker"
productName: "GroupDocs.Viewer Cloud"
description: "Self-host GroupDocs.Viewer Cloud with Docker"
keywords: "groupdocs.viewer cloud, docker"
toc: True
---

[Docker](https://docs.docker.com/get-started/overview/) is an open platform that effectively solves three main tasks development, deployment, and running the applications. With Docker, you can isolate your applications from the infrastructure that simplifies software development and delivery. The main building blocs are images and containers. The image includes everything you need to run the application: code or binaries, runtime dependencies, file system. The container is an isolated process with additional features that you can interact with. The use of containers to deploy applications is called *containerization*.

[Docker Hub](https://hub.docker.com/) is a repository or library of the container images where you can share and find images.

## Self-hosting

The GroupDocs.Viewer Cloud Container Image available at [https://hub.docker.com/r/groupdocs/viewer-cloud](https://hub.docker.com/r/groupdocs/viewer-cloud) and enables users to self-host GroupDocs.Viewer Cloud.

To run the GroupDocs.Viewer Cloud in Docker the Docker itself should be installed on your machine.

### Install Docker

Check [Get Started](https://www.docker.com/get-started) section for Docker installation for your platform. After you installed and started Docker on your local machine we can run the container.

{{< alert style="info" >}}
When running Docker on Windows make sure to switch to Linux containers by clicking on Docker icon in the tray and selecting "Switch to Linux containers..." (see [https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) for more details.)
{{< /alert >}}

### Run Container

Before running the container you can create two optional folders with files to process and custom fonts that we'll be mounted and available to GroupDocs.Viewer Cloud service when we start the container.

To run GroupDocs.Viewer Cloud in Docker type one of the following commands:

{{< alert style="info" >}}
In case you don't have license keys you can omit LICENSE_PUBLIC_KEY and LICENSE_PRIVATE_KEY parameters. Without license GroupDocs.Viewer will work in evaluation mode.
{{< /alert >}}

{{< tabs "example1">}}
{{< tab "Powershell" >}}
```powershell
docker run `
    -p 8080:80 `
    -v "${pwd}/fonts:/fonts" `
    -v "${pwd}/data:/data" `
    -e "LICENSE_PUBLIC_KEY#public_key" `
    -e "LICENSE_PRIVATE_KEY#private_key" `
    --name viewer_cloud `
    groupdocs/viewer-cloud
```
{{< /tab >}}
{{< tab "Bash" >}}
```bash
docker run \
    -p 8080:80 \
    -v $(pwd)/fonts:/fonts \
    -v $(pwd)/data:/data \
    -e LICENSE_PUBLIC_KEY#public_key \
    -e LICENSE_PRIVATE_KEY#private_key \
    --name viewer_cloud \
    groupdocs/viewer-cloud
```
{{< /tab >}}
{{< /tabs >}}

The Docker would download GroupDocs.Viewer Cloud image from Docker Hub and start a container. While downloading the image the output similar to shown on screenshot would be printed to the console:

{{< alert style="info" >}}
I'm running Docker on Windows and will be using PowerShell to run the commands but the experience would be the same in case you're on Linux.
{{< /alert >}}

![Docker image downloading process](/viewer/images/downloading_image.png)

After the container is started you'll see the following messages that indicate that GroupDocs.Viewer Cloud service up and running.

![Docker container started](/viewer/images/container_started.png)

Now you can work with GroupDocs.Viewer Cloud which is hosted on your machine.

### Health-check

When the container and GroupDocs.Viewer Cloud started you can check service status by calling GET [http://localhost:8080/](http://localhost:8080/). The successful response status (200) will indicate that the service is up and running.

{{< tabs "example2">}}
{{< tab "PowerShell" >}}
```powershell
Invoke-WebRequest -Uri http://localhost:8080/
```
{{< /tab >}}
{{< tab "Bash" >}}
```bash
curl -i http://localhost:8080/
```
{{< /tab >}}
{{< /tabs >}}

At the following screenshot, I'm calling [http://localhost:8080/](http://localhost:8080/) in a separate Powershell window and response indicates that service is alive:

![Health check](/viewer/images/health_check.png)

### Using UI

After starting, you can use Swagger UI at [http://localhost:8080/swagger/](http://localhost:8080/swagger/) and explore the API. With Swagger UI you can call API methods in your browser.

![Swagger UI](/viewer/images/swagger_ui.png)

### Using SDK

We generate our SDKs in different languages so you may check if yours is available at [GitHub](https://github.com/groupdocs-viewer-cloud). SDKs require authentication, so predefined CLIENT_ID/CLIENT_SECRET parameters must be set.

{{< alert style="info" >}}
If you don't find your language in the SKD list, feel free to request for it on our [Support Forums](https://forum.groupdocs.cloud/c/viewer), or use raw REST API requests as you can find it [here](https://products.groupdocs.cloud/viewer/curl).
{{< /alert >}}

The authentication is required in case you're going to use SDK. To enable authentication set `CLIENT_ID` & `CLIENT_SECRET` parameters as it shown below.

{{< tabs "example3">}}
{{< tab "PowerShell" >}}
```powershell
docker run `
    -p 8080:80 `
    -v "${pwd}/fonts:/fonts" `
    -v "${pwd}/data:/data" `
    -e "LICENSE_PUBLIC_KEY#public_key" `
    -e "LICENSE_PRIVATE_KEY#private_key" `
    -e "client_id=client_id" `
    -e "client_secret=client_secret" `
    --name viewer_cloud `
    groupdocs/viewer-cloud
```
{{< /tab >}}
{{< tab "Bash" >}}
```bash
docker run \
    -p 8080:80 \
    -v $(pwd)/fonts:/fonts \
    -v $(pwd)/data:/data \
    -e LICENSE_PUBLIC_KEY#public_key \
    -e LICENSE_PRIVATE_KEY#private_key \
    -e client_id=client_id \
    -e client_secret=client_secret \
    --name viewer_cloud \
    groupdocs/viewer-cloud
```
{{< /tab >}}
{{< /tabs >}}

Then, when using SDK, setup the api base url, as shown in examples below:

{{< tabs "example4">}}
{{< tab "C#" >}}
```csharp
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet-samples
string ClientId = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
string ClientSecret = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud

var configuration = new Configuration(ClientId, ClientSecret)
{
    ApiBaseUrl = "http://localhost:8080"
};
var apiInstance = new InfoApi(configuration);
var response = apiInstance.GetSupportedFileFormats();
```
{{< /tab >}}
{{< tab "Java" >}}
```java
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java-samples
String ClientId = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
String ClientSecret = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud

Configuration configuration = new Configuration(ClientId, ClientSecret);
configuration.setApiBaseUrl("http://localhost:8080");

InfoApi apiInstance = new InfoApi(configuration);
FormatsResult response = apiInstance.getSupportedFileFormats();
```
{{< /tab >}}
{{< tab "PHP" >}}
```php
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php-samples
use GroupDocs\Viewer\Model;
use GroupDocs\Viewer\Model\Requests;

$ClientId = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
$ClientSecret = ""; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud

$configuration = new GroupDocs\Viewer\Configuration();
$configuration->setAppSid($ClientId);
$configuration->setAppKey($ClientSecret);
$configuration->setApiBaseUrl("http://localhost:8080");

$infoApi= new GroupDocs\Viewer\InfoApi($configuration);

$response = $infoApi->getSupportedFileFormats();
```
{{< /tab >}}
{{< tab "JavaScript" >}}
```js
// For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node-samples
global.viewer_cloud = require("groupdocs-viewer-cloud");

global.clientId = "XXXX-XXXX-XXXX-XXXX"; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
global.clientSecret = "XXXXXXXXXXXXXXXX"; // Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
const config = new Configuration(clientId, clientSecret);
config.apiBaseUrl = "http://localhost:8080";
global.infoApi = viewer_cloud.InfoApi.fromConfig(config);

let response = await infoApi.getSupportedFileFormats();
```
{{< /tab >}}
{{< tab "Python" >}}
```python
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python-samples
import groupdocs_viewer_cloud

client_id = "XXXX-XXXX-XXXX-XXXX" # Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
client_secret = "XXXXXXXXXXXXXXXX" # Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud

configuration = Configuration(client_id, client_secret)
configuration.api_base_url = "http://localhost:8080"

infoApi = groupdocs_viewer_cloud.InfoApi.from_config(configuration)

result = infoApi.get_supported_file_formats()
```
{{< /tab >}}
{{< tab "Ruby" >}}
```ruby
# For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby-samples
require 'groupdocs_viewer_cloud'

$client_id = "XXXX-XXXX-XXXX-XXXX" # Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud
$client_secret = "XXXXXXXXXXXXXXXX" # Get ClientId and ClientSecret from https://dashboard.groupdocs.cloud

config = Configuration.new(client_id, client_secret)
config.api_base_url = "http://localhost:8080"

infoApi = GroupDocsViewerCloud::InfoApi.from_config(config)

result = infoApi.get_supported_file_formats()
```
{{< /tab >}}
{{< /tabs >}}

### Enable Google Cloud Storage

By default, a local storage used inside container for file operations. It's possible to connect a Google Cloud storage by setting GOOGLE_APPLICATION_CREDENTIALS and GOOGLE_STORAGE_BUCKET environment variables.

{{< tabs "example5">}}
{{< tab "PowerShell" >}}
```powershell
docker run `
    -p 8080:80 `
    -v "${pwd}/fonts:/fonts" `
    -v "${pwd}/data:/data" `
    -e "GOOGLE_APPLICATION_CREDENTIALS=/data/key.json" `
    -e "GOOGLE_STORAGE_BUCKET=bucket_id" `
    --name viewer_cloud `
    groupdocs/viewer-cloud
```
{{< /tab >}}
{{< tab "Bash" >}}
```bash
docker run \
    -p 8080:80 \
    -v $(pwd)/fonts:/fonts \
    -v $(pwd)/data:/data \
    -e GOOGLE_APPLICATION_CREDENTIALS=/data/key.json \
    -e GOOGLE_STORAGE_BUCKET=bucket_id \
    --name viewer_cloud \
    groupdocs/viewer-cloud
```
{{< /tab >}}
{{< /tabs >}}


### Stop Container

To stop the running Docker container, just use Ctrl+C in the same terminal where the container is running. Alternatively, you can stop the container by name.

```bash
docker stop viewer_cloud
```

## Licensing

GroupDocs.Viewer Cloud can be started in trial and licensed modes. When GroupDocs.Viewer Cloud is working in trial mode the following limitations are applied:

* You can convert only two first pages of the document
* Evaluation watermarks added to the output

You can find more information about evaluation at [Evaluate GroupDocs.Viewer]({{< ref "viewer/getting-started/evaluate-groupdocs-viewer.md" >}}).

## DockerHub

You can find more information at [DockerHub](https://hub.docker.com/repository/docker/groupdocs/viewer-cloud).
