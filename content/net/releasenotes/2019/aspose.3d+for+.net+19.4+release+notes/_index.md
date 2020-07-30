---
title : "Aspose.3D for .NET 19.4 Release Notes" 
description : "" 
weight : 12109 
toc : false
type: docs
url: /net/releasenotes/2019/aspose.3d+for+.net+19.4+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 19.4 Release Notes


This page contains release notes for [Aspose.3D for .NET 19.4](https://www.nuget.org/packages/Aspose.3D/19.4.0)

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-471|XPath like object addressing methods|New feature|
|THREEDNET-483|Support for VRML format  |New feature|
|THREEDNET-493|Added vulkan renderer support in .NET Core version|New feature|
|THREEDNET-496|FBX7500Binary Export Corruption Issue|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

#### Added new property Radius in class Aspose.ThreeD.Entities.Sphere

{{< code lang="cs" >}}
/// <summary>
/// Gets or sets the radius of the sphere.
/// </summary>
public double Radius { get; set; }
{{< /code >}}

Sample code to specify radius by property rather than constructor argument:

{{< code lang="cs" >}}
Scene scene = new Scene();
scene.RootNode.CreateChildNode(new Sphere() {Radius = 10});
scene.Save("sphere.obj", FileFormat.WavefrontOBJ);
{{< /code >}}

#### Added new file format VRML in class Aspose.ThreeD.FileFormat and Aspose.ThreeD.FileFormatType

{{< code lang="cs" >}}
/// <summary>
/// The Virtual Reality Modeling Language
/// </summary>
public static readonly FileFormat VRML;
{{< /code >}}

Aspose.3D can auto detect VRML format, so the FileFormat is usually ignored in Open method. Sample code:

{{< code lang="cs" >}}
Scene scene = new Scene();
scene.Open("test.wrl");
{{< /code >}}

