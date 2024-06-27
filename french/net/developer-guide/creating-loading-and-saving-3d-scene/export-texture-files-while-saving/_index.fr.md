---
title: Exporter des fichiers de texture tout en économisant 3D scène
type: docs
weight: 10
url: /fr/net/export-texture-files-while-saving-3d-scene
description: En utilisant Aspose.3D for .NET, les développeurs peuvent exporter des fichiers de texture vers le système de fichiers tout en économisant 3D scène.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), lors de l'exportation d'une scène vers des fichiers, il est souvent nécessaire d'exporter les textures, qu'elles soient incorporées ou externes, vers le même répertoire. Aspose.3D for .NET facilite ce processus, en s'assurant que toutes les textures sont correctement gérées et stockées avec la scène exportée. Ce guide montre comment y parvenir.

{{% /alert %}}

Pour exporter une scène et s'assurer que toutes les textures associées sont enregistrées dans le même répertoire, procédez comme suit:


{{% highlight "csharp" %}}

Scene scene = Scene.FromFile(@"BoomBox.glb");
var opt = new ObjSaveOptions();
opt.ExportTextures = true;
scene.Save(@"D:\tmp\boombox\output.obj", opt);

{{% /highlight %}}


Tous les objets `SaveOptions` dans Aspose.3D incluent la propriété `ExportTextures`, qui simplifie le processus de gestion des textures lors de l'exportation. Cette propriété garantit que toutes les textures, qu'elles soient externes ou incorporées, sont enregistrées dans le répertoire de sortie spécifié. Cette fonctionnalité est compatible avec divers formats de fichiers qui prennent en charge l'exportation de textures, tels que FBX, 3DS, OBJ, USD, GLTF et DAE.



Explication

1. Charger la scène: La scène est chargée à partir du fichier d'entrée.
1. Configurer les options de sauvegarde: Définissez `ExportTextures` à `true`.
1. Exporter la scène: la scène est enregistrée dans le répertoire de sortie avec les chemins de texture mis à jour.


En tirant parti de la propriété `ExportTextures` dans `SaveOptions`, vous pouvez exporter de manière transparente des scènes 3D avec leurs textures, en veillant à ce que toutes les ressources nécessaires soient organisées dans un seul répertoire. Cette fonctionnalité améliore la portabilité et la facilité d'utilisation des fichiers 3D sur diverses plates-formes et applications.

##  **Ressources**

1. [Tutoriel en ligne](https://products.aspose.com/3d/tutorial/)
1. [SaveOptions](https://reference.aspose.com/3d/net/aspose.threed.formats/saveoptions/)
