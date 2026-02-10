---
title: Создание и чтение существующей сцены 3D
type: docs
weight: 10
url: /ru/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API поддерживает создание новых 3D сцен с нуля, а затем сохранение в любом поддерживаемом формате файла. Разработчики также могут загрузить существующую сцену 3D для модификации, добавления или обработки.
---
##  **Обзор**
В статье рассматриваются следующие темы с использованием библиотеки манипулирования форматами файлов C# 3D.
- Создайте пустую сцену 3D в C# с нуля
- Чтение или загрузка существующей сцены 3D в C#
- Сохраните сцену 3D в поддерживаемых форматах 3D, используя C#
- Работа со свойствами сцены 3D в C#

##  **Создайте пустую сцену 3D и сохраните в поддерживаемых форматах файлов 3D**
Aspose.3D API поддерживает создание новых 3D сцен с нуля, а затем сохранение в любом поддерживаемом формате файла. Разработчики также могут загрузить существующую сцену 3D для модификации, добавления или обработки.

###  **Создание документа сцены 3D**
Пожалуйста, выполните следующие действия в C#, чтобы создать документ сцены 3D, используя API Aspose.3D:

1. Создайте экземпляр класса [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), представляющий документ сцены 3D.
1. Сгенерируйте документ сцены 3D, вызвав метод [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) объекта класса Scene.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

##  **Чтение сцены 3D**
Используя Aspose.3D API, разработчики могут загрузить все поддерживаемые документы 3D. Доступные конструкторы класса `Scene` позволяют это сделать, и они принимают правильную строку пути к файлу. Поддерживаемые форматы файлов для чтения являются следующими:

1. FBX 7,5 (ASCII, двоичный)
1. FBX 7,4 (ASCII, двоичный)
1. FBX 7,3 (ASCII, двоичный)
1. FBX 7,2 (ASCII, двоичный)
1. FBX 6,1 (ASCII, двоичный)
1. STL (ASCII, двоичный)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII, двоичный)
1. Майя (ASCII, двоичный)
1. OpenUSD (USD, USDZ)
1. Блендер
1. DXF
1. PLY (ASCII, двоичный)
1. X (ASCII, двоичный)
1. Draco
1. 3MF
1. RVM (Текстовый, двоичный)
1. ASE

Конструкторы класса `Scene` внутренне определяют формат документа 3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.

// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.Open("document.fbx");


{{< /highlight >}}

##  **Работа со свойствами сцены 3D**
Aspose.3D API позволяет читать свойства сцены 3D, используя дочерние узлы сцены. Следующий пример кода C# демонстрирует использование этой функции.

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
