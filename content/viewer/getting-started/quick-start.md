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
{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Get_All_Supported_Formats.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud e86f05aeed57101c77e399f1c80b99b5 Viewer_Java_Get_All_Supported_Formats.java >}}
{{< /tab >}}
{{< tab "PHP" >}}
{{< gist groupdocscloud 59f66e2a32e4f47157573d93b6c824cd Viewer_PHP_Get_All_File_Formats.php >}}
{{< /tab >}}
{{< tab "Node.js" >}}
{{< gist groupdocscloud f96d4c7dbf8cb43ec3d6717a7309d3b8 Viewer_Node_Get_All_File_Formats.js >}}
{{< /tab >}}
{{< tab "Python" >}}
{{< gist groupdocscloud 62dc8525f388f52d68047c1ce56986a4 Viewer_Python_Get_All_File_Formats.py >}}
{{< /tab >}}
{{< tab "Ruby" >}}
{{< gist groupdocscloud 2c9c4af250204823444eb40f8c412ed0 Viewer_Ruby_Get_All_Supported_Formats.rb >}}
{{< /tab >}}
{{< tab "Android" >}}
{{< gist groupdocscloud 6e9d8e6b54cde933baba15e2a645a57a Viewer_Android_Get_Supported_Formats.java >}}
{{< /tab >}}
{{< /tabs >}}