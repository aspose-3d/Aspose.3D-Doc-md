---
title: Манипулировать пользовательскими свойствами сцены 3D
type: docs
weight: 80
url: /ru/net/manipulate-custom-properties-of-a-3d-scene/
description: Разработчики могут добавлять, извлекать и удалять пользовательские свойства объектов 3D. RemoveProperty, GetProperty, SetProperty членов объектов 3D-это набор методов с короткими ручками для управления настраиваемыми свойствами объекта.
---
## **Добавление, извлечение и удаление пользовательских свойств объекта 3D**
Разработчики могут добавлять, извлекать и удалять пользовательские свойства объектов 3D. `RemoveProperty`, `GetProperty`, `SetProperty`, `SetProperty` члены объектов 3D представляют собой набор краткосрочных методов для управления настраиваемыми свойствами объекта. Это пример кода для установки, извлечения и удаления пользовательского свойства:

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

Чтобы сохранить пользовательские свойства в модели GLTF, вам нужно установить SaveExtras в true. Значение по умолчанию свойства SaveExtras является false.

{{% /alert %}}
