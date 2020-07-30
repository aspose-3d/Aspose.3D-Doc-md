---
title : "Aspose.3D for .NET 16.9.0 Release Notes" 
description : "" 
weight : 12142 
toc : false
type: docs
url: /net/releasenotes/2016/aspose.3d+for+.net+16.9.0+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 16.9.0 Release Notes


This page contains release notes for [Aspose.3D for .NET 16.9.0](https://www.nuget.org/packages/Aspose.3D/16.9.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-209|Generate tangent from mesh data.|New feature|
|THREEDNET-208|Normal mapping in rendering.|New feature|
|THREEDNET-182|Export 3D scene to PDF 1.6.|New feature|
|THREEDNET-205|Import 3D scenes from a PDF file.|New feature|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list for any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

### Save a 3D Scene in the PDF Format

Using the recent version (16.9.0) or higher, developers can save all supported 3D files in the PDF format.

#### Adds Aspose.ThreeD.Formats.PdfSaveOptions Class

We have added `PdfSaveOptions` class. It helps in applying setting before saving in the output PDF format.

#### Adds Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums

Developers can set a rendering mode and lighting scheme before saving a 3D scene into the PDF format.

### Import 3D Scene from the Source PDF

Using the recent version (16.9.0) or higher, developers can retrieve 3D scenes from an input PDF file.

#### Adds Aspose.ThreeD.Formats.PdfLoadOptions Class

We have added `PdfLoadOptions` class. It helps in loading content from the input PDF file. Developers may apply password for the protected PDFs.

#### Adds PDF format in the Aspose.ThreeD.FileFormat Class

We have added an entry of PDF format for loading and saving purposes.

#### Adds Aspose.ThreeD.Formats.PdfFormat Class

We have added `PdfFormat` class. It helps to manipulate PDFs.

### Adds Triangulate Method in the Aspose.ThreeD.Entities.PolygonModifier Class

We have added another overload of `Triangulate` method in the PolygonModifier class which takes a Scene class object as a parameter.

#### Adds two BuildTangentBinormal Methods in the Aspose.ThreeD.Entities.PolygonModifier Class

We have added two BuildTangentBinormal methods in the PolygonModifier class. One method takes the Scene class object as a parameter and another one takes the Mesh class object as a parameter.

### Usage Examples

Please check the list of help topics added in the Aspose.3D Wiki docs:

*   [Import 3D Scenes and Contents from a PDF](http://www.aspose.com/docs/display/3dnet/Import+3D+Scenes+and+Contents+from+a+PDF)
*   [Save a 3D Scene in the PDF](http://www.aspose.com/docs/display/3dnet/Save+a+3D+Scene+in+the+PDF)
*   [Convert All Polygons to Triangles in 3D Files](http://www.aspose.com/docs/display/3dnet/Convert+All+Polygons+to+Triangles+in+3D+Files)
*   [Build Tangent and Binormal Data for All Meshes in 3D Files](http://www.aspose.com/docs/display/3dnet/Build+Tangent+and+Binormal+Data+for+All+Meshes+in+3D+Files)

