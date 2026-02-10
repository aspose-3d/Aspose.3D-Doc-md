---
title: Read 3D document
type: docs
weight: 30
url: /sv/java/read-3d-document/
description: Aspose.3D for Java API har stöd för att läsa olika typer av 3D dokument.
---
##  **Lista över format som stöds 3D (import)**
Aspose.3D for Java API har stöd för att läsa olika typer av 3D dokument. Tillgängliga konstruktörer i klassen `Scene` hjälper till att göra det och de accepterar en giltig filsökvägssträng. De läsbara filformat som stöds är följande:

1. FBX 7.5 (ASCII, Binära)
1. FBX 7.4 (ASCII, Binära)
1. FBX 7.3 (ASCII, Binära)
1. FBX 7.2 (ASCII, Binära)
1. STL (ASCII, binär)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, binär)
1. X (ASCII, binära)
1. Draco
1. 3MF
1. RVM (Text, binärt)
1. ASE

Konstruktörerna av Scene klass detekterar dokumentformatet 3D internt.
##  **Importera 3D dokument**
Aspose. 3D for Java API har stöd för att importera olika typer av 3D dokument för ändring, tillägg och bearbetning.
###  **Läs en 3D Scene: Programmeringsprovning**
{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.open(MyDir + "document.fbx");
{{< /highlight >}}
##  **Arbetar med 3D Egenskaper**
Aspose.3D API låter dig läsa 3D Scenegenskaper med hjälp av scenens barnnoder. Följande kodprov visar hur denna funktion används.

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


