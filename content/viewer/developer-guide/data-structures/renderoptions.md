---
id: "renderoptions"
url: "viewer/renderoptions"
title: "RenderOptions"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

# RenderOptions #

RenderOptions data structure used as part of [ViewOptions ]({{< ref "viewer/developer-guide/data-structures/viewoptions.md" >}}))data structure. 
|---|---

{{< alert style="info" >}}
Not all options are supported by all document formats. Each option may correspond to one or more formats.
{{< /alert >}}

 

##### RenderOptions example #####

```html 

{
    "StartPageNumber": 0,
    "CountPagesToRender": 0,
    "DefaultFontName": "string",
    "DefaultEncoding": "string",
    "RenderComments": true,
    "RenderHiddenPages": true,
    "SpreadsheetOptions": {
      "PaginateSheets": true,
      "CountRowsPerPage": 0,
      "RenderGridLines": true,
      "RenderEmptyRows": true,
      "RenderEmptyColumns": true,
      "RenderHiddenRows": true,
      "RenderHiddenColumns": true,
      "RenderPrintAreaOnly": true
    },
    "CadOptions": {
      "ScaleFactor": 0,
      "Width": 0,
      "Height": 0
    },
    "EmailOptions": {
      "PageSize": "string",
      "FieldLabels": [
        {
          "Field": "string",
          "Label": "string"
        }
      ]
    },
    "ProjectManagementOptions": {
      "PageSize": "string",
      "TimeUnit": "string",
      "StartDate": "2019-02-26T10:48:23.911Z",
      "EndDate": "2019-02-26T10:48:23.911Z"
    }
 }

 ```

##### RenderOptions fields #####

|Name|Description
|---|---
|StartPageNumber|Page number, from which to start rendering. Rendering starts from first page by default.
|CountPagesToRender|Number of pages to render. All document pages rendered by default (or rest of pages, if StartPageNumber provided).
|DefaultFontName|The name of the default font.
 Default font name may be specified in following cases:
- You want to generally specify the default font to fall back on, if particular font
 in the document cannot be found during rendering.
- Your document uses fonts, that contain non-English characters and you want to make sure
 any missing font is replaced with one that has the same character set available.
|DefaultEncoding|Document encoding
|RenderComments|Indicates whether to render comments.
|RenderHiddenPages|Indicates whether hidden pages should be rendered.
|SpreadsheetOptions.PaginateSheets|Enables worksheets pagination. By default one worksheet is rendered into one page.
|SpreadsheetOptions.CountRowsPerPage|The number of rows rendered into one page when PaginateSheets # true.
Default value is 50.
|SpreadsheetOptions.RenderGridLines|Indicates whether to render grid lines.
|SpreadsheetOptions.RenderEmptyRows|Indicates whether empty rows should be rendered.
|SpreadsheetOptions.RenderEmptyColumns|Indicates whether empty columns should be rendered.
|SpreadsheetOptions.RenderHiddenRows|Enables rendering of hidden rows.
|SpreadsheetOptions.RenderHiddenColumns|Enables rendering of hidden columns.
|SpreadsheetOptions.RenderPrintAreaOnly|Enables rendering worksheet(s) sections which is defined as print area.

Renders each print area in a worksheet as a separate page.
|CadOptions.ScaleFactor|The scale factor affects the size of an output document.
|CadOptions.Width|The width of the render result in pixels.
|CadOptions.Height|The height of the render result in pixels.
|EmailOptions.PageSize|The size of the output page when rendering as PDF or image.
Supported values {Unknown|Letter|Ledger|A0|A1|A2|A3}:
~1. Unknown - the default, unspecified page size.
2. Letter - the size of the Letter page in points is 792x612.
3. Ledger - the size of the Letter page in points is 1224x792.
4. A0 - the size of the A0 page in points is 3371x2384.
5. A1 - the size of the A1 page in points is 2384x1685.
6. A2 - the size of the A2 page in points is 1684x1190.
7. A3 - the size of the A3 page in points is 1190x842.
8. A4 - the size of the A4 page in points is 842x595.
|EmailOptions.FieldLabels|The list of supported email message field labels
|ProjectManagementOptions.PageSize|The size of the page.
Supported values {Unknown|Letter|A0|A1|A2|A3}:
~1. Unknown - the default, unspecified page size.
2. Letter - the size of the Letter page in points is 792 × 612.
3. Ledger - the size of the Letter page in points is 1224 × 792.
4. A0 - the size of the A0 page in points is 3371 × 2384.
5. A1 - the size of the A1 page in points is 2384 × 1685.
6. A2 - the size of the A2 page in points is 1684 × 1190.
7. A3 - the size of the A3 page in points is 1190 × 842.
8. A4 - the size of the A4 page in points is 842 × 595.
|ProjectManagementOptions.TimeUnit|The time unit to use as minimal point.
Supported values {Unknown|Days|ThirdsOfMonths|Months}:
~1. Unknown - unknown, unspecified time scale.
2. Days - one day interval.
3. ThirdsOfMonths - one third of the month.
4. Months - one month interval.
|ProjectManagementOptions.StartDate|The start date of a Gantt Chart View to render. 
|ProjectManagementOptions.EndDate|The end date of a Gantt Chart View to render.

