---
title: Support du groupe IFC
type: docs
linkTitle: Support du groupe IFC
description: Cette page de documentation montre comment lire la hiérarchie sémantique d’un fichier IFC à l’aide d’Aspose.3D for .NET.
weight: 14
---

# Prise en charge du groupe IFC

## Vue d'ensemble

Le groupe IFC est une fonctionnalité récemment introduite dans Aspose.3D qui permet aux développeurs de travailler avec des groupes sémantiques définis dans les fichiers IFC. Contrairement à la hiérarchie géométrique traditionnelle, le groupe IFC offre un moyen de représenter les éléments du bâtiment avec un regroupement significatif, permettant une extraction et une manipulation de données plus riches.

## Qu’est‑ce que le groupe IFC ?

Dans le format IFC (Industry Foundation Classes), les groupes sont utilisés pour créer une hiérarchie basée sur la sémantique qui regroupe des entités liées (par exemple, murs, portes) sous un identifiant commun. Aspose.3D expose ces groupes via la classe [`Group`](https://reference.aspose.com/3d/net/aspose.threed/group/), permettant d’accéder au nom du groupe, aux informations sémantiques et aux nœuds enfants.

## Pourquoi utiliser le groupe IFC ?

L’utilisation du groupe IFC ajoute un contexte sémantique au graphe de scène purement géométrique, ce qui facilite les requêtes, le filtrage et le traitement des éléments du bâtiment en fonction de leur signification réelle. Cela simplifie des tâches telles que l’extraction de composants spécifiques du bâtiment, l’application de surcharges de matériaux ou la génération de rapports détaillés.

## Prise en charge par Aspose.3D

Aspose.3D fournit une prise en charge complète du groupe IFC dans l’API .NET. Les sections suivantes montrent comment activer et travailler avec les groupes IFC.

### Accès aux informations du groupe

```csharp
// Charger un fichier IFC
var scene = Aspose.ThreeD.Scene.FromFile("model.ifc");
// Parcourir les groupes
foreach(Group group in scene2.Library.Where(obj => obj is Group))
{
    Console.WriteLine($"Group Name: {group.Name}");
    Console.WriteLine($" Sub Groups: {group.Groups.Count}");
    Console.WriteLine($" Associated Nodes: {group.Nodes.Count}");
}
```

## Exemple de code

L’exemple complet suivant charge un fichier IFC et affiche la hiérarchie sémantique :

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");
scene.Open("sample.ifc", loadOptions);

void PrintGroup(Group group, string indent = "")
{
    foreach (var child in group.Groups)
    {
        Console.WriteLine($"{indent}{child.Name}");
        PrintGroup(child, indent + "  ");
    }
}

foreach(Group group in scene2.Library.Where(obj => obj is Group))
{
    PrintGroup(group);
}
```

## Références

* [Lien vers la documentation officielle Aspose.3D IFC](/3d/net/supported-file-formats/ifc)
* [Lien vers `Aspose.ThreeD.Group`](https://reference.aspose.com/3d/net/aspose.threed/group/)
* [Lien vers la spécification IFC](https://technical.buildingsmart.org/standards/ifc/ifc-schema-specifications/)