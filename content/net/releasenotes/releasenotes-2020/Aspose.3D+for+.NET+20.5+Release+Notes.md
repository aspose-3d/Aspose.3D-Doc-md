+++
title = "Aspose.3D for .NET 20.5 Release Notes" 
description = "" 
weight = 12095 
+++

Aspose.3D for .NET : Aspose.3D for .NET 20.5 Release Notes  

# Aspose.3D for .NET : Aspose.3D for .NET 20.5 Release Notes


This page contains release notes information forAspose.3D for .NET 20.5.

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-664 | JT files used LZMA compression are not supported. | Enhancement |
|THREEDNET-502 | Improve OAP query, add support for Material/AssetInfo/Transform | Enhancement |
|THREEDNET-668 | Exception on loading DXF file | Bug |
|THREEDNET-669 | Export repaired mesh to OBJ will fail | Bug |
|THREEDNET-670 | Node.GetBoundingBox() wrong value. | Bug |
|THREEDJAVA-73 | Exception on converting 3D file to PNG | Bug |
{{< /table >}}

## Public API and Backwards Incompatible Changes

*   Changed the signature of SelectSingleObject/SelectObjects from **Aspose.ThreeD.Node**

{{< code lang="cs" >}}
//public Aspose.ThreeD.A3DObject SelectSingleObject(string path)
public object SelectSingleObject(string path)

//public System.Collections.Generic.List<Aspose.ThreeD.A3DObject> SelectObjects(string path)
public System.Collections.Generic.List<object> SelectObjects(string path)
{{< /code >}}

**Sample Code**

{{< code lang="cs" >}}
var scene = new Scene(new Torus());
foreach (BoundingBox bbox in scene.RootNode.SelectObjects("//<BoundingBox>"))
{
     Console.WriteLine($"Found a bbox : {bbox}");
}
{{< /code >}}

This is introduced by THREEDNET-502 which can query deeper objects like Material/Texture/AssetInfo/Transform/VertexElements.

*   Fixed a typo in **Aspose.ThreeD.Profiles.HShape**

{{< code lang="cs" >}}
//Old property:
//public double OveralDepth{ get;set;}
  
//New property
public double OverallDepth{ get;set;} 
{{< /code >}}

