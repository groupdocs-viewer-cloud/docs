---
id: "options-objects"
url: "viewer/options-objects"
title: "Options Objects"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

{{< alert style="info" >}}
Note:  The features listed in this Page are supported only in GroupDocs.Viewer Cloud V1
{{< /alert >}}

# Options Objects #

Page contains description for option objects and object fields.





## [DocumentInfoOptions Object]("DocumentInfoOptions") ##
|---|---

Provides options for retrieving attachment information.

Example DocumentInfoOptions object

```html 
{
  "password": "document password",
  "attachmentPassword": "attachment password",
  "extractText": false,
  "renderComments": false,
  "renderHiddenPages": false,
  "defaultFontName": "font name",
  "transforms": [
    "Rotate",
	"Reorder",
	"AddPrintAction"
  ],
  "watermark": {
    "text": "watermark text",
    "color": "Magenta",
    "position": "Diagonal",
    "size": 50
  },
  "cellsOptions": {
    "renderGridLines": false,
    "paginateSheets": false,
    "encoding": "utf-8",
    "internalHyperlinkPrefix": "prefix",
    "countRowsPerPage": 50,
    "textOverflowMode": "OverlayIfNextIsEmpty",
	"ignoreEmptyRows": false
  },
  "cadOptions": {
    "scaleFactor": 50,
    "width": 600,
    "height": 800,
    "renderLayouts": true,
    "layoutName": "Master",
	"layers": ["Layer1"]
  },
  "emailOptions": {
    "encoding": "utf-8"
  },
  "wordsOptions": {
    "encoding": "utf-8",
    "renderTrackedChanges": false
  },
  "pdfOptions": {
    "enablePreciseRendering": false,
    "enableInitialContentOrdering": false,
    "renderLayersSeparately": false
  },
  "slidesOptions": {
    "renderNotes": false
  },
  "projectOptions": {
    "pageSize": "unknown",
    "pageSize": "unknown"
  }
}
 ```

 Info Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|Password|string|Allows to specify document password in case when document is password-protected.
|AttachmentPassword|string|Allows to specify attachment password in case when attachment is password-protected.
|ExtractText|bool|Enables document text extraction. For rendering document as image only.
|RenderComments|bool|Enables document comments rendering.
|RenderHiddenPages|bool|Enables document hidden pages, sheets or slides rendering.
|DefaultFontName|string|The name of the default font.
 Default font name may be specified in following cases:
- You want to generally specify the default font to fall back on, if particular font
 in the document cannot be found during rendering.
- Your document uses fonts, that contain non-English characters and you want to make sure
 any missing font is replaced with one that has the same character set available.
|Transforms|string[]|Transforms to apply. Available transforms ["Rotate","Reorder","AddPrintAction"].
Rotate - Pages will be rotated on angle if angle was set before.
Reorder - For rendering document as PDF only. Pages will be ordered according to rearrangements made before.
AddPrintAction - For rendering document as PDF only. An JavaScript action will be added which opens print dialog when PDF document is opened.
|Watermark|Watermark Object|Allows to specify watermark.
|CellsOptions|CellsOptions Object|The Spreadsheet documents rendering options.
|CadOptions|CadOptions Object|The CAD documents rendering options.
|EmailOptions|EmailOptions Object|The Email documents rendering options.
|WordsOptions|WordsOptions Object|The Text documents rendering options.
|PdfOptions|PdfOptions Object|The PDF documents rendering options.
|SlidesOptions|SlidesOptions Object|The Presentation documents rendering options.
|ProjectOptions|ProjectOptions Object|The Microsoft Project documents rendering options.







##  ##

Provides options for rendering document as image.

Example ImageOptions object

```html 
{
  "format": "png",
  "quality": 90,
  "width": 0,
  "height": 0,
  "startPageNumber": 0,
  "countPages": 0,
  "password": "string", 
  "attachmentPassword": "string",
  "extractText": false,
  "renderComments": false,
  "renderHiddenPages": false,	
  "defaultFontName": "string",
  "transforms": [
    "Rotate",
	"Reorder",
	"AddPrintAction"
  ],
  "watermark": {
    "text": "watermark text,
    "color": "Magenta",
    "position": "Diagonal",
    "size": 50
  },
  "cellsOptions": {
    "renderGridLines": false,
    "paginateSheets": false,
    "encoding": "utf-8",
    "internalHyperlinkPrefix": "prefix",
    "countRowsPerPage": 50,
    "textOverflowMode": "OverlayIfNextIsEmpty",
	"ignoreEmptyRows": false
  },
  "cadOptions": {
    "scaleFactor": 50,
    "width": 600,
    "height": 800,
    "renderLayouts": true,
    "layoutName": "Master",
	"layers": ["Layer1"]
  },
  "emailOptions": {
    "encoding": "utf-8"
  },
  "wordsOptions": {
    "encoding": "utf-8",
    "renderTrackedChanges": false
  },
  "pdfOptions": {
    "enablePreciseRendering": false,
    "enableInitialContentOrdering": false,
    "renderLayersSeparately": false
  },
  "slidesOptions": {
    "renderNotes": false
  },
  "projectOptions": {
    "pageSize": "unknown",
    "pageSize": "unknown"
  }
}
 ```

 ImageOptions Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|Format|string|Allows to set image format ("png", "jpg", "bmp").

Default value is "png".
|Quality| int|Allows to specify quality when format # "jpg". Valid values are between 1 and 100. 

Default value is 90.
|Width|int|Allows to specify output image width. 
Specify image width in case when you want to change output image dimensions.
When Width has value and Height value is 0 then Height value will be calculated to save image proportions.
|Height|int|Allows to specify output image height. 
Specify image height in case when you want to change output image dimensions.
When Height has value and Width value is 0 then Width value will be calculated to save image proportions.
|Password|string|Allows to specify document password in case when document is password-protected.
|AttachmentPassword|string|Allows to specify attachment password in case when attachment is password-protected.
|ExtractText|bool|Enables document text extraction. For rendering document as image only.
|RenderComments|bool|Enables document comments rendering.
|DefaultFontName|string|The name of the default font.
 Default font name may be specified in following cases:
- You want to generally specify the default font to fall back on, if particular font
 in the document cannot be found during rendering.
- Your document uses fonts, that contain non-English characters and you want to make sure
 any missing font is replaced with one that has the same character set available.
|Transforms|string[]|Transforms to apply. Available transforms ["Rotate","Reorder","AddPrintAction"].
Rotate - Pages will be rotated on angle if angle was set before.
Reorder - For rendering document as PDF only. Pages will be ordered according to rearrangements made before.
AddPrintAction - For rendering document as PDF only. An JavaScript action will be added which opens print dialog when PDF document is opened.
|Watermark|Watermark Object|Allows to specify watermark.
|CellsOptions|CellsOptions Object|The Spreadsheet documents rendering options.
|CadOptions|CadOptions Object|The CAD documents rendering options.
|EmailOptions|EmailOptions Object|The Email documents rendering options.
|WordsOptions|WordsOptions Object|The Text documents rendering options.
|PdfOptions|PdfOptions Object|The PDF documents rendering options.
|SlidesOptions|SlidesOptions Object|The Presentation documents rendering options.
|ProjectOptions|ProjectOptions Object|The Microsoft Project documents rendering options.







## [HtmlOptions Object]("Html") ##
|---|---

Provides options for rendering document pages as HTML.

Example HtmlOptions object

```html 
{
  "resourcePath": "string",
  "ignoreResourcePathInResources": false
  "embedResources": false,
  "enableMinification": false,
  "enableResponsiveRendering": false,
  "excludeFonts": false,
  "excludeFontsList": ["Arial", "Calibri"],
  "startPageNumber": 0,
  "countPages": 0,
  "password": "document password",
  "attachmentPassword": "attachment password",
  "extractText": false,
  "renderComments": false,
  "defaultFontName": "string",
  "transforms": [
    "Rotate",
	"Reorder",
	"AddPrintAction"
  ],
  "watermark": {
    "text": "watermark text",
    "color": "Magenta",
    "position": "Diagonal",
    "size": 50
  },
  "cellsOptions": {
    "renderGridLines": false,
    "paginateSheets": false,
    "encoding": "utf-8",
    "internalHyperlinkPrefix": "prefix",
    "countRowsPerPage": 50,
    "textOverflowMode": "OverlayIfNextIsEmpty",
	"ignoreEmptyRows": false,
	"renderHiddenRows": false,
	"renderHiddenColumns": false,
	"renderPrintAreaOnly": false
  },
  "cadOptions": {
    "scaleFactor": 50,
    "width": 600,
    "height": 800,
    "renderLayouts": true,
    "layoutName": "Master",
	"layers": ["Layer1"]
  },
  "emailOptions": {
    "encoding": "utf-8"
  },
  "wordsOptions": {
    "encoding": "utf-8",
    "renderTrackedChanges": false
  },
  "pdfOptions": {
    "enablePreciseRendering": false,
    "enableInitialContentOrdering": false,
    "renderLayersSeparately": false,
	"imageQuality": "Low"
  },
  "slidesOptions": {
    "renderNotes": false
  },
  "projectOptions": {
    "pageSize": "unknown",
    "pageSize": "unknown"
  }
}
 ```

 HtmlOptions Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|ResourcePath|string|Allows to specify HTML resources (styles, images and fonts) path.

For example when resource path is http:~/~/example.com/api/pages/{page-number}/resources/{resource-name} the {page-number} and {resource-name} templates will be replaced with page number and resource name accordingly.

Ignored when EmbedResources option is set to true.
|IgnoreResourcePathInResources|bool|Allows to ignore ResourcePath when processing *.css and *.svg files.

When this options is enabled ResourcePath won't be added to resource references in *.css and *.svg files.
| EmbedResources|bool|Controls output HTML document resources (styles, images and fonts) saving.

When this options set to true all resources will be embedded into HTML document and <see cref#"ResourcePath"/> option value will be ignored.
|EnableMinification (added in 18.2)|bool|Enables content (HTML and SVG) minification.
|EnableResponsiveRendering (added in 18.2)|bool|Indicates whether rendering will provide responsive web pages, that look well on different device types.
|ExcludeFonts (added in 18.5)|bool|Prevents adding fonts to the output HTML document.
|ExcludeFontsList (added in 18.11)|string[]|The list of font names, that will be excluded from HTML. Active only when ExcludeFonts is set to false.
|StartPageNumber|int|Allows to specify document page number as starting page to render.
|CountPages|int|Allows to specify count of document pages to render.
|Password|string|Allows to specify document password in case when document is password-protected.
|AttachmentPassword|string|Allows to specify attachment password in case when attachment is password-protected.
|ExtractText|bool|Enables document text extraction. For rendering document as image only.
|RenderComments|bool|Enables document comments rendering.
|RenderHiddenPages|bool|Enables document hidden pages, sheets or slides rendering.
|DefaultFontName|string|The name of the default font.
 Default font name may be specified in following cases:
- You want to generally specify the default font to fall back on, if particular font
 in the document cannot be found during rendering.
- Your document uses fonts, that contain non-English characters and you want to make sure
 any missing font is replaced with one that has the same character set available.
|Transforms|string[]|Transforms to apply. Available transforms ["Rotate","Reorder","AddPrintAction"].
Rotate - Pages will be rotated on angle if angle was set before.
Reorder - For rendering document as PDF only. Pages will be ordered according to rearrangements made before.
AddPrintAction - For rendering document as PDF only. An JavaScript action will be added which opens print dialog when PDF document is opened.
|Watermark|Watermark|Allows to specify watermark.
|CellsOptions|CellsOptions|The Spreadsheet documents rendering options.
|CadOptions|CadOptions|The CAD documents rendering options.
|EmailOptions|EmailOptions|The Email documents rendering options.
|WordsOptions|WordsOptions|The Text documents rendering options.
|PdfOptions|PdfOptions|The PDF documents rendering options.
|SlidesOptions|SlidesOptions|The Presentation documents rendering options.
|ProjectOptions|ProjectOptions|The Microsoft Project documents rendering options.







## [PdfFileOptions Object]("Pdf") ##
|---|---

Provides options for rendering document as PDF.

Example PdfFileOptions object

```html 
{
  "password": "document password",
  "extractText": false,
  "renderComments": false,
  "renderHiddenPages": false,
  "defaultFontName": "string",
  "transforms": [
    "Rotate",
	"Reorder",
	"AddPrintAction"
  ],
  "watermark": {
    "text": "watermark text",
    "color": "Magenta",
    "position": "Diagonal",
    "size": 50
  },
  "cellsOptions": {
    "renderGridLines": false,
    "paginateSheets": false,
    "encoding": "utf-8",
    "internalHyperlinkPrefix": "prefix",
    "countRowsPerPage": 50,
    "textOverflowMode": "OverlayIfNextIsEmpty",
	"ignoreEmptyRows": false
  },
  "cadOptions": {
    "scaleFactor": 50,
    "width": 600,
    "height": 800,
    "renderLayouts": true,
    "layoutName": "Master",
	"layers": ["Layer1"]
  },
  "emailOptions": {
    "encoding": "utf-8"
  },
  "wordsOptions": {
    "encoding": "utf-8",
    "renderTrackedChanges": false
  },
  "pdfOptions": {
    "enablePreciseRendering": false,
    "enableInitialContentOrdering": false,
    "renderLayersSeparately": false
  },
  "slidesOptions": {
    "renderNotes": false
  },
  "projectOptions": {
    "pageSize": "unknown",
    "pageSize": "unknown"
  }
}
 ```

 PdfFileOptions Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|Password|string|Allows to specify document password in case when document is password-protected.
|ExtractText|bool|Enables document text extraction. For rendering document as image only.
|RenderComments|bool|Enables document comments rendering.
|RenderHiddenPages|bool|Enables document hidden pages, sheets or slides rendering.
|DefaultFontName|string|The name of the default font.
 Default font name may be specified in following cases:
- You want to generally specify the default font to fall back on, if particular font
 in the document cannot be found during rendering.
- Your document uses fonts, that contain non-English characters and you want to make sure
 any missing font is replaced with one that has the same character set available.
|Transforms|string[]|Transforms to apply. Available transforms ["Rotate","Reorder","AddPrintAction"].
Rotate - Pages will be rotated on angle if angle was set before.
Reorder - For rendering document as PDF only. Pages will be ordered according to rearrangements made before.
AddPrintAction - For rendering document as PDF only. An JavaScript action will be added which opens print dialog when PDF document is opened.
|Watermark|Watermark Object|Allows to specify watermark.
|CellsOptions|CellsOptions Object|The Spreadsheet documents rendering options.
|CadOptions|CadOptions Object|The CAD documents rendering options.
|EmailOptions|EmailOptions Object|The Email documents rendering options.
|WordsOptions|WordsOptions Object|The Text documents rendering options.
|PdfOptions|PdfOptions Object|The PDF documents rendering options.
|SlidesOptions|SlidesOptions Object|The Presentation documents rendering options.
|ProjectOptions|ProjectOptions Object|The Microsoft Project documents rendering options.







## [RotateOptions Object]("RotateOptionsObject") ##
|---|---

Provides options for rotating document pages.

Example RotateOptions object

```html 
{
  "pageNumber": 1,
  "angle": 90,
  "password": "document password"
}
 ```

 RotateOptions Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|PageNumber|int|The page number which angle should be changed.
|Angle| int|The angle in degrees to which the page should be rotated.
|Password|string|Allows to specify document password in case when document is password-protected.







## [ReorderOptions Object]("ReorderOptions Object")  ##
|---|---

Provides options for reordering document pages.

Example ReorderOptions object

```html 

{
  "pageNumber": 1,
  "newPosition": 2,
  "password": "document password"
}

 ```

 



 ReorderOptions Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|PageNumber|int|The page number which angle should be changed.
|NewPosition|int|The position where page should be placed.
|Password|string|Allows to specify document password in case when document is password-protected.







## [Watermark Object]("WatermarkObject") ##
|---|---

Provides options for watermarking.

Example Watermark object.

```html 
"watermark": {
  "text": "watermark text",
  "color": "Magenta",
  "position": "Diagonal",
  "size": 50
}
 ```

 Watermark Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|Text|string|The watermark text.
|Color|string|The watermark color.
Supported formats "Magenta", "(112,222,11)", "(50,112,222,11)".
Default value is "Red".
|Position|string|The watermark position.
Supported positions "Diagonal", "TopLeft", "TopCenter", "TopRight", "BottomLeft", "BottomCenter" and "BottomRight".
Default value is "Diagonal".
|Size|int|Watermark size in percents.
Default value is 100. 







## [CellsOptions Object]("CellsOptionsObject") ##
|---|---

Provides options for rendering spreadsheet documents.

Example CellOptions object.

```html 
"cellsOptions": {
  "renderGridLines": false,
  "paginateSheets": true,
  "encoding": "utf-8",
  "internalHyperlinkPrefix": "prefix",
  "countRowsPerPage": 50,
  "textOverflowMode": "OverlayIfNextIsEmpty",
  "ignoreEmptyRows": false,
  "renderHiddenRows": false,
  "renderHiddenColumns": false,
  "renderPrintAreaOnly": false
}
 ```

 CellsOptions Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|RenderGridLines|bool|Indicates whether to render grid lines.
|PaginateSheets|bool|Enables worksheets pagination. By default one worksheet is rendered into one page.
|Encoding|string|The text (*.csv) document encoding.
|InternalHyperlinkPrefix|string|Prefix for hyperlink that references worksheet inside the same document.

For rendering document as HTML only.
|CountRowsPerPage|int|The number of rows rendered into one page when PaginateSheets # true.
Default value is 50.
|TextOverflowMode|string|
Text overflow mode applied when the text is too big to fit into the cell.



Supported modes "Overlay", "OverlayIfNextIsEmpty", "HideText" and "AutoFitColumn".



**Overlay** - Overlay next cells even they are not empty.



**OverlayIfNextIsEmpty** - Overlay next cells only if they are not empty



**HideText** - Hide overflow text



**AutoFitColumn** (added in 18.5) - Expand cell width to fit overflowed text



Default value is OverlayIfNextIsEmpty.

|IgnoreEmptyRows|bool|Indicates whether empty rows should be ignored.
|RenderHiddenRows (added in 18.5)|bool|Enables rendering of hidden rows.
|RenderHiddenColumns (added in 18.5)|bool|Enables rendering of hidden columns.
|RenderPrintAreaOnly (added in 18.5)|bool|Enables rendering worksheet(s) sections which is defined as print area.

Renders each print area in a worksheet as a separate page.







## [CadOptions Object]("CellsOptionsObject") ##
|---|---

Provides options for rendering CAD documents.

Example CadOptions object.

```html 
"cadOptions": {
  "scaleFactor": 50,
  "width": 600,
  "height": 800,
  "renderLayouts": true,
  "layoutName": "Master",
  "layers": ["Layer1"]
}
 ```

 CadOptions Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|ScaleFactor|float|The scale factor affects the size of an output document.
|Width|int|The width of the render result in pixels.
|Height|int|The height of the render result in pixels.
|RenderLayouts|bool|Indicates whether layouts from CAD document should be rendered.
|LayoutName|string|The name of the specific layout to render. 
|Layers|string[]|The list of document layers to render. By default all layers will be rendered. Layer names are case sensitive. (since 18.2)







## [EmailOptions Object]("EmailOptionsObject") ##
|---|---

Provides options for rendering Email documents.

Example EmailOptions object.

```html 
"emailOptions": {
  "encoding": "utf-8",
  "pageSize": "Unknown",
  "fieldLabels": [{"field":"From", "Label":"Sender"}]
}
 ```

 EmailOptions Fileds (Click here to expand)

|Name|Type|Description
|---|---|---
|Encoding|string|The document encoding e.g. "utf-8".
|PageSize (added in 18.7)|string|The size of the output page when rendering as PDF or image.
Supported values {Unknown|Letter|Ledger|A0|A1|A2|A3}:
~1. Unknown - the default, unspecified page size.
2. Letter - the size of the Letter page in points is 792x612.
3. Ledger - the size of the Letter page in points is 1224x792.
4. A0 - the size of the A0 page in points is 3371x2384.
5. A1 - the size of the A1 page in points is 2384x1685.
6. A2 - the size of the A2 page in points is 1684x1190.
7. A3 - the size of the A3 page in points is 1190x842.
8. A4 - the size of the A4 page in points is 842x595.
|FieldLabels (added in 18.7)|array|The list of supported email message field labels:
~1. Field: "Anniversary" - default value is "Anniversary".
2. Field: "Attachments" - default value is "Attachments".
3. Field: "Bcc" - default value is "Bcc".
4. Field: "Birthday" - default value is "Birthday".
5. Field: "Business" - default value is "Business".
6. Field: "BusinessAddress" - default value is "Business Address".
7. Field: "BusinessFax" - default value is "Business Fax".
8. Field: "BusinessHomepage" - default value is "BusinessHomePage".
9. Field: "Cc" - default value is "Cc".
10. Field: "Company" - default value is "Company".
~11. Field: "Department" - default value is "Department".
12. Field: "Email" - default value is "Email".
13. Field: "EmailDisplayAs" - default value is "Email Display As".
14. Field: "Email2" - default value is "Email2".
15. Field: "Email2DisplayAs" - default value is "Email2 Display As".
16. Field: "Email3" - default value is "Email3".
17. Field: "Email3DisplayAs" - default value is "Email3 Display As".
18. Field: "End" - default value is "End".
19. Field: "FirstName" - default value is "First Name".
20. Field: "From" - default value is "From".
21. Field: "FullName" - default value is "Full Name".
22. Field: "Gender" - default value is "Gender".
23. Field: "Hobbies" - default value is "Hobbies".
24. Field: "Home" - default value is "Home".
25. Field: "HomeAddress" - default value is "Home Address".
26. Field: "Importance" - default value is "Importance".
27. Field: "JobTitle" - default value is "Job Title".
28. Field: "LastName" - default value is "Last Name".
29. Field: "Location" - default value is "Location".
30. Field: "MiddleName" - default value is "Middle Name".
31. Field: "Mobile" - default value is "Mobile".
32. Field: "Organizer" - default value is "Organizer".
33. Field: "OtherAddress" - default value is "Other Address".
34. Field: "PersonalHomepage" - default value is "PersonalHomePage".
35. Field: "Profession" - default value is "Profession".
36. Field: "Recurrence" - default value is "Recurrence".
37. Field: "RecurrencePattern" - default value is "Recurrence Pattern".
38. Field: "RequiredAttendees" - default value is "Required Attendees".
39. Field: "Sent" - default value is "Sent".
40. Field: "ShowTimeAs" - default value is "Show Time As".
41. Field: "SpousePartner" - default value is "Spouse/Partner".
42. Field: "Start" - default value is "Start".
43. Field: "Subject" - default value is "Subject".
44. Field: "To" - default value is "To".
45. Field: "UserField1" - default value is "User Field 1".
46. Field: "UserField2" - default value is "User Field 2".
47. Field: "UserField3" - default value is "User Field 3".
48. Field: "UserField4" - default value is "User Field 4".







## [WordsOptions Object]("WordsOptionsObject") ##
|---|---

Provides options for rendering Text documents.

Example WordsOptions object.

```html 
"wordsOptions": {
  "encoding": "utf-8",
  "renderTrackedChanges": false
}
 ```

 WordsOptions Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|Encoding|string|The document encoding e.g. "utf-8".
|RenderTrackedChanges|bool|Indicates whether Tracked Changes (Revisions) should be rendered or not.







## [PdfOptions Object]("PdOptionsObject") ##
|---|---

Provides options for rendering PDF documents.

Example PdfOptions object.

```html 
"pdfOptions": {
  "enablePreciseRendering": false,
  "enableInitialContentOrdering": false,
  "renderLayersSeparately": false,
  "imageQuality": "Low"
}
 ```

 PdfOptions Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|EnablePreciseRendering|bool|Indicates whether the PDF document is rendered in a precise mode or not. It is recommended to enable this option when rendering documents with complex content e.g. documents which contains hieroglyphs or any kind o glyphs which should be rendered separately from each other.
|EnableInitialContentOrdering|bool|When this option is enabled content (graphics and text) will be added to HTML document accordingly Z-order in original PDF document. When this option is disabled content (graphics and text) will be added to a single layer.
|RenderLayersSeparately|bool|When this option is enabled layers will be separated from each other in the HTML document.
|ImageQuality (added in 18.5)|string|Specifies output image quality for image resources when rendering as HTML. The default value is Low. Supported values Low, Medium and High:

- Low - satisfying image quality and smallest image size.
- Medium - better image quality and larger image size.
- High - best image quality with largest image size.







## [SlidesOptions Object]("SlidesOptionsObject") ##
|---|---

Provides options for rendering Presentation documents.

Example SlidesOptions object.

```html 
"slidesOptions": {
  "renderNotes": false
}
 ```

 SlidesOptions Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|RenderNotes|bool|Indicates whether slide notes should be rendered.







## [ProjectOptions Object]("ProjectOptionsObject") ##
|---|---

{{< alert style="info" >}}
This object supported starting from v18.2
{{< /alert >}}

Provides options for rendering Microsoft Project documents.

Example ProjectOptions object.

```html 
"projectOptions": {
  "pageSize": "unknown",
  "timeUnit": "unknown",
  "startDate": "2018-10-24T00:00:00",
  "endDate": "2018-11-24T00:00:00"
}
 ```

 ProjectOptions Object Fields (Click here to expand)

|Name|Type|Description
|---|---|---
|PageSize|string|The size of the page.
Supported values {Unknown|Letter|A0|A1|A2|A3}:
~1. Unknown - the default, unspecified page size.
2. Letter - the size of the Letter page in points is 792 × 612.
3. Ledger - the size of the Letter page in points is 1224 × 792.
4. A0 - the size of the A0 page in points is 3371 × 2384.
5. A1 - the size of the A1 page in points is 2384 × 1685.
6. A2 - the size of the A2 page in points is 1684 × 1190.
7. A3 - the size of the A3 page in points is 1190 × 842.
8. A4 - the size of the A4 page in points is 842 × 595.
|TimeUnit|string|The time unit to use as minimal point.
Supported values {Unknown|Days|ThirdsOfMonths|Months}:
~1. Unknown - unknown, unspecified time scale.
2. Days - one day interval.
3. ThirdsOfMonths - one third of the month.
4. Months - one month interval.
|StartDate 

 |DateTime|The start date of a Gantt Chart View to render. 
|---|---

Supported starting from v18.11

 
|EndDate|DateTime|The end date of a Gantt Chart View to render.
|---|---|---

Supported starting from v18.11 







## [OutlookOptions Object]("OutlookOptions")  ##
|---|---

{{< alert style="info" >}}
OutlookOptions supported starting from v18.11
{{< /alert >}}

Provides options for rendering Microsoft Outlook data files (.pst|.ost).
|---

Example of OutlookOptions

```html 
"outlookOptions": {
  "maxItemsInFolder": "1000"
}
 ```

 OutlookOptions fields

|Name|Type|Description
|---|---|---
|MaxItemsInFolder|int|The limit of items to render in mailbox folders





