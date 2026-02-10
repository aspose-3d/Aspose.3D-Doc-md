---
description: "Diese Dokumentationsseite demonstriert, wie man Eigenschaften aus einer IFC‑Datei mithilfe von Aspose.3D for .NET liest."
linkTitle: "IFC-Property-Unterstützung"
title: "IFC-Property-Unterstützung"
type: docs
weight: 14
---
## Überblick

IFC‑Property‑Support ist eine Funktion in Aspose.3D, die Entwicklern das Lesen von Property‑Sets und Elementmengen ermöglicht, die in IFC‑Dateien definiert sind. Diese Eigenschaften werden in den Entitäten `IFCPROPERTYSET` und `IFCELEMENTQUANTITY` gespeichert und können über die Methode `A3DObject.GetProperty` abgerufen werden.

## Was ist IFC‑Property‑Support?

Im IFC‑Schema können Bauelemente zugehörige Property‑Sets (`IFCPROPERTYSET`) und Elementmengen (`IFCELEMENTQUANTITY`) besitzen. Aspose.3D bildet diese auf ein generisches Property‑Interface ab und stellt sie über `A3DObject.GetProperty(string propertyName)` zur Verfügung. Dadurch können Werte wie Brandschutzklassifizierung, Wärme­durchgangskoeffizient oder Materialmengen direkt aus dem 3D‑Modell abgerufen werden.

## Warum IFC‑Property‑Support verwenden?

* Zugriff auf reichhaltige semantische Daten, ohne die IFC‑Datei manuell zu parsen.  
* Ermöglicht nachgelagerte Prozesse wie Kostenschätzung, Konformitätsprüfung oder Datenexport.  
* Kombination von geometrischen und nicht‑geometrischen Informationen in einem einzigen Workflow.

## Aspose.3D‑Unterstützung

Das folgende C#‑Beispiel zeigt, wie eine IFC‑Datei geladen und eine Property ausgelesen wird:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// Finde ein bestimmtes Element, z. B. eine Wand
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// Lese einen Property‑Wert
if (wallNode != null)
{
    // Property‑Name wie in der IFC‑Datei definiert
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // Beispiel für eine Elementmenge
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### Hinweise

* Property‑Namen, die in einer IFC‑Datei definiert sind, erhalten das Präfix `ifc:`, um Konflikte mit nativen Eigenschaften zu vermeiden.  
* Property‑Namen sind case‑sensitive und müssen exakt den in der IFC‑Datei definierten Namen entsprechen.  
* `GetProperty` gibt ein `object` zurück; bei Bedarf in den passenden Typ (z. B. `double`, `string`) casten.  
* Dieser Beispielcode demonstriert das Abrufen von Properties von `Node`; jedoch kann jedes Ableitungselement von `A3DObject` `GetProperty` verwenden.  
* Wenn eine Property nicht existiert, liefert `GetProperty` `null`.

## Referenzen

* [Link zur offiziellen Aspose.3D IFC‑Dokumentation](/3d/net/supported-file-formats/ifc)  
* Link zu [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/)  
* IFC‑Spezifikation für `IFCPROPERTYSET` und `IFCELEMENTQUANTITY`