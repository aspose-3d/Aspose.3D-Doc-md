---
title: Leer el documento 3D
type: docs
weight: 30
url: /es/java/read-3d-document/
description: Aspose.3D for Java API tiene soporte para leer varios tipos de documentos 3D.
---
##  **Lista de formatos soportados por 3D (importación)**
Aspose.3D for Java API tiene soporte para leer varios tipos de documentos 3D. Los constructores disponibles de la clase `Scene` ayudan a hacerlo y aceptan una cadena de ruta de archivo válida. Los formatos de archivo legibles admitidos son los siguientes:

1. FBX 7,5 (ASCII, binario)
1. FBX 7,4 (ASCII, binario)
1. FBX 7,3 (ASCII, binario)
1. FBX 7,2 (ASCII, binario)
1. STL (ASCII, binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, binario)
1. X (ASCII... Binary)
1. Draco
1. 3MF
1. RVM (Texto, binario)
1. ASE

Los constructores de la clase Scene detectan el formato de documento 3D internamente.
##  **Importar documento 3D**
Aspose.3D for Java API tiene soporte para importar varios tipos de documentos 3D para fines de modificación, adición y procesamiento.
###  **Lectura de una escena 3D: Muestras de programación**
{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.open(MyDir + "document.fbx");
{{< /highlight >}}
##  **Trabajar con propiedades 3D**
Aspose.3D API le permite leer las propiedades de la escena 3D utilizando los nodos secundarios de la escena. El siguiente ejemplo de código muestra el uso de esta característica.

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


