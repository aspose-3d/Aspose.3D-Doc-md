---
title: 3D sahnesinin özel özelliklerini işlemek
type: docs
weight: 80
url: /tr/net/manipulate-custom-properties-of-a-3d-scene/
description: Developers can Add, retrieve, and remove custom properties of 3D objects. RemoveProperty, GetProperty, SetProperty members of 3D objects are a set of short-handed methods to manipulate customized properties of the object.
---
##  **3D nesnesinin özel özelliklerini ekleyin, alın ve kaldırın**
Developers can Add, retrieve, and remove custom properties of 3D objects. `RemoveProperty`, `GetProperty`, `SetProperty` members of 3D objects are a set of short-handed methods to manipulate customized properties of the object. This is the code example to set, retrieve and remove a custom property:

**C#**

{{< highlight "java" >}}

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

{{< /highlight >}}

{{% alert color="primary" %}} 

In order to save custom properties into the GLTF models, you need to set SaveExtras to true. The default value of SaveExtras property is false.

{{% /alert %}}
