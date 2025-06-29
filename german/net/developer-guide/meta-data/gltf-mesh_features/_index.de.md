---
title: glTF Mesh Features Beispiel
type: docs
linkTitle: glTF Mesh Features
description: "Diese Dokumentationsseite demonstriert, wie man eine glTF-Datei mit EXT_mesh_features unter Verwendung von Aspose.3D für .NET erstellt."
weight: 10
---

# Erstellen von glTF-Dateien mit EXT_mesh_features

Dieses Beispiel demonstriert, wie eine glTF-Datei mit der Erweiterung EXT_mesh_features mithilfe der Aspose.3D API erstellt wird.

## Code-Erklärung

Der folgende C#-Code erstellt ein Mesh mit Kontrollpunkten und Polygonen und fügt dann Feature-IDs zu den Kontrollpunkten hinzu, bevor es in einer glTF-Datei gespeichert wird:

```csharp
// Dieses Beispiel erstellt eine glTF-Datei mit EXT_mesh_features
// Zuerst erstellen wir ein Mesh
var mesh = new Mesh();

// Kontrollpunkte (Eckpunkte) zum Mesh hinzufügen
// Der erste Satz von vier Punkten erstellt ein Quadrat in der XY-Ebene bei y=1
mesh.ControlPoints.Add(new Vector4(0, 1, 0));  // Punkt 0
mesh.ControlPoints.Add(new Vector4(2, 1, 0));  // Punkt 1
mesh.ControlPoints.Add(new Vector4(2, 2, 0));  // Punkt 2
mesh.ControlPoints.Add(new Vector4(1, 2, 0));  // Punkt 3

// Der zweite Satz von vier Punkten erstellt ein weiteres Quadrat in der XY-Ebene bei y=0
mesh.ControlPoints.Add(new Vector4(3, 0, 0));  // Punkt 4
mesh.ControlPoints.Add(new Vector4(4, 0, 0));  // Punkt 5
mesh.ControlPoints.Add(new Vector4(4, 1, 0));  // Punkt 6
mesh.ControlPoints.Add(new Vector4(3, 1, 0));  // Punkt 7

// Dreieckige Flächen (Polygone) aus den Kontrollpunkten erstellen
// Das erste Quadrat (Punkte 0-3) wird in zwei Dreiecke unterteilt
mesh.CreatePolygon(0, 1, 2);  // Dreieck 0-1-2
mesh.CreatePolygon(0, 2, 3);  // Dreieck 0-2-3

// Das zweite Quadrat (Punkte 4-7) wird ebenfalls in zwei Dreiecke unterteilt
mesh.CreatePolygon(4, 5, 6);  // Dreieck 4-5-6
mesh.CreatePolygon(4, 6, 7);  // Dreieck 4-6-7

// Dann erstellen wir ein Benutzerelement, um Feature-IDs zu speichern
// Dies verknüpft Feature-IDs mit Kontrollpunkten
var featureId = (VertexElementUserData)mesh.CreateElement(
    VertexElementType.UserData,  // Elementtyp
    MappingMode.ControlPoint,   // Auf Kontrollpunkte anwenden
    ReferenceMode.Direct        // Direkte Zuordnung (nicht indiziert)
);

// Feature-IDs jedem Kontrollpunkt zuweisen
// Die ersten vier Punkte erhalten ID 0, die nächsten vier erhalten ID 1
featureId.Data = new float[] { 0, 0, 0, 0, 1, 1, 1, 1 };

// Der spezielle Attributname, der der EXT_mesh_features-Spezifikation entspricht, festlegen
// Das Format _FEATURE_ID_<n> wird vom glTF-Exporteur erkannt
featureId.Name = "_FEATURE_ID_0";

// Das Mesh in einer glTF-Binärdatei (GLB) speichern
// Der Exporteur generiert automatisch die Daten für die EXT_mesh_features-Erweiterung
// Einen relativen Pfad für die Ausgabedatei verwenden
(new Scene(mesh)).Save("mesh_feature.glb");
```

## Schlüsselkonzepte

### Mesh-Erstellung
- Die Klasse `Mesh` stellt eine polygonale Mesh-Geometrie dar
- Kontrollpunkte definieren die Eckpunkte des Mesh
- Die Methode `CreatePolygon` erstellt dreieckige Flächen zwischen Kontrollpunkten

### Feature-IDs
- Feature-IDs ermöglichen die Gruppierung von Geometrie innerhalb eines Mesh
- Implementiert über `VertexElementUserData` mit einer speziellen Namenskonvention
- `_FEATURE_ID_0` zeigt an, dass dies ein Feature-ID-Stream ist
- Es können mehrere Feature-ID-Streams mit zunehmenden Indizes erstellt werden

### Datenzuweisung
- Feature-IDs werden als Gleitkommawerte gespeichert
- Jeder Kontrollpunkt erhält einen entsprechenden Feature-ID-Wert
- In diesem Beispiel verwenden wir zwei unterschiedliche Feature-IDs: 0 und 1

### Dateiexport
- Das Speichern im GLB-Format bewahrt alle Features, einschließlich EXT_mesh_features
- Aspose.3D verwaltet die Generierung der Erweiterung automatisch
- Die resultierende Datei enthält Metadaten über die Mesh-Features
- Die Verwendung relativer Pfade macht den Code portabler und einfacher in verschiedenen Umgebungen ausführbar

Dieses Beispiel demonstriert, wie Aspose.3D verwendet werden kann, um glTF-Dateien zu erstellen, die die Erweiterung EXT_mesh_features für eine erweiterte 3D-Datendarstellung nutzen.