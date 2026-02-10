---
title: Mevcut bir 3D sahne oluşturun ve okuyun
type: docs
weight: 10
url: /tr/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API yeni 3D sahnelerini sıfırdan oluşturmayı ve ardından desteklenen herhangi bir dosya biçiminde kaydetmeyi destekler. Geliştiriciler ayrıca değişiklik, ekleme veya işleme amaçları için mevcut bir 3D sahne yükleyebilir.
---
##  **Overview**
The article explains the following topics using C# 3D file formats manipulation library.
- Sıfırdan C# içinde boş bir 3D sahne oluşturun
- Mevcut 3D sahnesini C# olarak okuyun veya yükleyin
- 3D sahnesini C# kullanarak desteklenen 3D formatlarında kaydedin
- Work with 3D Scene Properties in C#

##  **Boş bir 3D sahne oluşturun ve desteklenen 3D dosya formatlarında kaydedin**
Aspose.3D API yeni 3D sahnelerini sıfırdan oluşturmayı ve ardından desteklenen herhangi bir dosya biçiminde kaydetmeyi destekler. Geliştiriciler ayrıca değişiklik, ekleme veya işleme amaçları için mevcut bir 3D sahne yükleyebilir.

###  **3D sahne belgesi oluşturma**
Please follow these steps in C# to create a 3D Scene document using the Aspose.3D APIs:

1. 3D sahne belgesini temsil eden [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) sınıfının bir örneğini oluşturun.
1. Generate a 3D Scene document by calling the [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) method of the Scene class object.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

##  **3D sahnesini okumak**
Using Aspose.3D API, developers can load all the supported 3D documents. The available constructors of the `Scene` class allow to do so and they accept a valid file path string. The supported readable file formats are as follows:

1. FBX 7.5 (ascii, ikili)
1. FBX 7.4 (ascii, ikili)
1. FBX 7.3 (ascii, İkili)
1. FBX 7.2 (ascii, ikili)
1. FBX 6.1 (ascii, ikili)
1. STL (ascii, ikili)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ascii, ikili)
1. Maya (ascii, ikili)
1. Openusd (USD, USDZ)
1. Blender
1. DXF
1. PLY (ascii, ikili)
1. X (ASCI I, Binary)
1. Draco
1. 3MF
1. RVM (metin, ikili)
1. ASE

Constructors of the `Scene` class detect 3D document format internally.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.

// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.Open("document.fbx");


{{< /highlight >}}

##  **3D sahne özellikleri ile çalışmak**
Aspose.3D API, sahnenin çocuk düğümlerini kullanarak 3D sahne özelliklerini okumanızı sağlar. Aşağıdaki C# kod örneği bu özelliğin kullanımını gösterir.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Scene scene = Scene.FromFile("EmbeddedTexture.fbx");
Material material = scene.RootNode.ChildNodes[0].Material;
PropertyCollection props = material.Properties;
//List all properties using foreach
foreach (var prop in props)
{
    Console.WriteLine("{0} = {1}", prop.Name, prop.Value);
}
//or using ordinal for loop
for (int i = 0; i < props.Count; i++)
{
    var prop = props[i];
    Console.WriteLine("{0} = {1}", prop.Name, prop.Value);
}
//Get property value by name
var diffuse = props["Diffuse"];
Console.WriteLine(diffuse);
//modify property value by name
props["Diffuse"] = new Vector3(1, 0, 1);
//Get property instance by name
Property pdiffuse = props.FindProperty("Diffuse");
Console.WriteLine(pdiffuse);
//Since Property is also inherited from A3DObject
//It's possible to get the property of the property
Console.WriteLine("Property flags = {0}", pdiffuse.GetProperty("flags"));
//and some properties that only defined in FBX file:
Console.WriteLine("Label = {0}", pdiffuse.GetProperty("label"));
Console.WriteLine("Type Name = {0}", pdiffuse.GetProperty("typeName"));
//so traversal on property's property is possible
foreach (var pp in pdiffuse.Properties)
{
    Console.WriteLine("Diffuse.{0} = {1}", pp.Name, pp.Value);
}

{{< /highlight >}}
