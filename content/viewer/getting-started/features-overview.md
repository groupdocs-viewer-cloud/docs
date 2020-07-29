---
id: "features-overview"
url: "viewer/features-overview"
title: "Features Overview"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---



# GroupDocs.Viewer Cloud V2 #

GroupDocs.Viewer Cloud is a REST API that provides methods to render the most popular file formats into Image (JPG, PNG or BMP), HTML or PDF formats.

The difference between the V2 version from V1 is a more simplified API with fewer methods and options. Also, it has a more optimized and refined internal architecture. In this version, the API includes methods for working with cloud storage, which is an important part: main viewer API methods take input documents from storage and put results there.

## API Sections Overview ##

|Api section|Description
|---|---
|**Viewer API**|Main API methods for getting information about documents and rendering them
|File API|Methods for upload, download, copy, move, delete files : input documents and rendering results, in the cloud storage
|Folder API|Methods for create, copy, move, delete folders in the cloud storage
|Storage API|Methods for getting storage information and file information


## File formats ##

See the full list of [Supported File Formats]({{< ref "viewer/getting-started/supported-document-formats.md" >}})).
|---|---

## Security and Authentication ##

The GroupDocs.Viewer Cloud API is secured and requires authentication. Two keys AppSID and AppKey are required for Authentication which can be created at the [Dashboard](http://dashboard.groupdocs.cloud/). Check [Authenticating API Requests]({{< ref "total/getting-started/overview-rest-api/authenticating-api-requests.md" >}})) article for a complete example. 
|---|---|---|---

## SDKs ##

Check out our GitHub [repository](https://github.com/groupdocs-viewer-cloud) for a complete list of GroupDocs.Viewer SDKs along with working examples, to get you started in no time. 
|---|---

At the moment following SDKs are provided: 

* .NET ([Sources](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet), [NuGet Package](https://www.nuget.org/packages/GroupDocs.Viewer-Cloud/))
|---|---|---|---
* PHP ([Sources](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php), [Composer Package](https://packagist.org/packages/groupdocscloud/viewer-sdk-php))
* Java ([Sources](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-java), [Jar](https://repository.groupdocs.cloud/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs/groupdocs-viewer-cloud))
* Ruby ([Sources](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-ruby), [RubyGem](https://rubygems.org/gems/groupdocs_viewer_cloud))
* NodeJS ([Sources](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-node), [Npm Package](https://www.npmjs.com/package/groupdocs-viewer-cloud))
* Python ([Sources](https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-python), [PyPI Package](https://pypi.org/project/groupdocs-viewer-cloud/))

## API Explorer ##

The easiest way to try out our API right away in your browser! With the [GroupDocs Cloud API explorer](https://apireference.groupdocs.cloud/viewer/). This is a collection of Swagger documentation for the GroupDocs Cloud APIs. You can get information about all the resources in the API. It also provides testing and interactivity to our API endpoint documentation.
|---|---
