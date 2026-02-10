---
description: "Cette page de documentation montre comment lire les propriétés d'un fichier IFC à l'aide d'Aspose.3D for .NET."
linkTitle: "Support des propriétés IFC"
title: "Support de propriétés IFC"
type: docs
weight: 14
---
## Aperçu

La prise en charge des propriétés IFC est une fonctionnalité d’Aspose.3D qui permet aux développeurs de lire les ensembles de propriétés et les quantités d’éléments définis dans les fichiers IFC. Ces propriétés sont stockées dans les entités `IFCPROPERTYSET` et `IFCELEMENTQUANTITY` et peuvent être accessibles via la méthode `A3DObject.GetProperty`.

## Qu’est‑ce que la prise en charge des propriétés IFC ?

Dans le schéma IFC, les éléments du bâtiment peuvent avoir des ensembles de propriétés associés (`IFCPROPERTYSET`) et des quantités d’éléments (`IFCELEMENTQUANTITY`). Aspose.3D les mappe à une interface de propriété générique, les exposant via `A3DObject.GetProperty(string propertyName)`. Cela permet de récupérer des valeurs telles que la classe de feu, la transmittance thermique ou les quantités de matériaux directement depuis le modèle 3D.

## Pourquoi utiliser la prise en charge des propriétés IFC ?

* Accéder à des données sémantiques riches sans analyser manuellement le fichier IFC.  
* Permettre des processus en aval tels que l’estimation des coûts, la vérification de conformité ou l’exportation de données.  
* Combiner informations géométriques et non géométriques dans un même flux de travail.

## Prise en charge par Aspose.3D

L’exemple C# suivant montre comment charger un fichier IFC et lire une propriété :

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// Trouver un élément spécifique, p. ex., un mur
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// Récupérer la valeur d'une propriété
if (wallNode != null)
{
    // Nom de la propriété tel que défini dans le fichier IFC
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // Exemple de quantité d'élément
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### Remarques

* Les noms de propriétés définis dans un fichier IFC sont préfixés par `ifc:` afin d’éviter les conflits avec les propriétés natives.  
* Les noms de propriétés sont sensibles à la casse et doivent correspondre exactement aux noms définis dans le fichier IFC.  
* `GetProperty` renvoie un `object` ; effectuez le cast vers le type approprié (par ex., `double`, `string`) selon les besoins.  
* Ce code d’exemple montre la récupération de propriétés à partir de `Node` ; toutefois, tout descendant de `A3DObject` peut utiliser `GetProperty`.  
* Si une propriété n’existe pas, `GetProperty` renvoie `null`.

## Références

* [Lien vers la documentation officielle Aspose.3D IFC](/3d/net/supported-file-formats/ifc)  
* Lien vers [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/)  
* Spécification IFC pour `IFCPROPERTYSET` et `IFCELEMENTQUANTITY`