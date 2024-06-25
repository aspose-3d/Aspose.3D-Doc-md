---
title: 操作 3D 场景的自定义属性
type: docs
weight: 80
url: /zh/net/manipulate-custom-properties-of-a-3d-scene/
description: 开发人员可以添加、检索和删除 3D 对象的自定义属性。3D 对象的RemoveProperty、GetProperty、SetProperty成员是一组用于操作对象的自定义属性的常用方法。
---
##  **添加、检索和删除 3D 对象的自定义属性**
开发人员可以添加、检索和删除 3D 对象的自定义属性。3D 对象的 `RemoveProperty` 、 `GetProperty` 、 `SetProperty` 成员是一组用于操作对象的自定义属性的常用方法。这是设置、检索和移除自定义属性的代码示例:

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

为了将自定义属性保存到 GLTF 模型中，您需要将SaveExtras设置为true。SaveExtras属性的默认值为false。

{{% /alert %}}
