---
title : "Aspose.3D for .NET 19.5 Release Notes" 
description : "" 
weight : 12108 
toc : false
type: docs
url: /net/releasenotes/2019/aspose.3d+for+.net+19.5+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 19.5 Release Notes


This page contains release notes for [Aspose.3D for .NET 19.5](https://www.nuget.org/packages/Aspose.3D/19.5.0)

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-501|Integrate with latest Dynabic.Metered|Enhancement|
|THREEDNET-505|Allow change plane's orientation by specifying an up normal|Enhancement|
|THREEDNET-489|Shadow is not working in Vulkan renderer|Bug|
|THREEDNET-504|Draco created from STL file is broken|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

#### Added new property Radius in class Aspose.ThreeD.Entities.Plane

{{< code lang="cs" >}}
/// <summary>
/// Gets or sets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane
/// </summary>
public Vector3 Up { get; set; }
{{< /code >}}

Sample code to specify radius by property rather than constructor argument:

{{< code lang="cs" >}}
Scene scene = new Scene();
scene.RootNode.CreateChildNode(new Plane() {Up = new Vector3(1, 1, 3)});
//This will generate a plane that has customized orientation
scene.Save("test.obj", FileFormat.WavefrontOBJ);
{{< /code >}}

#### Added new method "GetConsumptionCredit" in class Aspose.ThreeD.Metered

{{< code lang="cs" >}}
/// <summary>
/// Gets consumption credit
/// </summary>
/// <returns>consumption quantity</returns>
public static decimal GetConsumptionCredit();
{{< /code >}}

Gets the consumption credit of current month, used by Dynabic.Metered billing service.

