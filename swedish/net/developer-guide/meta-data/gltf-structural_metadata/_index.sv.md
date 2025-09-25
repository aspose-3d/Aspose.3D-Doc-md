---
title: glTF Strukturmetadataexempel
type: docs
linkTitle: glTF Strukturmetadata
description: "Denna dokumentationssida visar hur man läser strukturell metadata från en glTF-fil med Aspose.3D för .NET."
weight: 11
---

# Läsa strukturell metadata från glTF-filer

Detta exempel visar hur man läser strukturell metadata från en glTF-fil som innehåller EXT_structural_metadata-tillägget med Aspose.3D API.

## Code Explanation

Följande C#-kod laddar en glTF-scen med strukturell metadata, och läser och visar information om egenskapstabeller och deras egenskaper:

```csharp
// Ladda glTF-scen med EXT_structural_metadata från fil
var scene = Scene.FromFile("ComplexType.gltf");

// Ladda strukturell metadata från scen
var metadata = StructuralMetadata.From(scene);
Console.WriteLine("Dumping strukturell metadata från input glTF-fil:");

// Iterera genom alla egenskapstabeller i metadata
foreach (var propTable in metadata.PropertyTables)
{
    // Hämta meta klassen för egenskapstabellen
    Console.WriteLine($"Egenskapstabell {propTable.Name}, typnamn : {propTable.MetaClass.Name}");

    // Iterera genom alla egenskaper definierade i meta klassen
    foreach (var propertyDefinition in propTable.MetaClass.Properties)
    {
        // Hämta egenskapdata definierad i EXT_structural_metadata
        object property = propTable.Values[propertyDefinition.Name];
        
        // Dumpa egenskapnamn, typ och värde
        Console.WriteLine($"{propertyDefinition.Name} : {propertyDefinition.Type} = {property}");
    }
}
```

## Key Concepts

### Strukturell Metadata
- Klassen `StructuralMetadata` ger tillgång till metadata definierad i EXT_structural_metadata-tillägget
- Detta tillägg tillåter lagring av semantisk information om 3D-objekt
- Metadata kan inkludera egenskapstabeller som definierar attribut för objekt i scenen

### Egenskapstabeller
- Representerade av klassen `PropertyTable`
- Varje tabell har:
  - Ett namn
  - En meta klass som definierar strukturen
  - Värden som innehåller faktiska egenskapdata

### Meta Klasser
- Definierade av klassen `MetaClass`
- Beskriver strukturen för en egenskapstabell
- Innehåller en samling av egenskapdefinitioner
- Varje definition specificerar:
  - Namn på egenskapen
  - Typ av egenskapen
  - Andra metadataattribut

### Egenskapsåtkomst
- Egenskaper nås genom `Values`-ordboken för en egenskapstabell
- Nyckeln är egenskapnamnet som definierats i meta klassen
- Värden konverteras automatiskt till lämpliga typer när det är möjligt

Detta exempel visar hur Aspose.3D kan användas för att läsa och bearbeta strukturell metadata från glTF-filer, vilket gör det möjligt för utvecklare att få tillgång till rik semantisk information som lagras tillsammans med 3D-geometri.