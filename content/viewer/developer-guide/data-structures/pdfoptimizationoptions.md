---
id: "pdfoptimizationoptions"
url: "viewer/pdfoptimizationoptions"
title: "PdfOptimizationOptions"
productName: "GroupDocs.Viewer Cloud"
weight: 1
description: ""
keywords: ""
---

PdfOptimizationOptions data structure contains the PDF optimization options to apply to the output PDF file.

##### ImageOptions example #####

```html

{
    "Lineriaze": false,
    "RemoveAnnotations": false,
    "RemoveFormFields": false,
    "ConvertToGrayScale": false,
    "SubsetFonts": false,
    "CompressImages": false,
    "ImageQuality": 100,
    "ResizeImages": false,
    "MaxResolution": 300,
    "OptimizeSpreadsheets": false
}

```

##### ImageOptions fields #####

|Name|Description
|---|---
|Lineriaze|Enables optimization the output PDF file for viewing online with a web browser. This optimization allows a browser to display the first pages of a PDF file when you open the document, instead of waiting for the entire file to download.
|RemoveAnnotations|Enables removing annotation from the output PDF file.
|RemoveFormFields|Enables removing form fields from a PDF file.
|ConvertToGrayScale|Enables converting the output PDF file to a grayscale.
|SubsetFonts|Subsets fonts in the output PDF file. If the file uses embedded fonts, it contains all font data. GroupDocs.Viewer Cloud can subset embedded fonts to reduce the file size.
|CompressImages|Enables compressing images in the output PDF file. Use this option to allow other compressing options: PdfOptimizationOptions.ImageQuality and PdfOptimizationOptions.MaxResolution.
|ImageQuality|Sets the image quality in the output PDF file (in percent). To change the image quality, first set the PdfOptimizationOptions.CompressImages property to true.
|ResizeImages|Enables setting the maximum resolution in the output PDF file. To allow this option, set the GroupDocs.Viewer.Options.PdfOptimizationOptions.CompressImages property to true. This option allows setting the GroupDocs.Viewer.Options.PdfOptimizationOptions.MaxResolution property.
|MaxResolution|Sets the maximum resolution in the output PDF file. To allow this option, set the GroupDocs.Viewer.Options.PdfOptimizationOptions.CompressImages and GroupDocs.Viewer.Options.PdfOptimizationOptions.MaxResolution properties to true. The default value is 300.
|OptimizeSpreadsheets|Enables optimization of spreadsheets in the PDF files. This optimization allows to reduce the output file size by setting up border lines. Besides that, it removes the Arial and Times New Roman characters of 32-127 codes.
