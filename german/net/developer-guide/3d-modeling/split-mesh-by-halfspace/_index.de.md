---
title: "Wie man ein Mesh durch eine Halbraum in Aspose.3D aufteilt"
type: docs
linkTitle: "Split Mesh by HalfSpace"
description: "Erfahren Sie, wie Sie 3D-Meshes mithilfe von Halbraum-Ebenen in Aspose.3D aufteilen"
weight: 10
---

# Aufteilen von Meshes durch Halbraum in Aspose.3D

Dieses Tutorial zeigt, wie Sie Aspose.3D verwenden, um Mesh-Aufteilungsoperationen mit Halbraum-Ebenen durchzuführen. Diese Technik ist nützlich, um bestimmte Abschnitte eines 3D-Modells basierend auf räumlichen Kriterien zu extrahieren.

## Verständnis von Halbraum-Operationen

Ein Halbraum stellt einen unendlichen Raum dar, der durch eine Ebene geteilt wird. In Kombination mit den booleschen Operationen von Aspose.3D ermöglicht es Ihnen, bestimmte Abschnitte eines Meshes zu extrahieren, die sich auf einer Seite der definierten Ebene befinden.

### Schlüsselkonzepte:
- **Halbraum**: Stellt einen unendlichen Raum dar, der durch eine Ebene geteilt wird
- **Boolesche Operationen**: Werden verwendet, um Mesh-Abschnitte relativ zum Halbraum zu extrahieren
- **Ebenengleichung**: Definiert als ax + by + cz + d = 0, wobei (a,b,c) der Normalenvektor ist
- **Positive Seite**: Der Teil des Raums, auf den der Ebenen-Normalenvektor zeigt

## Codebeispiel: Aufteilen eines Meshes mit Halbraum

Der folgende C#-Code demonstriert, wie ein einfaches Box-Mesh erstellt und mit einer Halbraum-Ebene aufgeteilt wird:

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Utilities;

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // Erstellen einer neuen 3D-Szene
        Scene scene = new Scene();
        
        // Erstellen eines Box-Meshes (Standardmaße 2x2x2)
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // Erstellen eines Halbraum-Schnittbereichs
        HalfSpace halfSpace = new HalfSpace();
        
        // Definieren der Ebenengleichung: ax + by + cz + d = 0
        // Verwenden eines Normalenvektors, der in Z-Richtung zeigt
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // Positionieren des Halbraums (Erstellen eines Knotens und Transformation)
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // Position bei z=0.5
        
        // Durchführen der booleschen Aufteilungsoperation
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // Hinzufügen des Ergebnisses zur Szene und Speichern
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("Mesh-Aufteilung mit Halbraum erfolgreich abgeschlossen.");
    }
}
```

## Code-Erklärung

### Namensraum-Anforderungen
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // Enthält die Klassen HalfSpace und BooleanOperator
using Aspose.ThreeD.Utilities; // Enthält Vector3- und Plane-Hilfsprogramme
```

### Erstellen der Geometrie
1. **Szeneninitialisierung**: `Scene scene = new Scene();`
2. **Box-Erstellung**: `(new Box()).ToMesh()` erstellt einen Standardwürfel
3. **Knotenhierarchie**: Mesh wird über einen untergeordneten Knoten zur Szene hinzugefügt

### Definieren der Schnittfläche
1. **Ebenendefinition**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - Erstellt eine horizontale XY-Ebene bei z=0
   - Normalenvektor (0,0,1) zeigt aufwärts

2. **Positionierung**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - Bewegt die Schnittfläche auf z=0.5
   - Beeinflusst, welcher Teil des Meshes erhalten bleibt

### Durchführen der Operation
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- Gibt den Teil des Meshes auf der positiven Seite der Ebene zurück
- Ergebnis wird wieder in die Knotenhierarchie hinzugefügt

### Speichern des Ergebnisses
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- Unterstützte Formate sind OBJ, STL, FBX, GLTF und mehr
- Nur der aufgeteilte Fragment wird gespeichert, nicht das ursprüngliche Mesh

## Visualisieren der Operation

### Originale Box-Abmessungen:
- Erstreckt sich von (-1,-1,-1) bis (1,1,1)
- Zentriert am Ursprung

### Mit Ebene bei z=0.5:
- Behält den Bereich bei, bei dem z > 0.5 (oberer Teil der Box)
- Verwirft den Bereich, bei dem z < 0.5 (unterer Teil)

## Erweiterte Nutzung

### Abrufen beider Seiten des Schnitts
```csharp
// Ursprünglicher Split (positive Seite)
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// Invertieren der Ebene für die negative Seite
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### Anpassen der Schnittfläche
```csharp
// Andere Ausrichtung - angewinkelter Schnitt
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

Diese Implementierung demonstriert die Kernfunktionalität der Mesh-Aufteilungsfunktionen von Aspose.3D mit Halbraum-Ebenen und ermöglicht so die präzise Extraktion von 3D-Geometrie basierend auf räumlichen Kriterien.