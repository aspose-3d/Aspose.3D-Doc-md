---
title: "Comment diviser un maillage par un demi-espace dans Aspose.3D"
type: docs
linkTitle: "Split Mesh by HalfSpace"
description: "Apprenez à diviser les maillages 3D à l'aide de plans HalfSpace dans Aspose.3D"
weight: 10
---

# Division des Maillages par Demi-Espace dans Aspose.3D

Ce tutoriel explique comment utiliser Aspose.3D pour effectuer des opérations de division de maillages à l'aide de plans Demi-Espace. Cette technique est utile pour extraire des portions spécifiques d'un modèle 3D en fonction de critères spatiaux.

## Comprendre les Opérations Demi-Espace

Un Demi-Espace représente un espace infini divisé par un plan. Lorsqu'il est combiné avec les opérations booléennes d'Aspose.3D, il vous permet d'extraire des portions spécifiques d'un maillage qui existent d'un côté du plan défini.

### Concepts clés :
- **Demi-Espace**: Représente un espace infini divisé par un plan
- **Opérations Booléennes**: Utilisées pour extraire des portions de maillage par rapport au Demi-Espace
- **Équation de Plan**: Définie comme ax + by + cz + d = 0, où (a,b,c) est le vecteur normal
- **Côté Positif**: La portion d'espace où le vecteur normal du plan pointe

## Exemple de Code : Division d'un Maillage avec un Demi-Espace

Le code C# suivant montre comment créer un maillage de boîte simple et le diviser à l'aide d'un plan Demi-Espace :

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Utilities;

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // Créer une nouvelle scène 3D
        Scene scene = new Scene();
        
        // Créer un maillage de boîte (dimensions 2x2x2 par défaut)
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // Créer un plan de coupe Demi-Espace
        HalfSpace halfSpace = new HalfSpace();
        
        // Définir l'équation du plan : ax + by + cz + d = 0
        // Utiliser le vecteur normal pointant dans la direction Z
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // Positionner le Demi-Espace (créer un nœud et une transformation)
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // Positionner à z=0.5
        
        // Effectuer l'opération de division booléenne
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // Ajouter le résultat à la scène et enregistrer
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("Division du maillage à l'aide d'un Demi-Espace terminée avec succès.");
    }
}
```

## Explication du Code

### Exigences de l'Espace de Noms
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // Contient les classes HalfSpace et BooleanOperator
using Aspose.ThreeD.Utilities; // Contient les utilitaires Vector3 et Plane

### Création de la Géométrie
1. **Initialisation de la Scène**: `Scene scene = new Scene();`
2. **Création de la Boîte**: `(new Box()).ToMesh()` crée un cube standard
3. **Hiérarchie de Nœuds**: Le maillage est ajouté à la scène via un nœud enfant

### Définition du Plan de Coupe
1. **Définition du Plan**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - Crée un plan XY horizontal à z=0
   - Le vecteur normal (0,0,1) pointe vers le haut

2. **Positionnement**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - Déplace le plan de coupe à z=0.5
   - Affecte la portion du maillage qui est conservée

### Effectuer l'Opération
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- Renvoie la portion du maillage du côté positif du plan
- Le résultat est ajouté à la hiérarchie de la scène

### Enregistrer le Résultat
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- Les formats pris en charge incluent OBJ, STL, FBX, GLTF et plus encore
- Seule la portion divisée est enregistrée, pas le maillage d'origine

## Visualisation de l'Opération

### Dimensions d'origine de la Boîte :
- S'étend de (-1,-1,-1) à (1,1,1)
- Centrée sur l'origine

### Avec le plan à z=0.5 :
- Conserve la portion où z > 0.5 (partie supérieure de la boîte)
- Rejette la portion où z < 0.5 (partie inférieure)

## Utilisation Avancée

### Obtenir les Deux Côtés de la Coupe
```csharp
// Division initiale (côté positif)
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// Inverser le plan pour le côté négatif
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### Ajuster le Plan de Coupe
```csharp
// Orientation différente - coupe inclinée
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

Cette implémentation démontre les fonctionnalités de base des capacités de division de maillage d'Aspose.3D à l'aide de plans Demi-Espace, permettant l'extraction précise de la géométrie 3D en fonction de critères spatiaux.