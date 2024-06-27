---
title: Spécifiez 3D Options de chargement de fichier
type: docs
weight: 10
url: /fr/java/specify-3d-file-load-options/
description: Il existe plusieurs surcharges de méthode Scene.open ou surcharges de constructeur de classe Scène qui acceptent l'instance LoadOptions.
---
##  **3D Options de chargement des fichiers**
Il existe plusieurs surcharges de méthode Scene.open ou surcharges de constructeur de classe Scène qui acceptent l'instance LoadOptions. Il doit s'agir d'une instance d'une classe dérivée de la classe LoadOptions. Chaque format de charge a une classe correspondante qui contient les options de charge pour ce format de charge, par exemple il existe ColladaSaveOptions pour le format de sauvegarde FileFormat.COLLADA.
###  **Utilisation des options de chargement de 3DS discret**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSLoadOption.java" >}}
###  **Utilisation des options de charge Obj**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier 3D Obj.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJLoadOption.java" >}}
###  **Utilisation des options de chargement STL**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLLoadOption.java" >}}
###  **Utilisation des options de chargement U3D**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DLoadOption.java" >}}
###  **Utilisation des options de chargement glTF**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier glTF.
####  **Retournez la coordination de la texture V/T**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFLoadOptions.java" >}}
###  **Utilisation des options de charge Ply**
Le code ci-dessous montre comment définir les options de chargement avant de charger un modèle PLY.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-PLYLoadOption.java" >}}
###  **Utilisation des options de charge DirectX X**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier DirectX X.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-XLoadOption.java" >}}
###  **Utiliser FBX Options de chargement**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-LoadOptions-FBXLoadOptions.java" >}}
