---
title: Lire le document 3D
type: docs
weight: 30
url: /fr/java/read-3d-document/
description: Aspose.3D for Java API supporte la lecture de divers types de documents 3D.
---
##  **Liste des formats supportés par 3D (import)**
Aspose.3D for Java API supporte la lecture de divers types de documents 3D. Les constructeurs disponibles de la classe `Scene` aident à le faire et ils acceptent une chaîne de chemin de fichier valide. Les formats de fichiers lisibles pris en charge sont les suivants:

1. FBX 7.5 (ASCII, binaire)
1. FBX 7.4 (ASCII, binaire)
1. FBX 7.3 (ASCII, binaire)
1. FBX 7.2 (ASCII, binaire)
1. STL (ASCII, binaire)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, binaire)
1. X (ASCII, binaire)
1. Draco
1. 3MF
1. RVM (Texte, Binaire)
1. ASE

Les constructeurs de la classe Scene détectent le format de document 3D en interne.
##  **Importer un document 3D**
Aspose.3D for Java API supporte l'importation de divers types de documents 3D à des fins de modification, d'ajout et de traitement.
###  **Lecture d'une scène 3D: Échantillons de programmation**
{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.open(MyDir + "document.fbx");
{{< /highlight >}}
##  **Travailler avec les propriétés 3D**
Aspose.3D API vous permet de lire les propriétés de scène 3D en utilisant les nœuds enfants de la scène. L'exemple de code suivant illustre l'utilisation de cette fonctionnalité.

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


