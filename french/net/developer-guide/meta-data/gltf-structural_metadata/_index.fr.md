---
title: "Exemple de métadonnées structurelles glTF"
type: docs
linkTitle: "Métadonnées structurelles glTF"
description: "Cette page de documentation démontre comment lire les métadonnées structurelles à partir d'un fichier glTF en utilisant Aspose.3D pour .NET."
weight: 11
---

# Lecture des métadonnées structurelles à partir des fichiers glTF

Cet exemple démontre comment lire les métadonnées structurelles à partir d'un fichier glTF contenant l'extension EXT_structural_metadata en utilisant l'API Aspose.3D.

## Explication du code

Le code C# suivant charge une scène glTF avec des métadonnées structurelles, puis lit et affiche des informations sur les tables de propriétés et leurs propriétés :

```csharp
// Charger la scène glTF avec EXT_structural_metadata à partir du fichier
var scene = Scene.FromFile("ComplexType.gltf");

// Charger les métadonnées structurelles à partir de la scène
var metadata = StructuralMetadata.From(scene);
Console.WriteLine("Affichage des métadonnées structurelles du fichier glTF d'entrée:");

// Itérer à travers toutes les tables de propriétés dans les métadonnées
foreach (var propTable in metadata.PropertyTables)
{
    // Obtenir la classe méta de la table de propriété
    Console.WriteLine($"Table de propriété {propTable.Name}, nom du type : {propTable.MetaClass.Name}");

    // Itérer à travers toutes les propriétés définies dans la classe méta
    foreach (var propertyDefinition in propTable.MetaClass.Properties)
    {
        // Obtenir les données de propriété définies dans EXT_structural_metadata
        object property = propTable.Values[propertyDefinition.Name];
        
        // Afficher le nom, le type et la valeur de la propriété
        Console.WriteLine($"{propertyDefinition.Name} : {propertyDefinition.Type} = {property}");
    }
}
```

## Concepts clés

### Métadonnées structurelles
- La classe `StructuralMetadata` fournit un accès aux métadonnées définies dans l'extension EXT_structural_metadata
- Cette extension permet de stocker des informations sémantiques sur les objets 3D
- Les métadonnées peuvent inclure des tables de propriétés qui définissent des attributs pour les objets de la scène

### Tables de propriétés
- Représentées par la classe `PropertyTable`
- Chaque table possède :
  - Un nom
  - Une classe méta qui définit la structure
  - Des valeurs contenant les données réelles des propriétés

### Classes métas
- Définies par la classe `MetaClass`
- Décrivent la structure d'une table de propriété
- Contiennent une collection de définitions de propriétés
- Chaque définition spécifie :
  - Le nom de la propriété
  - Le type de la propriété
  - D'autres attributs de métadonnées

### Accès aux propriétés
- Les propriétés sont accessibles via le dictionnaire `Values` d'une table de propriété
- La clé est le nom de la propriété tel que défini dans la classe méta
- Les valeurs sont automatiquement converties en types appropriés lorsque c'est possible

Cet exemple démontre comment Aspose.3D peut être utilisé pour lire et traiter des métadonnées structurelles à partir de fichiers glTF, permettant aux développeurs d'accéder à des informations sémantiques riches stockées avec la géométrie 3D.