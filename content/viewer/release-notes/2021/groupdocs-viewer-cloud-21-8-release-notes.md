---
id: "groupdocs-viewer-cloud-21-8-release-notes"
url: "viewer/groupdocs-viewer-cloud-21-8-release-notes"
title: "GroupDocs.Viewer Cloud 21.8 Release Notes"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

This page contains release notes for GroupDocs.Viewer Cloud 21.8

## Major Features ##

+ Added new rendering options for Archive, Email, Pdf, WordProcessing and Text files formats
+ Added support for Mail storage (Lotus notes), Visio files formats
+ Added ability to set or limit images width/height when rendering to HTML/PDF
+ Added ability to limit width/height when rendering to Image
+ Added optimization for printing when rendering to HTML

## Full List of Issues Covering all Changes in this Release ##

|Key|Summary|Category
|---|---|---
|VIEWERCLOUD-413|Set output image size limits when rendering single image to PDF/HTML|Feature
|VIEWERCLOUD-414|Optimize output HTML for printing|Feature
|VIEWERCLOUD-415|Configure count of characters per row and rows per page to render|Feature
|VIEWERCLOUD-412|Review & Update Cloud SDK Tags at Nuget.org|Task

## Public API and Backward Incompatible Changes ##

The list of added options in this release:

|Property|Type|Description
|---|---|---
HtmlOptions.ForPrinting|bool|Indicates whether to optimize output HTML for printing
HtmlOptions.ImageHeight, PdfOptions.ImageHeight|int|The height of an output image in pixels
HtmlOptions.ImageWidth, PdfOptions.ImageHeight|int|The width of the output image in pixels
HtmlOptions.ImageMaxHeight, PdfOptions.ImageMaxHeight|int|Max height of an output image in pixels
HtmlOptions.ImageMaxWidth, PdfOptions.ImageMaxWidth|int|Max width of an output image in pixels
RenderOptions.TextOptions|TextOptions|Rendering options for Text source file formats
TextOptions.MaxCharsPerRow|int|Max chars per row on page. Default value is 85
TextOptions.MaxRowsPerPage|int|Max rows per page. Default value is 55
RenderOptions.MailStorageOptions|MailStorageOptions|Rendering options for Mail storage (Lotus Notes, MBox) data files
MailStorageOptions.TextFilter|string|The keywords used to filter messages
MailStorageOptions.AddressFilter|string|The email-address used to filter messages by sender or recipient
MailStorageOptions.MaxItems|int|The maximum number of messages or items for render. Default value is 0 - all messages will be rendered
RenderOptions.VisioRenderingOptions|VisioRenderingOptions|Rendering options for Visio source file formats
VisioRenderingOptions.RenderFiguresOnly|bool|Render only Visio figures, not a diagram
VisioRenderingOptions.FigureWidth|int|Figure width, height will be calculated automatically. Default value is 100
ArchiveOptions.FileName|string|The filename to display in the header. By default the name of the source file is displayed
ArchiveOptions.ItemsPerPage|int| Number of records per page (for rendering to HTML only)
EmailOptions.DateTimeFormat|string|Time Format (can be include TimeZone) for example: 'MM d yyyy HH:mm tt'
EmailOptions.TimeZoneOffset|string|Message time zone offset. Format should be compatible with .net TimeSpan
PdfDocumentOptions.RenderTextAsImage|bool|When this option is set to true, the text is rendered as an image in the output HTML
WordProcessingOptions.LeftMargin|float|Left page margin (for HTML rendering only)
WordProcessingOptions.RightMargin|float|Right page margin (for HTML rendering only)
WordProcessingOptions.TopMargin|float|Top page margin (for HTML rendering only)
WordProcessingOptions.BottomMargin|float|Bottom page margin (for HTML rendering only)
