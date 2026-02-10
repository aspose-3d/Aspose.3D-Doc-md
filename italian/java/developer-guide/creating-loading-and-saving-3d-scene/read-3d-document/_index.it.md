---
title: Leggi il documento 3D
type: docs
weight: 30
url: /it/java/read-3d-document/
description: Aspose.3D for Java API supporta la lettura di vari tipi di documenti 3D.
---
##  **Elenco dei formati supportati da 3D (importazione)**
Aspose.3D for Java API supporta la lettura di vari tipi di documenti 3D. I costruttori disponibili della classe `Scene` aiutano a farlo e accettano una stringa di percorso file valida. I formati di file leggibili supportati sono i seguenti:

1. FBX 7.5 (ASCII, binario)
1. FBX 7.4 (ASCII, binario)
1. FBX 7.3 (ASCII, binario)
1. FBX 7.2 (ASCII, binario)
1. STL (ASCII, binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, binario)
1. X (ASCII, binario)
1. Draco
1. 3MF
1. RVM (testo, binario)
1. ASE

I costruttori della classe Scene rilevano internamente il formato del documento 3D.
##  **Importa 3D documento**
Aspose.3D for Java API supporta l'importazione di vari tipi di documenti 3D per la modifica, l'aggiunta e l'elaborazione.
###  **Lettura di una scena da 3D: campioni di programmazione**
{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.open(MyDir + "document.fbx");
{{< /highlight >}}
##  **Lavorare con 3D proprietà**
Aspose.3D API ti consente di leggere 3D proprietà della scena utilizzando i nodi figlio della scena. Il seguente esempio di codice dimostra l'utilizzo di questa funzionalità.

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


