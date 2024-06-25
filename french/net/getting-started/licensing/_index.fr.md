---
title: Licensing
type: docs
weight: 60
url: /fr/net/licensing/
description: Aperçu des exigences Licensing et de la version d'évaluation Limitations pour le traitement des formats de fichier 3D dans C#.
---
Aperçu des exigences Licensing et de la version d'évaluation Limitations pour le traitement des formats de fichier 3D dans C#.

##  **Limitations de la version d'évaluation**
Une version d'évaluation gratuite de Aspose.3D for .NET peut être téléchargée à partir de la section téléchargements du site Web de Aspose à: [Télécharger Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
###  **Limitation**
La version d'évaluation fournit toutes les fonctionnalités, sauf ce qui suit:

- Les utilisateurs ne peuvent ouvrir/importer un maximum de 50 3D documents à une scène.
- Chaque nœud ne peut pas avoir plus de 5 nœuds enfants.
- Chaque nœud ne peut pas avoir plus de 2 entités attachées.
- Chaque géométrie ne peut pas avoir plus de 2 éléments de sommet attachés.
- Chaque nœud ne peut pas avoir plus de 1 matériau.
- Les utilisateurs ne peuvent enregistrer qu'un maximum de 50 3D documents dans une scène.
- Les utilisateurs verront également un filigrane d'évaluation dans les images rendues et tous les autres fichiers de sortie.

{{% alert color="primary" %}} 
Si vous utilisez Aspose.3D sans licence appropriée, il pourrait déclencher un `Aspose.ThreeD.TrialException` lorsque l'utilisation atteint les restrictions sans licence, vous pouvez désactiver l'exception en:

* [Acheter une licence complète en vedette](https://purchase.aspose.com/buy).
* Demandez une licence temporaire de 30 jours, veuillez vous référer à [Comment obtenir une licence temporaire?](https://purchase.aspose.com/temporary-license) Pour plus d'informations.
.
* Définissez `Aspose.ThreeD.TrialException.SuppressTrialException` sur `true`, le `TrialException` ne sera pas levé pendant l'appel `Open/Save` sur Scène, mais les restrictions ci-dessus ne seront pas levées.
* Utilisez manuellement un bloc `try/catch` sur `Scene.Open/Save`, cette exception est juste une notification, ignorer cela n'affectera pas le chargement/sauvegarde de la scène.

{{% /alert %}} 

##  **Appliquer la licence à l'aide d'un objet Fichier ou Stream**
La licence peut être chargée à partir d'un [Fichier](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile) ou [Objet stream](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET essaiera de trouver la licence aux emplacements suivants:

1. Chemin explicite.
1. Le dossier qui contient Aspose.3D.dll.
1. Le dossier qui contient l'assembly qui a appelé Aspose.3D.dll.
1. Le dossier qui contient l'assembly d'entrée (votre. Exe).
1. Une ressource incorporée dans l'assembly qui a appelé Aspose.3D.dll.

Le moyen le plus simple de définir une licence consiste à placer le fichier de licence dans le même dossier que le fichier Aspose.3D.dll et à spécifier le nom du fichier, sans chemin d'accès, comme indiqué dans l'exemple ci-dessous.

{{% alert color="primary" %}} 

Si vous utilisez un autre Aspose for .NET API avec Aspose.3D for .NET, veuillez spécifier l'espace de noms pour la licence comme `Aspose.ThreeD.License`.

{{% /alert %}} 
###  **Chargement d'une licence à partir d'un fichier**
La façon la plus simple d'appliquer une licence est de placer le fichier de licence dans le même dossier que le fichier Aspose.3D.dll et de spécifier uniquement le nom du fichier sans chemin.

{{% alert color="primary" %}} 

Lorsque vous appelez la méthode `SetLicense`, le nom de licence que vous passez doit être celui du fichier de licence. Par exemple, si vous changez le nom du fichier de licence en "Aspose.3D.lic.xml", passez ce nom de fichier à la méthode `threeD.SetLicense(…)`.

{{% /alert %}} 

**Exemple:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
###  ` `**Chargement d'une licence à partir d'un objet Stream**
L'exemple suivant montre comment charger une licence à partir d'un flux.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
##  **Appliquer la licence à l'aide de la ressource intégrée**
Une façon d'appliquer une licence est de la définir [En utilisant un objet de fichier ou de flux](). Une autre façon intéressante d'empaqueter la licence avec votre application et de vous assurer qu'elle ne sera pas perdue est de l'inclure en tant que ressource incorporée dans l'un des assemblys qui appelle la DLL du composant (inclus dans Aspose.3D).

Pour inclure le fichier de licence en tant que ressource intégrée:

1. Dans Visual Studio .NET, incluez le fichier de licence (.lic) dans le projet en sélectionnant**Fichier**, Puis**Ajouter un élément existant**Et finalement**Ajouter**.
1. Sélectionnez le fichier dans l'Explorateur de solutions.
1. Réglez le**Construire une action**À**Ressource intégrée**Dans la fenêtre Propriétés.
1. Pour accéder à la licence incorporée dans l'assembly (en tant que ressource incorporée), ajoutez simplement le fichier de licence en tant que ressource incorporée au projet et passez le nom du fichier de licence à la méthode SetLicense. La classe License trouve automatiquement le fichier de licence dans les ressources incorporées. Il n'est pas nécessaire d'appeler les méthodes GetExecutingAssembly et GetManifestResourceStream de la classe System.Reflection.Assembly dans le Framework Microsoft .NET.

L'extrait de code suivant est utilisé pour définir la licence.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
##  **Appliquer une licence mesurée**
Aspose.3D for .NET API permet aux développeurs d'appliquer une licence mesurée. C'est un nouveau mécanisme de licence. Le nouveau mécanisme d'octroi de licences sera utilisé en même temps que la méthode d'octroi de licences existante. Les clients qui souhaitent être facturés en fonction de l'utilisation des fonctionnalités API peuvent utiliser la licence mesurée. Pour plus de détails, veuillez consulter la section [Compté Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered).

Une nouvelle classe [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) a été ajoutée pour appliquer la clé mesurée. Cet exemple de code montre comment définir des clés publiques et privées dosées:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
