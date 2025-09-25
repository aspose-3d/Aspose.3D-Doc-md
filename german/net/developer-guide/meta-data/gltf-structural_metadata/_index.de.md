---
title: "glTF Strukturelle Metadaten Beispiel"
type: docs
linkTitle: "glTF Strukturelle Metadaten"
description: "Diese Dokumentationsseite zeigt, wie man strukturelle Metadaten aus einer glTF-Datei mit Aspose.3D for .NET liest."
weight: 11
---

# Lesen struktureller Metadaten aus glTF-Dateien

Dieses Beispiel zeigt, wie man strukturelle Metadaten aus einer glTF-Datei, die die EXT_structural_metadata-Erweiterung enthält, mit der Aspose.3D-API liest.

## Code-Erklärung

Der folgende C#-Code lädt eine glTF-Szene mit strukturellen Metadaten und liest anschließend Informationen zu Eigenschaftstabellen und deren Eigenschaften:

```csharp
// Lade glTF-Szene mit EXT_structural_metadata aus Datei
var scene = Scene.FromFile("ComplexType.gltf");

// Lade strukturelle Metadaten aus der Szene
var metadata = StructuralMetadata.From(scene);
Console.WriteLine("Ausgabe struktureller Metadaten aus der Eingangsdatei glTF:");

// Iteriere durch alle Eigenschaftstabellen in den Metadaten
foreach (var propTable in metadata.PropertyTables)
{
    // Erhalte die Metaklasse der Eigenschaftstabelle
    Console.WriteLine($"Eigenschaftstabelle {propTable.Name}, Typname : {propTable.MetaClass.Name}");

    // Iteriere durch alle in der Metaklasse definierten Eigenschaften
    foreach (var propertyDefinition in propTable.MetaClass.Properties)
    {
        // Erhalte die in EXT_structural_metadata definierten Eigenschaftsdaten
        object property = propTable.Values[propertyDefinition.Name];
        
        // Gib Eigenschaftsnamen, Typ und Wert aus
        Console.WriteLine($"{propertyDefinition.Name} : {propertyDefinition.Type} = {property}");
    }
}
```

## Wichtige Konzepte

### Strukturelle Metadaten
- Die `StructuralMetadata`-Klasse bietet Zugriff auf in der EXT_structural_metadata-Erweiterung definierte Metadaten
- Diese Erweiterung erlaubt das Speichern semantischer Informationen zu 3D-Objekten
- Metadaten können Eigenschaftstabellen enthalten, die Attribute für Objekte in der Szene definieren

### Eigenschaftstabellen
- Dargestellt durch die `PropertyTable`-Klasse
- Jede Tabelle hat:
  - Einen Namen
  - Eine Metaklasse, die die Struktur definiert
  - Werte, die eigentliche Eigenschaftsdaten enthalten

### Metaklassen
- Definiert durch die `MetaClass`-Klasse
- Beschreiben die Struktur einer Eigenschaftstabelle
- Enthalten eine Sammlung von Eigenschaftsdefinitionen
- Jede Definition spezifiziert:
  - Name der Eigenschaft
  - Typ der Eigenschaft
  - Andere Metadatenattribute

### Eigenschaftszugriff
- Eigenschaften werden über das `Values`-Dictionary einer Eigenschaftstabelle zugegriffen
- Der Schlüssel ist der Eigenschaftsname, wie in der Metaklasse definiert
- Werte werden bei Möglichkeit automatisch in geeignete Typen konvertiert

Dieses Beispiel zeigt, wie Aspose.3D verwendet werden kann, um strukturelle Metadaten aus glTF-Dateien zu lesen und zu verarbeiten, wodurch Entwicklern der Zugriff auf reichhaltige semantische Informationen ermöglicht wird, die zusammen mit der 3D-Geometrie gespeichert sind.