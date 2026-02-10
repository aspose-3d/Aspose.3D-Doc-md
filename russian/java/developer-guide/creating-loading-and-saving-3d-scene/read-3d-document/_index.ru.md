---
title: Прочитать документ 3D
type: docs
weight: 30
url: /ru/java/read-3d-document/
description: Aspose.3D for Java API поддерживает чтение различных типов документов 3D.
---
##  **Список поддерживаемых форматов 3D (импорт)**
Aspose.3D for Java API поддерживает чтение различных типов документов 3D. Доступные конструкторы класса `Scene` помогают это сделать, и они принимают правильную строку пути к файлу. Поддерживаемые форматы файлов для чтения являются следующими:

1. FBX 7,5 (ASCII, двоичный)
1. FBX 7,4 (ASCII, двоичный)
1. FBX 7,3 (ASCII, двоичный)
1. FBX 7,2 (ASCII, двоичный)
1. STL (ASCII, двоичный)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, двоичный)
1. X (ASCII, двоичный)
1. Draco
1. 3MF
1. RVM (Текстовый, двоичный)
1. ASE

Конструкторы класса Scene определяют внутренний формат документа 3D.
##  **Импортировать документ 3D**
Aspose.3D for Java API поддерживает импорт различных типов документов 3D для изменения, добавления и обработки.
###  **Чтение сцены 3D: Примеры программирования**
{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.open(MyDir + "document.fbx");
{{< /highlight >}}
##  **Работа со свойствами 3D**
Aspose.3D API позволяет читать свойства сцены 3D, используя дочерние узлы сцены. Следующий пример кода демонстрирует использование этой функции.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
String dataDir = RunExamples.getDataDir();
Scene scene = new Scene(dataDir+ "EmbeddedTexture.fbx");
Material material = scene.getRootNode().getChildNodes().get(0).getMaterial();
PropertyCollection props = material.getProperties();
//List all properties using for loop
for (Property prop:props)
{
    System.out.println("Name" + prop.getName() + " Value = " + prop.getValue());
}
//or using ordinal for loop
for (int i = 0; i < props.size(); i++)
{
    Property prop = props.get(i);
    System.out.println("Name" + prop.getName() + " Value = " + prop.getValue());
}
//Get property value by name
Object diffuse = (Vector3)props.get("Diffuse");
System.out.println(diffuse);
//modify property value by name
props.set("Diffuse", new Vector3(1, 0, 1));
//Get property instance by name
Property pdiffuse = props.findProperty("Diffuse");
System.out.println(pdiffuse);
//Since Property is also inherited from A3DObject
//It's possible to get the property of the property
System.out.println("Property flags = " + pdiffuse.getProperty("flags"));
//and some properties that only defined in FBX file:
System.out.println("Label = " + pdiffuse.getProperty("label"));
System.out.println("Type Name = " + pdiffuse.getProperty("typeName"));
//so traversal on property's property is possible
for (Property pp: pdiffuse.getProperties())
{
	System.out.println("Diffuse. " + pp.getName() + " = " + pp.getValue());
}

{{< /highlight >}}


