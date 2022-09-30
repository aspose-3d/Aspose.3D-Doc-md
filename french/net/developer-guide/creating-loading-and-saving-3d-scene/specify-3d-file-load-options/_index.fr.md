---
title: Spécifiez les options de charge de fichier 3D dans C#
linktitle: Spécifiez les options de charge de fichier 3D
type: docs
weight: 30
url: /fr/net/specify-3d-file-load-options/
description: Il existe plusieurs surcharges de méthode Scene.Open ou surcharges de constructeur de classe Scène qui acceptent un objet LoadOptions. Chaque format de charge a une classe correspondante qui contient les options de charge pour ce format de charge.
---
## **Aperçu**

Cet article explique comment vous pouvez charger différents types de fichiers 3D en utilisant leurs classes d'option de charge respectives dans C# à l'intérieur de l'objet Scène, puis vous pouvez[Sauvegardez-le dans différents formats de fichiers supportés par 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). En chargeant et en enregistrant, vous pouvez effectuer un nombre de conversions différentes, par ex.

- Convertissez FBX en OBJ
- Convertissez 3DS en FBX
- Convertissez U3D en OBJ
- Convertissez OBJ en 3DS
- Convertir X en 3DS en C#

## **3D Options de charge de fichier**
Il existe plusieurs surcharges de méthode [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) ou surcharges de constructeur de classe Scène qui acceptent un objet `LoadOptions`. Cela devrait être un objet d'une classe dérivée de la classe `LoadOptions`. Chaque format de charge a une classe correspondante qui contient des options de charge pour ce format de charge, par exemple il y a `ColladaSaveOptions` pour le format de sauvegarde `FileFormat.Collada`.
### **Utilisation des options de charge Discret 3DS**
Le code C# ci-dessous montre comment définir les options de charge avant de charger un fichier Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
### **Utilisation des options de charge Obj**
Le code C# ci-dessous montre comment définir les options de charge avant de charger un fichier Obj 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
### **Utilisation des options de charge STL**
Le code C# ci-dessous montre comment définir les options de charge avant de charger un fichier STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
### **Utilisation des options de charge U3D**
Le code C# ci-dessous montre comment définir les options de charge avant de charger un fichier U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
### **Utilisation des options de charge glTF**
Le code C# ci-dessous montre comment définir les options de charge avant de charger un fichier glTF.
#### **Retournez la coordination de la texture V/T**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
### **Utilisation des options de charge Ply**
Le code C# ci-dessous montre comment définir les options de charge avant de charger un modèle PLY.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
### **Utilisation des options de charge X DirectX**
Le code C# ci-dessous montre comment définir les options de charge avant de charger un fichier DirectX X.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
### **Utilisez les options de charge RVM**
**C#**

{{< highlight "java" >}}

 // set load options of RVM

Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

// import RVM

scene.Open("LAD-TOP.rvm", opt);

// save in the OBJ format

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
### **Utilisation des options de charge FBX**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
