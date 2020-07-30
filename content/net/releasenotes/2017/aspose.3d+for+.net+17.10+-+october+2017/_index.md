---
title : "Aspose.3D for .NET 17.10 - October 2017" 
description : "" 
weight : 12129 
toc : false
type: docs
url: /net/releasenotes/2017/aspose.3d+for+.net+17.10+-+october+2017/
---

# Aspose.3D for .NET : Aspose.3D for .NET 17.10 - October 2017


This page contains release notes for [Aspose.3D for .NET 17.10](https://www.nuget.org/packages/Aspose.3D/17.10.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-292|Add support of importing 3MF|New feature|
|THREEDNET-302|OBJ to GLTF - incomplete rendering of 3D model|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

#### Adds Microsoft3MF member to Aspose.ThreeD.FileFormat and Aspose.ThreeD.FileFormatType classes

**C#**

{{< code lang="c#" >}}
/// <summary>
/// Microsoft 3D Manufacturing Format
/// </summary>
public static readonly Aspose.ThreeD.FileFormat Microsoft3MF;
 
/// <summary>
/// Microsoft 3D Manufacturing Format
/// </summary>
public static readonly Aspose.ThreeD.FileFormatType Microsoft3MF;
{{< /code >}}

The auto format detection is supported for 3MF file, so developers can import it directly with Scene class constructor without explicitly specify the FileFormat.

**C#**

Scene scene = new Scene("sphere\_logo.3mf");

