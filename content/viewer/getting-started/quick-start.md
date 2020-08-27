---
id: "quick-start"
url: "viewer/quick-start"
title: "Quick Start"
productName: "GroupDocs.Viewer Cloud"
weight: 3
description: "GroupDocs.Viewer Cloud Quick Start"
keywords: "GroupDocs.Viewer Cloud, Quick Start"
---

## Create an account

Sign up at <https://id.containerize.com/signup> to create a free account.

## Create an API client app

Before you can make any requests to GroupDocs for Cloud API you need to get APP SID and APP key (secret key). That will be used to invoke the GroupDocs Cloud API.

You can get it from default Application or create new Application from [My Apps tab of GroupDocs for Cloud Dashboard]({{< ref "total/getting-started/ui-topics/create-new-app-and-get-app-key-and-sid.md" >}}).

## Install the SDK of your choice

GroupDocs.Viewer Cloud SDK is written in different languages, all you need to get started is adding our [SDK]({{< ref "viewer/getting-started/available-sdks.md" >}}) to your project.

## Make an API request

Use the **App SID** and **App key (secret key)** from the API app client you created in step one and replace in the corresponding code. Below is an example demonstrating using Formats API to get all supported file formats in GroupDocs.Viewer Cloud.

{{< alert style="info" >}}The GitHub repository for [GroupDocs.Viewer Cloud](https://github.com/groupdocs-viewer-cloud) has a complete set of examples, demonstrating our API capabilities.{{< /alert >}}

{{< tabs tabTotal="6" tabID="10" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Node.js" tabName5="Python" tabName6="Ruby" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_All_Supported_Formats.cs >}}

{{< /tab >}} {{< tab tabNum="3" >}}

{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_All_File_Formats.php >}}

{{< /tab >}} {{< tab tabNum="2" >}}

{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_All_Supported_Formats.java >}}

{{< /tab >}} {{< tab tabNum="6" >}}

{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_All_Supported_Formats.rb >}}

{{< /tab >}} {{< tab tabNum="4" >}}

{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_All_File_Formats.js >}}

{{< /tab >}} {{< tab tabNum="5" >}}

{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_All_File_Formats.py >}}

{{< /tab >}} {{< /tabs >}}
