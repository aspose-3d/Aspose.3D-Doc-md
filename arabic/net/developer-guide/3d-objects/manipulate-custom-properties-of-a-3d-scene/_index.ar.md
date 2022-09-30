---
title: Mخصائص مخصصة من 3D cenسين
type: docs
weight: 80
url: /ar/net/manipulate-custom-properties-of-a-3d-scene/
description: Dإيفلين يمكن أن Add ، واسترداد ، وإزالة خصائص مخصصة من 3D الكائنات. RemoveProperty ، GetProperty ، أعضاء etProperty من 3D الكائنات هي مجموعة من طرق قصيرة اليد لمعالجة خصائص مخصصة للكائن.
---
## **Add ، Retrieve و ememove خصائص مخصصة من 3D O**
Dإيفلين يمكن أن Add ، واسترداد ، وإزالة خصائص مخصصة من 3D الكائنات. `RemoveProperty`, `GetProperty`, `SetProperty` أعضاء 3D الكائنات هي مجموعة من أساليب قصيرة اليد لمعالجة خصائص مخصصة للكائن. Tهو مثال التعليمات البرمجية لتعيين واسترداد وإزالة خاصية مخصصة:

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

In الطلب لحفظ خصائص مخصصة في نماذج GLTF ، تحتاج إلى تعيين SaveExtras إلى true. Tانه القيمة الافتراضية property aveExtras الملكية كاذبة.

{{% /alert %}}
