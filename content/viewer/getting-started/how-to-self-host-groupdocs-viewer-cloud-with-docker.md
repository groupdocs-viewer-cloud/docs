---
id: "how-to-self-host-groupdocs-viewer-cloud-with-docker"
url: "viewer/how-to-self-host-groupdocs-viewer-cloud-with-docker"
title: "How to self-host GroupDocs.Viewer Cloud with Docker"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---



## Overview ##

[Docker](https://docs.docker.com/get-started/overview/) is an open platform that effectively solves three main tasks development, deployment, and running the applications. With Docker, you can isolate your applications from the infrastructure that simplifies software development and delivery. The main building blocs are images and containers. The image includes everything you need to run the application: code or binaries, runtimes dependencies, file system. The container is an isolated process with additional features that you can interact with. The use of containers to deploy applications is called *containerization*.

[Docker Hub](https://hub.docker.com/) is a repository or library of the container images where you can share and find images.

## Self-hosting ##

The GroupDocs.Viewer Cloud Container Image available at [https://hub.docker.com/r/groupdocs/viewer-cloud](https://hub.docker.com/r/groupdocs/viewer-cloud) and enables users to self-host GroupDocs.Viewer Cloud.

To run the GroupDocs.Viewer Cloud in Docker the Docker itself should be installed on your machine. 

### Install Docker ###

Check [Get Started](https://www.docker.com/get-started) section for Docker installation for your platform. After you installed and started Docker on your local machine we can run the container.

*NOTE: When running Docker on Windows make sure to switch to Linux containers by clicking on Docker icon in the tray and selecting "Switch to Linux containers..." (see [https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) for more details.)*

### Run Container ###

Before running the container you can create two optional folders with files to process and custom fonts that we'll be mounted and available to GroupDocs.Viewer Cloud service when we start the container.

To run GroupDocs.Viewer Cloud in Docker type one of the following commands:

*NOTE: In case you don't have license keys you can omit LICENSE_PUBLIC_KEY and LICENSE_PRIVATE_KEY parameters. Without license GroupDocs.Viewer will work in evaluation mode. *

**Windows (PowerShell)**

```html 

docker run `
    -p 8080:80 `
    -v "${pwd}/fonts:/fonts" `
    -v "${pwd}/data:/data" `
    -e "LICENSE_PUBLIC_KEY#public_key" `
    -e "LICENSE_PRIVATE_KEY#private_key" `
    --name viewer_cloud `
    groupdocs/viewer-cloud

 ```

**Linux (bash)**

```html 

docker run \
    -p 8080:80 \
    -v $(pwd)/fonts:/fonts \
    -v $(pwd)/data:/data \
    -e LICENSE_PUBLIC_KEY#public_key \
    -e LICENSE_PRIVATE_KEY#private_key \
    --name viewer_cloud \
    groupdocs/viewer-cloud

 ```

The Docker would download GroupDocs.Viewer Cloud image from Docker Hub and start a container. While downloading the image the output similar to shown on screenshot would be printed to the console:

*NOTE: I'm running Docker on Windows and will be using PowerShell to run the commands but the experience would be the same in case you're on Linux.*

![](viewer/images/downloading_image.png)

After the container is started you'll see the following messages that indicate that GroupDocs.Viewer Cloud service up and running.

![](viewer/images/container_started.png)

Now you can work with GroupDocs.Viewer Cloud which is hosted on your machine. 

### Health-check ###

When the container and GroupDocs.Viewer Cloud started you can check service status by calling GET [http:~~/~~/localhost:8080/](http://localhost:8080/). The successful response status (200) will indicate that the service is up and running.

**Windows (PowerShell)**

```html 

Invoke-WebRequest -Uri http://localhost:8080/

 ```

**Linux (bash)**

```html 

curl -i http://localhost:8080/

 ```

At the following screenshot, I'm calling [http:~~/~~/localhost:8080/](http://localhost:8080/) in a separate Powershell window and response indicates that service is alive:

![](viewer/images/health_check.png)

### Using UI ###

After starting, you can use Swagger UI at [http:~~/~~/localhost:8080/swagger/](http://localhost:8080/swagger/) and explore the API. With Swagger UI you can call API methods in your browser.

![](viewer/images/swagger_ui.png)

### Using SDK ###

We generate our SDKs in different languages so you may check if yours is available at [GitHub](https://github.com/groupdocs-viewer-cloud). SDKs require authentication, so predefined CLIENT_ID/CLIENT_SECRET parameters must be set.

*NOTE: If you don't find your language in the SKD list, feel free to request for it on our [Support Forums](https://forum.groupdocs.cloud/c/viewer), or use raw REST API requests as you can find it [here](https://products.groupdocs.cloud/viewer/curl).*

**Windows (PowerShell)**

```html 

docker run `
    -p 8080:80 `
    -v "${pwd}/fonts:/fonts" `
    -v "${pwd}/data:/data" `
    -e "LICENSE_PUBLIC_KEY#public_key" `
    -e "LICENSE_PRIVATE_KEY#private_key" `
    -e "CLIENT_ID#client_id" `
    -e "CLIENT_SECRET#client_secret" `
    --name viewer_cloud `
    groupdocs/viewer-cloud

 ```

**Linux (bash)**

```html 

docker run \
    -p 8080:80 \
    -v $(pwd)/fonts:/fonts \
    -v $(pwd)/data:/data \
    -e LICENSE_PUBLIC_KEY#public_key \
    -e LICENSE_PRIVATE_KEY#private_key \
    -e CLIENT_ID#client_id \
    -e CLIENT_SECRET#client_secret \
    --name viewer_cloud \
    groupdocs/viewer-cloud

 ```

### Stop Container ###

To stop the running Docker container, just use Ctrl+C in the same terminal where the container is running. Alternatively, you can stop the container by name.

```html 

docker stop viewer_cloud

 ```

## Licensing ##

GroupDocs.Viewer Cloud can be started in trial and licensed modes. When GroupDocs.Viewer Cloud is working in trial mode the following limitations are applied:

* You can convert only two first pages of the document
* Evaluation watermarks added to the output

You can find more information about evaluation at [Evaluate GroupDocs.Viewer]({{< ref "viewer/getting-started/evaluate-groupdocs-viewer.md" >}})).