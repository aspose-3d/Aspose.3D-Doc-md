---
title: Lesen Sie das Dokument 3D
type: docs
weight: 30
url: /de/java/read-3d-document/
description: Aspose.3D for Java API hat Unterstützung beim Lesen verschiedener Arten von 3D Dokumenten.
---
##  **Liste der von 3D unterstützten Formate (Import)**
Aspose.3D for Java API hat Unterstützung beim Lesen verschiedener Arten von 3D Dokumenten. Die verfügbaren Konstruktoren der `Scene`-Klasse helfen dabei und akzeptieren eine gültige Datei pfad zeichenfolge. Die unterstützten lesbaren Dateiformate lauten wie folgt:

1. FBX 7.5 (ASCII, Binär)
1. FBX 7.4 (ASCII, Binär)
1. FBX 7.3 (ASCII, Binär)
1. FBX 7.2 (ASCII, Binär)
1. STL (ASCII, Binär)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binär)
1. X (ASCII, Binär)
1. Draco
1. 3MF
1. RVM (Text, Binär)
1. ASE

Die Konstruktoren der Scene-Klasse erkennen das Dokument format 3D intern.
##  **3D-Dokument importieren**
Aspose.3D for Java API unterstützt den Import verschiedener Arten von 3D Dokumenten für die Modifikation, Ergänzung und Verarbeitung.
###  **Lesen einer 3D-Szene: Samples programmieren**
{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.open(MyDir + "document.fbx");
{{< /highlight >}}
##  **Arbeiten mit 3D Eigenschaften**
Aspose.3D API ermöglicht es Ihnen, die Szene eigenschaften von 3D mithilfe der unter geordneten Knoten der Szene zu lesen. Das folgende Code beispiel zeigt die Verwendung dieser Funktion.

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


