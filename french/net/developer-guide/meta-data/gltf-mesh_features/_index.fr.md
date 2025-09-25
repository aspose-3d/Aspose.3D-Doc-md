---
title: Exemple de fonctionnalités de maillage glTF
type: docs
linkTitle: Caractéristiques des maillages glTF
description: Cette page de documentation montre comment créer un fichier glTF avec EXT_mesh_features en utilisant Aspose.3D pour .NET.
weight: 10
---

# Création de fichiers glTF avec EXT_mesh_features

Cet exemple montre comment créer un fichier glTF avec l'extension EXT_mesh_features en utilisant l'API Aspose.3D.

## Explication du code

Le code C# suivant crée un maillage avec des points de contrôle et des polygones, puis ajoute des ID de fonctionnalité aux points de contrôle avant d'enregistrer dans un fichier glTF

```csharp
// Cet exemple créera un fichier glTF avec EXT_mesh_features
// Tout d'abord, nous créons un maillage
var mesh = new Mesh();

// Ajouter des points de contrôle (sommets) au maillage
// Le premier ensemble de quatre points crée un carré dans le plan XY à y=1
mesh.ControlPoints.Add(new Vector4(0, 1, 0));  // Point 0
mesh.ControlPoints.Add(new Vector4(2, 1, 0));  // Point 1
mesh.ControlPoints.Add(new Vector4(2, 2, 0));  // Point 2
mesh.ControlPoints.Add(new Vector4(1, 2, 0));  // Point 3

// Le deuxième ensemble de quatre points crée un autre carré dans le plan XY à y=0
mesh.ControlPoints.Add(new Vector4(3, 0, 0));  // Point 4
mesh.ControlPoints.Add(new Vector4(4, 0, 0));  // Point 5
mesh.ControlPoints.Add(new Vector4(4, 1, 0));  // Point 6
mesh.ControlPoints.Add(new Vector4(3, 1, 0));  // Point 7

// Créer des faces triangulaires (polygones) à partir des points de contrôle
// Le premier carré (points 0-3) est divisé en deux triangles
mesh.CreatePolygon(0, 1, 2);  // Triangle 0-1-2
mesh.CreatePolygon(0, 2, 3);  // Triangle 0-2-3

// Le deuxième carré (points 4-7) est également divisé en deux triangles
mesh.CreatePolygon(4, 5, 6);  // Triangle 4-5-6
mesh.CreatePolygon(4, 6, 7);  // Triangle 4-6-7

// Ensuite, nous créons un élément de données utilisateur pour stocker les ID de fonctionnalité
// Cela associera les ID de fonctionnalité aux points de contrôle
var featureId = (VertexElementUserData)mesh.CreateElement(
    VertexElementType.UserData,  // Type d'élément
    MappingMode.ControlPoint,   // Appliquer aux points de contrôle
    ReferenceMode.Direct        // Mapping direct (non indexé)
);

// Attribuer des ID de fonctionnalité à chaque point de contrôle
// Les quatre premiers points obtiennent l'ID 0, les quatre suivants obtiennent l'ID 1
featureId.Data = new float[] { 0, 0, 0, 0, 1, 1, 1, 1 };

// Définir le nom d'attribut spécial qui conforme à la spécification EXT_mesh_features
// Le format _FEATURE_ID_<n> est reconnu par l'exportateur glTF
featureId.Name = "_FEATURE_ID_0";

// Enregistrer le maillage dans un fichier glTF binaire (GLB)
// L'exportateur générera automatiquement les données d'extension EXT_mesh_features
// Utiliser un chemin d'accès relatif pour le fichier de sortie
(new Scene(mesh)).Save("mesh_feature.glb");
```

## Concepts clés

### Création de maillage
- La classe `Mesh` représente une géométrie de maillage polygonal
- Les points de contrôle définissent les sommets du maillage
- La méthode `CreatePolygon` crée des faces triangulaires entre les points de contrôle

### ID de fonctionnalité
- Les ID de fonctionnalité permettent de regrouper la géométrie au sein d'un maillage
- Implémentés via `VertexElementUserData` avec une convention de nommage spéciale
- `_FEATURE_ID_0` indique qu'il s'agit d'un flux d'ID de fonctionnalité
- Plusieurs flux d'ID de fonctionnalité peuvent être créés avec des indices croissants

### Attribution de données
- Les ID de fonctionnalité sont stockés sous forme de valeurs flottantes
- Chaque point de contrôle reçoit une valeur d'ID de fonctionnalité correspondante
- Dans cet exemple, nous utilisons deux ID de fonctionnalité distincts 0 et 1

### Exportation de fichier
- L'enregistrement au format GLB préserve toutes les fonctionnalités, y compris EXT_mesh_features
- Aspose.3D gère automatiquement la génération de l'extension
- Le fichier résultant contient des métadonnées sur les fonctionnalités du maillage
- L'utilisation de chemins d'accès relatifs rend le code plus portable et plus facile à exécuter dans différents environnements

Cet exemple montre comment Aspose.3D peut être utilisé pour créer des fichiers glTF qui utilisent l'extension EXT_mesh_features pour une représentation avancée des données 3D.