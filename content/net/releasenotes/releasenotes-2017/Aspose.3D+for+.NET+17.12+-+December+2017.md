+++
title = "Aspose.3D for .NET 17.12 - December 2017" 
description = "" 
weight = 12127 
+++

Aspose.3D for .NET : Aspose.3D for .NET 17.12 - December 2017  

# Aspose.3D for .NET : Aspose.3D for .NET 17.12 - December 2017


This page contains release notes for [Aspose.3D for .NET 17.12](https://www.nuget.org/packages/Aspose.3D/17.12.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-304|Add support of exporting RVM (AVEVA PDMS)|New feature|
|THREEDNET-312|Add shorthand way to scale geometries|Improvement|
|THREEDNET-314|Add support of exporting custom property/ID to nodes in GLTF format|Improvement|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

#### Adds SaveExtras property to Aspose.ThreeD.Formats.GLTFSaveOptions class

The default value of SaveExtras property is false, if you want Aspose.3D for .NET API to export customized properties of the object, you can assign it to true.

**C#**

public bool SaveExtras{ get;set;}

The customized properties will be saved into an 'extra' field due to the glTF's specification. A code example is narrated below.

#### Adds three members to Aspose.ThreeD.A3DObject class

RemoveProperty, GetProperty, SetProperty are a set of short-handed methods to manipulate customized properties of the object. The old methods like FindProperty and CreateDynamicProperty are too verbose, and planned to be removed in the future. The customized properties are supported by FBX/glTF (All versions).

**C#**

public bool RemoveProperty(string property)public object GetProperty(string property)public void SetProperty(string property, object value)

**Sample code:**

**C#**

Scene scene = new Scene();var box = scene.RootNode.CreateChildNode("box", new Box());box.SetProperty("obj-id", "box-id");scene.Save("test.fbx", FileFormat.FBX7400ASCII);scene.Save("test.gltf", new GLTFSaveOptions(FileFormat.GLTF){SaveExtras = true});scene.Save("test-2.gltf", new GLTFSaveOptions(FileFormat.GLTF2){SaveExtras = true});

This sample code will save the scene with the customized properties into FBX, glTF and glTF 2.0.

#### Adds two members to Aspose.ThreeD.Entities.PolygonModifier class

These members are handy, if developers do not want to change the node's transform but want to scale the geometries and only applicable to geometries.

**C#**

public static void Scale(Aspose.ThreeD.Scene scene, Aspose.ThreeD.Utilities.Vector3 scale)public static void Scale(Aspose.ThreeD.Node node, Aspose.ThreeD.Utilities.Vector3 scale)

**Sample code:**

**C#**

// scale the model in huge-scene.obj by 0.01 and save it to another file:Scene scene = new Scene("huge-scene.obj");PolygonModifier.Scale(scene, new Vector3(0.01));scene.Save("scaled-scene.obj", FileFormat.WavefrontOBJ);

#### Adds FindNode method to Aspose.ThreeD.Node class

This is a handy method to find a child node by the name, it will return null if could not find a node.

**C#**

Scene scene = new Scene();scene.RootNode.CreateChildNode("child", new Box());Node child = scene.RootNode.FindNode("child");

#### Usage Examples

Please check the list of help topics added or updated in the Aspose.3D Wiki docs:

1.  [Manipulate custom properties of a 3D Scene](https://docs2.aspose.com/3d/net/developerguide/3dobjects/manipulate+custom+properties+of+a+3d+scene)
2.  [Scale geometries of a 3D Scene](https://docs2.aspose.com/3d/net/developerguide/geometry/scale+geometries+of+a+3d+scene)

