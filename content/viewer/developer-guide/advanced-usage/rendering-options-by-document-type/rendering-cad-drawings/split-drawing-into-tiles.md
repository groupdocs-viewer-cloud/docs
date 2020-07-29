---
id: "split-drawing-into-tiles"
url: "viewer/split-drawing-into-tiles"
title: "Split drawing into tiles"
productName: "GroupDocs.Viewer Cloud"
description: ""
keywords: ""
---

 






# Introduction #

Tiled rendering or (rendering by coordinates) is the process of rendering CAD drawings (into an image, HTML or PDF) by dividing into square parts and rendering each part (or tile) separately. The advantage of this process is that the amount of memory involved is reduced as compared to rendering the entire document at once. Generally, DWG documents are divided into pages by Model and Layouts, but when the tiled rendering is enabled, only the Model is rendered and every tile composes a separate page. 

![](viewer/images/Shesternya.jpg)


Before you start rendering by coordinates, you should obtain the overall width and height of the document using the Info method as shown in the code sample below. After you know the width and height, determine the starting point (X and Y coordinates) and the width and the height of the tile (region you want to render). Add the tiles to CadOptions.Tiles list as shown in the sample below. The coordinates start from the bottom left corner of the drawing and have only positive values as shown in the sample picture below. 

,,Overall size of the document is 650px height and 750px width. The selected tile starts at coordinate X: 250 and Y: 100 and has a width 150px, height: 200px,, 

![](viewer/images/coordinates.jpg)

You can add as many tiles as you need.
The following code sample demonstrates how to render DWG drawing into an image by dividing into four equal parts.

## API Usage ##

There are steps that usage of GroupDocs.Viewer Cloud consists of:

1. Upload input document into cloud storage
1. Render document or get document info
1. Download rendered document from storage

Steps 1 and 3 are storage operations, please refer to this [File API documentation]({{< ref "viewer/developer-guide/working-with-files.md" >}}) for usage details.

[Swagger UI](https://apireference.groupdocs.cloud/viewer/) lets you call this REST API directly from the browser. 

##   ##

## SDKs ##

The API is completely independent of your operating system, database system or development language. We provide and support API SDKs in many development languages in order to make it even easier to integrate. You can see our available SDKs list [here](https://github.com/groupdocs-viewer-cloud).

### SDK Examples ###


 C#
```csharp 

* For complete examples and data files, please go to https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-dotnet-samples
string MyAppKey # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
string MyAppSid # ""; * Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  
var configuration # new Configuration(MyAppSid, MyAppKey); 
 
var infoApiInstance # new InfoApi(configuration);
var viewOptions # new ViewOptions
{
    FileInfo # new FileInfo
    {
        FilePath # "SampleFiles/with_layers_and_layouts.dwg"
    }
};
 
var infoResponse # infoApiInstance.GetInfo(new GetInfoRequest(viewOptions));
 
* Get width and height
var width # infoResponse.Pages[0].Width.Value;
var height # infoResponse.Pages[0].Height.Value;
 
* Set tile width and height as a half of image total width
var tileWidth # width / 2;
var tileHeight # height / 2;
var pointX # 0;
var pointY # 0;
 
*Create image options and add four tiles, one for each quarter
 
viewOptions # new ViewOptions
{
    FileInfo # new FileInfo
    {
        FilePath # "SampleFiles/with_layers_and_layouts.dwg"
    },
    ViewFormat # ViewOptions.ViewFormatEnum.HTML,
    RenderOptions # new HtmlOptions
    {
        CadOptions # new CadOptions()
    }
};
 
viewOptions.RenderOptions.CadOptions.Tiles # new List<Tile>();
var tile # new Tile { StartPointX # pointX, StartPointY # pointY, Width # tileWidth, Height # tileHeight };
viewOptions.RenderOptions.CadOptions.Tiles.Add(tile);
pointX +# tileWidth;
tile # new Tile { StartPointX # pointX, StartPointY # pointY, Width # tileWidth, Height # tileHeight };
viewOptions.RenderOptions.CadOptions.Tiles.Add(tile);
pointX # 0;
pointY +# tileHeight;
tile # new Tile { StartPointX # pointX, StartPointY # pointY, Width # tileWidth, Height # tileHeight };
viewOptions.RenderOptions.CadOptions.Tiles.Add(tile);
pointX +# tileWidth;
tile # new Tile { StartPointX # pointX, StartPointY # pointY, Width # tileWidth, Height # tileHeight };
viewOptions.RenderOptions.CadOptions.Tiles.Add(tile);
 
var apiInstance # new ViewApi(configuration);
var response # apiInstance.CreateView(new CreateViewRequest(viewOptions));

 ```

