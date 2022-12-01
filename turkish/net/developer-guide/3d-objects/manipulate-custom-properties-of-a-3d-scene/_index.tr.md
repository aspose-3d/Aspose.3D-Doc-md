---
title: Bir 3D cene cene MManipulate özel özellikleri
type: docs
weight: 80
url: /tr/net/manipulate-custom-properties-of-a-3d-scene/
description: Developers, 3D nesnelerinin özel özelliklerini alabilir, alabilir ve kaldırabilir. RemoveProperty, Get. roperty, Set. roperty üyeleri 3D nesneleri, nesnenin özelleştirilmiş özelliklerini işlemek için kısa teslim yöntemlerden oluşan bir kümedir.
---
## **Add, Retrieve ve Remove 3D Object özel özellikleri**
Developers, 3D nesnelerinin özel özelliklerini alabilir, alabilir ve kaldırabilir. `RemoveProperty`, `GetProperty`, `SetProperty` 076. 481 nesnelerinin üyeleri, nesnenin özelleştirilmiş özelliklerini işlemek için bir dizi kısa teslim yöntemidir. This, özel bir özelliği ayarlamak, almak ve kaldırmak için kod örneğidir:

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

In özel özellikleri GLTF modellerine kaydetmek için, SaveExtras doğru ayarlamanız gerekir. So SaveExtras özelliğinin varsayılan değeri yanlıştır.

{{% /alert %}}
