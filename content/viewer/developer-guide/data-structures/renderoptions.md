---
id: "renderoptions"
url: "viewer/renderoptions"
title: "RenderOptions"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

RenderOptions data structure used as part of [ViewOptions]({{< ref "viewer/developer-guide/data-structures/viewoptions.md" >}}) data structure.

{{< alert style="info" >}}
Not all options are supported by all document formats. Each option may correspond to one or more formats.
{{< /alert >}}

### RenderOptions example

```json
 {
    "StartPageNumber": 0,
    "CountPagesToRender": 0,
    "PagesToRender": [
      0
    ],
    "PageRotations": [
      {
        "PageNumber": 0,
        "RotationAngle": "On90Degree"
      }
    ],
    "DefaultFontName": "string",
    "DefaultEncoding": "string",
    "DetectEncoding": true,
    "RenderComments": true,
    "RenderNotes": true,
    "RenderHiddenPages": true,
    "SpreadsheetOptions": {
      "PaginateSheets": true,
      "CountRowsPerPage": 0,
      "CountColumnsPerPage": 0,
      "RenderGridLines": true,
      "RenderEmptyRows": true,
      "RenderEmptyColumns": true,
      "RenderHiddenRows": true,
      "RenderHiddenColumns": true,
      "RenderHeadings": true,
      "RenderPrintAreaOnly": true,
      "TextOverflowMode": "Overlay"
    },
    "CadOptions": {
      "ScaleFactor": 0,
      "Width": 0,
      "Height": 0,
      "Tiles": [
        {
          "StartPointX": 0,
          "StartPointY": 0,
          "Width": 0,
          "Height": 0
        }
      ],
      "RenderLayouts": true,
      "LayoutName": "string",
      "Layers": [
        "string"
      ]
    },
    "EmailOptions": {
      "PageSize": "Unspecified",
      "FieldLabels": [
        {
          "Field": "string",
          "Label": "string"
        }
      ],
      "DateTimeFormat": "string",
      "TimeZoneOffset": "string"
    },
    "ProjectManagementOptions": {
      "PageSize": "Unspecified",
      "TimeUnit": "Unspecified",
      "StartDate": "2024-03-25T06:24:32.674Z",
      "EndDate": "2024-03-25T06:24:32.674Z"
    },
    "PdfDocumentOptions": {
      "DisableCharsGrouping": true,
      "EnableLayeredRendering": true,
      "EnableFontHinting": true,
      "RenderOriginalPageSize": true,
      "ImageQuality": "Low",
      "RenderTextAsImage": true,
      "FixedLayout": true,
      "WrapImagesInSvg": true,
      "DisableFontLicenseVerifications": true
    },
    "WordProcessingOptions": {
      "RenderTrackedChanges": true,
      "LeftMargin": 0,
      "RightMargin": 0,
      "TopMargin": 0,
      "BottomMargin": 0
    },
    "OutlookOptions": {
      "Folder": "string",
      "TextFilter": "string",
      "AddressFilter": "string",
      "MaxItemsInFolder": 0
    },
    "ArchiveOptions": {
      "Folder": "string",
      "FileName": "string",
      "ItemsPerPage": 0
    },
    "TextOptions": {
      "MaxCharsPerRow": 0,
      "MaxRowsPerPage": 0
    },
    "MailStorageOptions": {
      "TextFilter": "string",
      "AddressFilter": "string",
      "MaxItems": 0
    },
    "VisioRenderingOptions": {
      "RenderFiguresOnly": true,
      "FigureWidth": 0
    },
    "WebDocumentOptions": {
      "PageSize": "Unspecified",
      "LeftMargin": 0,
      "RightMargin": 0,
      "TopMargin": 0,
      "BottomMargin": 0
    }
  }

```

### RenderOptions fields

|Name|Description
|---|---
|StartPageNumber|Page number, from which to start rendering. Rendering starts from first page by default.
|CountPagesToRender|Number of pages to render. All document pages rendered by default (or rest of pages, if StartPageNumber provided).
|DefaultFontName|The name of the default font. Default font name may be specified in following cases: You want to generally specify the default font to fall back on, if particular font  in the document cannot be found during rendering. Your document uses fonts, that contain non-English characters and you want to make sure any missing font is replaced with one that has the same character set available.
|DefaultEncoding|Document encoding
|RenderComments|Indicates whether to render comments.
|RenderHiddenPages|Indicates whether hidden pages should be rendered.
|SpreadsheetOptions.PaginateSheets|Enables worksheets pagination. By default one worksheet is rendered into one page.
|SpreadsheetOptions.CountRowsPerPage|The number of rows rendered into one page when PaginateSheets = true. Default value is 50.
|SpreadsheetOptions.RenderGridLines|Indicates whether to render grid lines.
|SpreadsheetOptions.RenderEmptyRows|Indicates whether empty rows should be rendered.
|SpreadsheetOptions.RenderEmptyColumns|Indicates whether empty columns should be rendered.
|SpreadsheetOptions.RenderHiddenRows|Enables rendering of hidden rows.
|SpreadsheetOptions.RenderHiddenColumns|Enables rendering of hidden columns.
|SpreadsheetOptions.RenderPrintAreaOnly|Enables rendering worksheet(s) sections which is defined as print area. Renders each print area in a worksheet as a separate page.
|CadOptions.ScaleFactor|The scale factor affects the size of an output document.
|CadOptions.Width|The width of the render result in pixels.
|CadOptions.Height|The height of the render result in pixels.
|EmailOptions.PageSize|The size of the output page when rendering as PDF or image.Supported values {Unknown,Letter,Ledger,A0,A1,A2,A3}: 1. Unknown - the default, unspecified page size. 2. Letter - the size of the Letter page in points is 792x612.3. Ledger - the size of the Letter page in points is 1224x792. 4. A0 - the size of the A0 page in points is 3371x2384. 5. A1 - the size of the A1 page in points is 2384x1685. 6. A2 - the size of the A2 page in points is 1684x1190. 7. A3 - the size of the A3 page in points is 1190x842. 8. A4 - the size of the A4 page in points is 842x595.
|EmailOptions.FieldLabels|The list of supported email message field labels.
|EmailOptions.DateTimeFormat|Time Format (can be include TimeZone) for example: 'MM d yyyy HH:mm tt', if not set - current system format is used.
|EmailOptions.TimeZoneOffset|Message time zone offset. Format should be compatible with .net TimeSpan
|ProjectManagementOptions.PageSize|The size of the page. Supported values {Unknown,Letter,A0,A1,A2,A3}: 1. Unknown - the default, unspecified page size. 2. Letter - the size of the Letter page in points is 792 × 612. 3. Ledger - the size of the Letter page in points is 1224 × 792. 4. A0 - the size of the A0 page in points is 3371 × 2384. 5. A1 - the size of the A1 page in points is 2384 × 1685. 6. A2 - the size of the A2 page in points is 1684 × 1190. 7. A3 - the size of the A3 page in points is 1190 × 842. 8. A4 - the size of the A4 page in points is 842 × 595.
|ProjectManagementOptions.TimeUnit|The time unit to use as minimal point. Supported values {Unknown,Days,ThirdsOfMonths,Months}: 1. Unknown - unknown, unspecified time scale. 2. Days - one day interval. 3. ThirdsOfMonths - one third of the month. 4. Months - one month interval.
|ProjectManagementOptions.StartDate|The start date of a Gantt Chart View to render.
|ProjectManagementOptions.EndDate|The end date of a Gantt Chart View to render.
|PdfDocumentOptions.DisableCharsGrouping|Disables chars grouping to keep maximum precision during chars positioning when rendering the page.
|PdfDocumentOptions.EnableLayeredRendering|Enables rendering of text and graphics according to z-order in original PDF document when rendering into HTML.
|PdfDocumentOptions.EnableFontHinting|Enables font hinting. The font hinting adjusts the display of an outline font. Supported only for TTF fonts when these fonts are used in source document.
|PdfDocumentOptions.RenderOriginalPageSize|When this option enabled the output pages will have the same size in pixels as page size in a source PDF document. By default GroupDocs.Viewer calculates output image page size for better rendering quality. This option is supported when rendering into PNG or JPG formats.
|PdfDocumentOptions.ImageQuality|Specifies output image quality for image resources when rendering into HTML. The default value is Low.
|PdfDocumentOptions.RenderTextAsImage|When this option is set to true, the text is rendered as an image in the output HTML. Enable this option to make text unselectable or to fix characters rendering and make HTML look like PDF. The default value is false. This option is supported when rendering into HTML.
|PdfDocumentOptions.FixedLayout|Enables rendering the PDF and EPUB documents to HTML with a fixed layout.
|PdfDocumentOptions.WrapImagesInSvg|Enables wrapping each image in the output HTML document in SVG tag to improve the output quality.
|PdfDocumentOptions.DisableFontLicenseVerifications|Disables any license restrictions for all fonts in the current XPS/OXPS document.
|WordProcessingOptions.RenderTrackedChanges|Enables tracked changes (revisions) rendering.
|WordProcessingOptions.LeftMargin|Left page margin (for HTML rendering only).
|WordProcessingOptions.RightMargin|Right page margin (for HTML rendering only).
|WordProcessingOptions.TopMargin|Top page margin (for HTML rendering only).
|WordProcessingOptions.BottomMargin|Bottom page margin (for HTML rendering only).
|OutlookOptions.Folder|The name of the folder (e.g. Inbox, Sent Item or Deleted Items) to render.
|OutlookOptions.TextFilter|The keywords used to filter messages.
|OutlookOptions.AddressFilter|The email-address used to filter messages by sender or recipient.
|OutlookOptions.MaxItemsInFolder|The maximum number of messages or items, that can be rendered from one folder.
|ArchiveOptions.Folder|The folder inside the archive to be rendered.
|ArchiveOptions.FileName|The filename to display in the header. By default the name of the source file is displayed.
|ArchiveOptions.ItemsPerPage|Number of records per page (for rendering to HTML only).
|TextOptions.MaxCharsPerRow|Max chars per row on page. Default value is 85.
|TextOptions.MaxRowsPerPage|Max rows per page. Default value is 55.
|MailStorageOptions.TextFilter|The keywords used to filter messages.
|MailStorageOptions.AddressFilter|The email-address used to filter messages by sender or recipient.
|MailStorageOptions.MaxItems|The maximum number of messages or items for render. Default value is 0 - all messages will be rendered.
|VisioRenderingOptions.RenderFiguresOnly|Render only Visio figures, not a diagram.
|VisioRenderingOptions.FigureWidth|Figure width, height will be calculated automatically. Default value is 100.
|WebDocumentOptions.PageSize|The size of the output page. The default value is GroupDocs.Viewer.Options.PageSize.Letter 792 x 612 points. When contents does not fit set a larger page size e.g. GroupDocs.Viewer.Options.PageSize.A3.
|WebDocumentOptions.LeftMargin|The distance (in points) between the left edge of the page and the left boundary of the body text. The default value is 5 points.
|WebDocumentOptions.RightMargin|The distance (in points) between the right edge of the page and the left boundary of the body text. The default value is 5 points.
|WebDocumentOptions.TopMargin|The distance (in points) between the top edge of the page and the left boundary of the body text. The default value is 5 points.
|WebDocumentOptions.BottomMargin|The distance (in points) between the bottom edge of the page and the left boundary of the body text. The default value is 5 points.
