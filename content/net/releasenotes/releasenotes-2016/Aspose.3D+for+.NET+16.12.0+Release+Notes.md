+++
title = "Aspose.3D for .NET 16.12.0 Release Notes" 
description = "" 
weight = 12140 
+++

Aspose.3D for .NET : Aspose.3D for .NET 16.12.0 Release Notes  

# Aspose.3D for .NET : Aspose.3D for .NET 16.12.0 Release Notes


This page contains release notes for [Aspose.3D for .NET 16.12.0](https://www.nuget.org/packages/Aspose.3D/16.12.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-223|Add support of importing the DXF.|New feature|
|THREEDNET-224|Add a metered License key system.|New feature|
|THREEDNET-226|Can't extract 3D data from a PDF.|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

### Adds a DXF format entry in the Aspose.ThreeD.FileFormat Class

We have added a DXF (Graphic Image Format) entry for the importing purposes. The auto-detect for DXF file is supported, so usually developers don't need to manually specify this file format when opening a DXF file (using Scene class).

### Adds Aspose.ThreeD.Metered Class

We have added `Metered` class. It allows developers to unlock the evaluation limitations of Aspose.3D API as well as track and maintain API licenses. It also monitors the regular usage of Aspose.3D API. To apply the metered licensing system, developers can create an object of the `Metered` class and call its `SetMeteredKey` method. The `SetMeteredKey` method takes two string parameters as public and private keys. Our clients can get the public and private keys from Aspose.

### Usage Examples

Please check the list of help topics added in the Aspose.3D Wiki docs:

1.  [Reading a 3D Scene](http://www.aspose.com/docs/display/3dnet/Create+and+Read+an+Existing+3D+Scene#CreateandReadanExisting3DScene-Readinga3DScene)
2.  [Set Public and Private Keys to Apply Metered License](http://docs.asposeptyltd.com/docs/display/3dnet/Licensing#Licensing-SetPublicandPrivateKeystoApplyMeteredLicense)

