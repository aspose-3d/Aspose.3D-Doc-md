---
title: Spécifiez les options de sauvegarde de fichier 3D
type: docs
weight: 40
url: /fr/python-net/specify-3d-file-save-options/
description: Il existe plusieurs surcharges de méthode Scene.Save qui acceptent un objet SaveOptions. Chaque format de sauvegarde a une classe correspondante qui contient des options de sauvegarde pour ce format de sauvegarde.
---
##  **3D Options de sauvegarde des fichiers**
Il existe plusieurs surcharges de méthode [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) qui acceptent un objet `SaveOptions`. Cela devrait être un objet d'une classe dérivée de la classe `SaveOptions`. Chaque format de sauvegarde a une classe correspondante qui contient des options de sauvegarde pour ce format de sauvegarde, par exemple, il y a `ColladaSaveOptions` pour le format de sauvegarde `FileFormat.Collada`.
###  **Utilisation des options de sauvegarde Collada**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Collada.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
###  **Utilisation des options de sauvegarde Discreet3DS**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D dans un format Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
###  **Utilisation des options de sauvegarde FBX**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D dans un format FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` expose également la propriété `enable_compression` qui peut être utilisée pour compresser de grandes données binaires dans le fichier FBX. La valeur par défaut de cette propriété est true. L'extrait de code ci-dessous explique comment vous pouvez travailler avec cette propriété tout en enregistrant une scène.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
###  **Utilisation des options Obj Save**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Obj.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
###  **Utilisation des options de sauvegarde STL**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
###  **Utilisation des options de sauvegarde U3D**
Le code ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un document au format U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
###  **Utilisation des options de sauvegarde glTF**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 



Le code ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un document au format glTF.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
###  **PrettyPrint in glTF Options de sauvegarde**
Vous pouvez également utiliser la propriété PrettyPrint de la classe GLTFSaveOptions pour une impression JSON compréhensible par l'homme. Le code ci-dessous montre comment utiliser cette fonctionnalité.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
###  **Enregistrer les dépendances d'une scène 3D dans le système de fichiers réel**
Les développeurs peuvent avoir besoin d'enregistrer toutes les dépendances de scène 3D dans le système de fichiers réel. Ils peuvent définir le chemin d'un répertoire local, enregistrer dans l'objet MemoryFileSystem ou simplement jeter les dépendances. La propriété FileSystem est ajoutée dans toutes les classes d'option de sauvegarde.
####  **Jeter l'enregistrement des fichiers matériels**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
####  **Sauvegardez les dépendances dans le répertoire local**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
####  **Sauvegardez les dépendances dans l'objet MemoryFileSystem**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
###  **Utilisation des options de sauvegarde Google Draco (.drc)**
Le code ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un modèle 3D au format DRC.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
###  **Utilisation des options de sauvegarde RVM**
Le code ci-dessous montre comment définir les options de sauvegarde avant de sauvegarder un modèle 3D au format RVM.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
