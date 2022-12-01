---
title: Spécifiez 3D Options de sauvegarde de fichier dans C#
linktitle: Spécifiez 3D Options de sauvegarde de fichier
type: docs
weight: 40
url: /fr/net/specify-3d-file-save-options/
description: Il existe plusieurs surcharges de méthode Scene.Save qui acceptent un objet SaveOptions. Chaque format de sauvegarde a une classe correspondante qui contient des options de sauvegarde pour ce format de sauvegarde.
---
## **Aperçu**

Cet article explique comment vous pouvez enregistrer les fichiers 3D dans différents formats[Après les avoir chargés dans l'objet Scène](https://docs.aspose.com/3d/net/specify-3d-file-load-options/)En utilisant C#. En chargeant et en enregistrant, vous pouvez effectuer un nombre de conversions différentes, par ex.

- Convertissez FBX en X C#
- Convertissez GLTF en OBJ
- Convertissez OBJ en X C#
- Convertissez STL en OBJ
- Convertissez RVM en 3DS

## **3D Options de sauvegarde de fichier**
Il existe plusieurs surcharges de méthode [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) qui acceptent un objet SaveOptions. Cela devrait être un objet d'une classe dérivée de la classe `SaveOptions`. Chaque format de sauvegarde a une classe correspondante qui contient des options de sauvegarde pour ce format de sauvegarde, par exemple, il y a `ColladaSaveOptions` pour le format de sauvegarde `FileFormat.Collada`.
### **Utilisation des options de sauvegarde Collada**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Collada.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
### **Utilisation des options de sauvegarde Discreet3DS**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
### **Utilisation des options de sauvegarde FBX**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format FBX.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` expose également la propriété `EnableCompression` qui peut être utilisée pour compresser de grandes données binaires dans le fichier FBX. La valeur par défaut de cette propriété est vraie. Ci-dessous code extrait explique comment vous pouvez travailler avec cette propriété tout en enregistrant une scène.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
### **Utilisation des options Obj Save**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Obj.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
### **Utilisation des options de sauvegarde STL**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
### **Utilisation des options de sauvegarde U3D**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un document au format U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
### **Utilisation des options de sauvegarde glTF**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 



Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un document au format glTF.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
### **PrettyPrint dans glTF Enregistrer les options**
Vous pouvez également utiliser la propriété PrettyPrint de la classe GLTFSaveOptions pour une impression JSON compréhensible par l'homme. Le code ci-dessous montre comment utiliser cette fonctionnalité.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
### **Enregistrer les dépendances d'une scène 3D dans le système de fichiers réels**
Les développeurs peuvent exiger d'enregistrer toutes les dépendances de scène 3D dans le système de fichiers réel. Ils peuvent définir le chemin d'un répertoire local, enregistrer dans l'objet `MemoryFileSystem` ou simplement supprimer les dépendances. La propriété `FileSystem` est ajoutée dans toutes les classes d'options de sauvegarde.
#### **Jeter l'enregistrement des fichiers matériels**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
#### **Sauvegardez les dépendances dans le répertoire local**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
#### **Sauvegardez les dépendances dans l'objet MemoryFileSystem**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
### **Utilisation des options de sauvegarde Google Draco (.drc)**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un modèle 3D au format DRC.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
### **Utilisation des options de sauvegarde RVM**
Le code C# ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un modèle 3D au format RVM.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
