---
title : "Manipulate custom properties of a 3D Scene" 
description : "" 
weight : 12046 
toc : false
type: docs
url: /net/developerguide/3dobjects/manipulate+custom+properties+of+a+3d+scene/
---

# Aspose.3D for .NET : Manipulate custom properties of a 3D Scene


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Add, Retrieve and Remove custom properties of a 3D Object](#add,-retrieve-and-remove-custom-properties-of-a-3d-object)
{{< /panel >}}
 

 

## Add, Retrieve and Remove custom properties of a 3D Object

Developers can Add, retrieve, and remove custom properties of 3D objects. RemoveProperty, GetProperty, SetProperty members of 3D objects are a set of short-handed methods to manipulate customized properties of the object. This is the code example to set, retrieve and remove a custom property:

**C#**

{{< code lang="c#" >}}
// initialize a scene 
Scene scene = new Scene();
// create a Box instance
var box = scene.RootNode.CreateChildNode("box", new Box());
// add custom property
box.SetProperty("property-name", "property-value");
box.SetProperty("property-name2", "property-value2");
// get a custom property by name
Property property = (Property)box.GetProperty("property-name");
// remove the custom property by name or property instance
box.RemoveProperty("property-name");
box.RemoveProperty(property);
// save 3D scene
scene.Save("test.fbx", FileFormat.FBX7400ASCII);
scene.Save("test.gltf", new GLTFSaveOptions(FileFormat.GLTF){SaveExtras = true});
scene.Save("test-2.gltf", new GLTFSaveOptions(FileFormat.GLTF2){SaveExtras = true});
{{< /code >}}

In order to save custom properties into the GLTF models, you need to set SaveExtras to true. The default value of SaveExtras property is false.

