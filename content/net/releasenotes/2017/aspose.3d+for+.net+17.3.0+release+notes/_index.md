---
title : "Aspose.3D for .NET 17.3.0 Release Notes" 
description : "" 
weight : 12136 
toc : false
type: docs
url: /net/releasenotes/2017/aspose.3d+for+.net+17.3.0+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 17.3.0 Release Notes


This page contains release notes for [Aspose.3D for .NET 17.3.0](https://www.nuget.org/packages/Aspose.3D/17.3.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-233|Add support of importing Google Draco (.drc) files.|New feature|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

#### Adds Draco format entry in the Aspose.ThreeD.FileFormat Class

This release of Aspose.3D for .NET API has added support of importing Google Draco(.drc) files. Developers can import a Google Draco file, and then save it in any supported 3D format.

This code example demonstrates how to import a Google Draco file into Aspose.3D API:

**.NET, C#**

{{< code lang="cs" >}}
// Initialize a Scene class object
Scene scene = new Scene();
// load an existing 3D document
scene.Open("document.drc", FileFormat.Draco);
{{< /code >}}

### Usage Examples

Please check the list of help topics added in the Aspose.3D Wiki docs:

1.  [Read a 3D Scene](https://docs.aspose.com//display/3dnet/Create+and+Read+an+Existing+3D+Scene#CreateandReadanExisting3DScene-Readinga3DScene)

