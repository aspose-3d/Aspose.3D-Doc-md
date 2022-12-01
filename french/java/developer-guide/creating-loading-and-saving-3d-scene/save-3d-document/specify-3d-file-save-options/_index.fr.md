---
title: Spécifiez 3D Options de sauvegarde de fichier
type: docs
weight: 10
url: /fr/java/specify-3d-file-save-options/
description: Il existe plusieurs surcharges de méthode Scene.save qui acceptent une instance SaveOptions.
---
## **3D Options de sauvegarde de fichier**
Il existe plusieurs surcharges de méthode Scene.save qui acceptent une instance SaveOptions. Il doit s'agir d'une instance d'une classe dérivée de la classe SaveOptions. Chaque format de sauvegarde a une classe correspondante qui contient les options de sauvegarde pour ce format de sauvegarde, par exemple il existe ColladaSaveOptions pour le format de sauvegarde FileFormat.COLLADA.
### **Utilisation des options de sauvegarde Collada**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Collada.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
### **Utilisation des options de sauvegarde Discreet3DS**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
### **Utilisation des options de sauvegarde FBX**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format FBX.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
### **Utilisation des options de sauvegarde OBJ**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format Obj.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
### **Utilisation des options de sauvegarde STL**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un fichier 3D au format STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
### **Utilisation des options de sauvegarde U3D**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un document au format U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
### **Utilisation des options de sauvegarde glTF**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 



Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un document au format glTF.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
### **PrettyPrint dans glTF Enregistrer les options**
Vous pouvez également utiliser la méthode setPrettyPrint de la classe GLTFSaveOptions pour une impression JSON compréhensible par l'homme. Le code ci-dessous montre comment utiliser cette fonctionnalité.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
### **Enregistrer les dépendances d'une scène 3D dans le système de fichiers réels**
Les développeurs peuvent exiger d'enregistrer toutes les dépendances de la scène 3D dans le système de fichiers réel. Ils peuvent définir le chemin d'un répertoire local, enregistrer dans l'objet `MemoryFileSystem` ou simplement supprimer les dépendances. La propriété FileSystem est ajoutée dans toutes les classes d'options de sauvegarde.
#### **Jeter l'enregistrement des fichiers matériels**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
#### **Sauvegardez les dépendances dans le répertoire local**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
#### **Sauvegardez les dépendances dans l'instance MemoryFileSystem**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
### **Utilisation des options de sauvegarde Google Draco (.DRC)**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un modèle 3D au format DRC.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
### **Utilisation des options de sauvegarde RVM**
Le code ci-dessous montre comment définir les options de sauvegarde avant d'enregistrer un modèle 3D au format RVM.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
