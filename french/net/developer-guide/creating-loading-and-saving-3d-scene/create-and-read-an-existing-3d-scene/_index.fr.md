---
title: Créer et lire une scène 3D existante
type: docs
weight: 10
url: /fr/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API prend en charge la création des nouvelles scènes 3D à partir de zéro, puis les sauvegarde dans n'importe quel format de fichier pris en charge. Les développeurs peuvent également charger une scène 3D existante à des fins de modification, d'ajout ou de traitement.
---
##  **Aperçu**
L'article explique les sujets suivants en utilisant la bibliothèque de manipulation des formats de fichiers C# 3D.
- Créer une scène vide 3D dans C# à partir de zéro
- Lire ou charger la scène 3D existante dans C#
- Enregistrez la scène 3D dans les formats 3D pris en charge à l'aide de C#
- Travailler avec 3D Propriétés de la scène dans C#

##  **Créez une scène 3D vide et enregistrez dans les formats de fichier 3D pris en charge**
Aspose.3D API prend en charge la création des nouvelles scènes 3D à partir de zéro, puis les sauvegarde dans n'importe quel format de fichier pris en charge. Les développeurs peuvent également charger une scène 3D existante à des fins de modification, d'ajout ou de traitement.

###  **Création d'un document de scène 3D**
Veuillez suivre ces étapes dans C# pour créer un document scène 3D en utilisant les API Aspose.3D:

1. Créez une instance de la classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) qui représente un document de scène 3D.
1. Générez un document de scène 3D en appelant la méthode [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) de l'objet de classe Scene.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

##  **Lecture d'une scène 3D**
En utilisant Aspose.3D API, les développeurs peuvent charger tous les documents 3D pris en charge. Les constructeurs disponibles de la classe `Scene` le permettent et ils acceptent une chaîne de chemin de fichier valide. Les formats de fichiers lisibles pris en charge sont les suivants:

1. FBX 7.5 (ASCII, binaire)
1. FBX 7.4 (ASCII, binaire)
1. FBX 7.3 (ASCII, binaire)
1. FBX 7.2 (ASCII, binaire)
1. FBX 6.1 (ASCII, binaire)
1. STL (ASCII, binaire)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII, binaire)
1. Maya (ASCII, binaire)
1. OpenUSD (USD, USDZ)
1. Mixeur
1. DXF
1. PLY (ASCII, binaire)
1. X (ASCII, binaire)
1. Draco
1. 3MF
1. RVM (Texte, Binaire)
1. ASE

Les constructeurs de la classe `Scene` détectent le format de document 3D en interne.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.

// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.Open("document.fbx");


{{< /highlight >}}

##  **Travailler avec 3D Propriétés de scène**
Aspose.3D API vous permet de lire les propriétés de scène 3D en utilisant les nœuds enfants de la scène. L'exemple de code C# suivant illustre l'utilisation de cette fonctionnalité.

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
