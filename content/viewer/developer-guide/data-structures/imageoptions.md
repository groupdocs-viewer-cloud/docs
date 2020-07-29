---
id: "imageoptions"
url: "viewer/imageoptions"
title: "ImageOptions"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

# ImageOptions #

ImageOptions data structure inherits [RenderOptions ]({{< ref "viewer/developer-guide/data-structures/renderoptions.md" >}}))and used as part of [ViewOptions ]({{< ref "viewer/developer-guide/data-structures/viewoptions.md" >}}))data structure. 
|---|---|---|---

##### ImageOptions example #####

```html 

{
	"Width": 0,
	"Height": 0,
	"ExtractText": false,
	"JpegQuality": 0,
}

 ```

##### ImageOptions fields #####

|Name|Description
|---|---
|<RenderOptions fields>|ImageOptions inherits all properties of [RenderOptions]({{< ref "viewer/developer-guide/data-structures/renderoptions.md" >}}))
|Width|Allows to specify output image width. 
Specify image width in case when you want to change output image dimensions.
When Width has value and Height value is 0 then Height value will be calculated 
to save image proportions.
|Height|Allows to specify output image height. 
Specify image height in case when you want to change output image dimensions.
When Height has value and Width value is 0 then Width value will be calculated 
to save image proportions.
|ExtractText|When enabled Viewer will extract text when it's possible (e.g. raster formats don't have text layer) and
return it in the viewing result.
This option might be useful when you want to add selectable text layer over the image.
|JpegQuality|Allows to specify quality when rendering as JPG.
Valid values are between 1 and 100. 
Default value is 90.

