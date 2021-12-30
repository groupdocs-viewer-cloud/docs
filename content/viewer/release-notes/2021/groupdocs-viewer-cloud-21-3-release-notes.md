---
id: "groupdocs-viewer-cloud-21-3-release-notes"
url: "viewer/groupdocs-viewer-cloud-21-3-release-notes"
title: "GroupDocs.Viewer Cloud 21.3 Release Notes"
productName: "GroupDocs.Viewer Cloud"
weight: 4
description: ""
keywords: ""
---

This page contains release notes for GroupDocs.Viewer Cloud 21.3

## Major Features ##

+ Added support of adobe illustrator (.ai) file format
+ Updated PdfOptions to accept an array of Permissions instead of a single value

## Full List of Issues Covering all Changes in this Release ##

|Key|Summary|Category
|---|---|---
|VIEWERCLOUD-94|Support of AI (Adobe Illustrator) file Format|Feature
|VIEWERCLOUD-400|Update PdfOptions to accept an array of Permissions instead of a single value|Improvement

## Public API and Backward Incompatible Changes ##

Changed type of the option PdfViewOptions.Permissions from enum Permissions to List of strings,
so it is possible to set multiple values that will be combined into document permission.
Note: permissions applied only if PermissionsPassword property set.
