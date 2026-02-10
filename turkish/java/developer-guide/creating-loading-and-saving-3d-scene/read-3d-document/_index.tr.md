---
title: 3D belgesini oku
type: docs
weight: 30
url: /tr/java/read-3d-document/
description: Aspose.3D for Java API 3D belgelerinin çeşitli türlerini okuma desteğine sahiptir.
---
##  **3D desteklenen formatların listesi (içe aktarma)**
Aspose.3D for Java API has support of reading various type of 3D documents. The available constructors of the `Scene` class helps to do so and they accept a valid file path string. The supported readable file formats are as follows:

1. FBX 7.5 (ascii, ikili)
1. FBX 7.4 (ascii, ikili)
1. FBX 7.3 (ascii, İkili)
1. FBX 7.2 (ascii, ikili)
1. STL (ascii, ikili)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ascii, ikili)
1. X (ASCI I, Binary)
1. Draco
1. 3MF
1. RVM (metin, ikili)
1. ASE

The constructors of Scene class detect 3D document format internally.
##  **İthalat 3D belge**
Aspose.3D for Java API değişiklik, ekleme ve işleme amaçları için 3D belgesinin çeşitli türlerini ithal etme desteğine sahiptir.
###  **3D sahne okuma: programlama örnekleri**
{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.open(MyDir + "document.fbx");
{{< /highlight >}}
##  **Working with 3D Properties**
Aspose.3D API, sahnenin çocuk düğümlerini kullanarak 3D sahne özelliklerini okumanızı sağlar. Aşağıdaki kod örneği bu özelliğin kullanımını gösterir.

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


