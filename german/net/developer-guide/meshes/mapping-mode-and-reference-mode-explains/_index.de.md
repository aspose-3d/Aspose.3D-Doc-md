---
title: Mapping Mode und Reference Mode erklärt
type: docs
weight: 10
url: /de/net/mapping-mode-and-reference-mode-explains
description: Mit Aspose.3D for .NET können Entwickler Mesh mit verschiedenen Vertex-Daten elementen definieren. Hier erklären wir, wie Daten der Komponente von Meshes zugeordnet und Daten neu erstellt werden.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) können Entwickler Meshes mit verschiedenen Vertex-Daten elementen definieren, einschl ießlich Normalen, Farben und Gewichten. Aspose.3D bietet zwei Mechanismen zur Optimierung der Daten wieder verwendung: `MappingMode` und `ReferenceMode`. Diese Mechanismen sind darauf ausgelegt, den Speicher bedarf von Netzen zu minimieren, insbesondere in fort geschrittenen Formaten wie FBX und USD. Mapping Mode ermöglicht eine effiziente Zuordnung von Scheitel punkt daten zu Netz komponenten, während Reference Mode die Referenz ierung von Vertex element daten über mehrere Netz komponenten hinweg erleichtert. Zusammen genommen verbessern diese Funktionen die Leistung und die Speicher effizienz und machen Aspose.3D zu einem leistungs starken Tool für den Umgang mit komplexen 3D-Modellen in .NET-Anwendungen.

{{% /alert %}}



###  `MappingMode` erklärt

 `MappingMode` bestimmt, wie die Element daten auf die Oberfläche der Geometrie in Aspose.3D for .NET abgebildet werden. Es bietet verschiedene Möglichkeiten, dieses Mapping zu definieren:

1. **Kontroll punkt**Jedes Daten element wird dem Kontroll punkt der Geometrie zugeordnet. Dieser Modus stellt sicher, dass jeder Kontroll punkt, der die Form der Geometrie definiert, einem bestimmten Daten element zugeordnet ist.
1. **Polygon vertex**Die Daten werden dem Scheitel punkt eines Polygons zugeordnet. In Fällen, in denen ein Kontroll punkt von mehreren Polygonen gemeinsam genutzt wird, verfügt jede Instanz des Kontroll punkts, wie sie in verschiedenen Polygonen angezeigt wird, über eigene Daten. Dies stellt sicher, dass selbst gemeinsam genutzte Kontroll punkte eindeutige Daten haben können, wenn sie als Eckpunkte für verschiedene Polygone dienen.
1. **Polygon**Die Daten werden dem gesamten Polygon zugeordnet. Dies bedeutet, dass alle Eckpunkte eines Polygons dasselbe Daten element gemeinsam haben. Dieser Modus ist nützlich, wenn einheitliche Daten auf die gesamte Polygon oberfläche angewendet werden müssen, um die Konsistenz innerhalb des Polygons sicher zustellen.
1. **Rand**Die Daten werden auf die Kanten der Geometrie abgebildet. Jeder Endpunkt einer Kante teilt dieselben Daten und bietet eine Möglichkeit, einheitliche Daten auf die Kanten anzuwenden, während unterschied liche Daten für verschiedene Kanten zugelassen werden. Dies kann besonders nützlich sein, um Eigenschaften zu definieren, die für Kanten spezifisch sind, wie z. B. Falten werte oder kanten basierte Attribute
1. **AllSame**Ein einzelnes Daten element wird auf die gesamte Oberfläche der Geometrie abgebildet. Unabhängig davon, ob die Daten als Kontroll punkte, Polygon scheitel punkte oder Kanten endpunkte interpret iert werden, wird derselbe Daten wert einheitlich auf alle Elemente angewendet. Dieser Modus ist ideal für Szenarien, in denen ein konstanter Wert in der gesamten Geometrie beibehalten werden muss, um sicher zustellen, dass ein einheitliches Attribut über das gesamte 3D-Modell verteilt ist.




###  `ReferenceMode` erklärt
 `ReferenceMode` definiert, ob Daten nach Indizes wieder verwendet werden sollen. Es gibt drei Richtlinien für `ReferenceMode`:

1.**Direkt**Daten werden direkt referenziert und in der `Data`-Eigenschaft von `VertexElement` gespeichert.
1.**Index To Direct**Werden die Daten durch Index referenziert und dann über Index in der Daten liste von `VertexElement` aufgerufen.
1.**Index**Daten werden nur durch Index referenziert, jetzt verwenden nur noch die `VertexElementMaterial` diesen Referenz modus. Dies ist ähnlich wie `IndexToDirect`, aber die Unterschiede sind, dass die Materialien unter der Eigenschaft `Node` `Materials` definiert sind, nicht in `VertexElementMaterial`, alle `VertexElement` funktionieren nur mit primitiven Daten.



Zum Beispiel bei einer Definition eines Würfels:

{{< highlight "csharp" >}}
var cube = new Mesh();
Vector4[] controlPoints = new Vector4[]
{
    new Vector4( -5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 10.0, -5.0, 1.0),
    new Vector4( -5.0, 10.0, -5.0, 1.0)
};
cube.ControlPoints.AddRange(controlPoints);

// Front face (Z+)
cube.CreatePolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
cube.CreatePolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
cube.CreatePolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
cube.CreatePolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
cube.CreatePolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
cube.CreatePolygon(new int[] { 3, 2, 6, 7 });

var vertexColor = (VertexElementVertexColor) cube.CreateElement(VertexElementType.VertexColor);
vertexColor.MappingMode = MappingMode.ControlPoint;
var red = new Vector4(1, 0, 0, 1);
var green = new Vector4(0, 1, 0, 1);
var blue = new Vector4(0, 0, 1, 1);
var white = new Vector4(1, 1, 1, 1);

{{< /highlight >}}

Wenn Sie den Kontroll punkten 0 und 1 Rot, den Steuer punkten 2 und 3 Grün, den Steuer punkten 4 und 5 Blau und den Kontroll punkten 6 und 7 Weiß zuweisen möchten, können Sie dies mit dem folgenden Ansatz erreichen:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.Direct;
vertexColor.Data.Add(red); // 0
vertexColor.Data.Add(red); // 1
vertexColor.Data.Add(green); // 2
vertexColor.Data.Add(green); // 3
vertexColor.Data.Add(blue); // 4
vertexColor.Data.Add(blue); // 5
vertexColor.Data.Add(white); // 6
vertexColor.Data.Add(white); // 7
{{< /highlight >}}

Um Kontroll punkten Farben effizient zuzuweisen und den Speicher verbrauch zu reduzieren, können Sie Indizes verwenden, um auf die Farben zu verweisen. Indem Sie die Farben separat definieren und dann mit Indizes referenzieren, können Sie die Redundanz minimieren. So können Sie dies erreichen:

Definieren Sie zunächst 4 Farben im Vector4-Typ für die eindeutigen Farben und verwenden Sie dann ein Array von 8 Indizes, um diese Farben jedem Kontroll punkt zuzuweisen:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.IndexToDirect;
vertexColor.Data.Add(red);
vertexColor.Data.Add(green);
vertexColor.Data.Add(blue);
vertexColor.Data.Add(white);

vertexColor.SetIndices(new int[] { 0, 0, 1, 1, 2, 2, 3, 3 });
{{< /highlight >}}

In diesem Ansatz:

1. Definieren Sie eindeutige Farben: Als Vector4-Instanzen werden nur 4 Farben definiert (rot, grün, blau, weiß).
1. Erstellen Sie ein Farbindex array: Ein Array von 8 Indizes wird verwendet, um diese 4 Farben für jeden Kontroll punkt zu referenz ieren.
1. Karten farben mithilfe von Indizes: Indem Sie die Farben über Indizes referenz ieren, reduzieren Sie den Speicher verbrauch, da jede Farbe einmal gespeichert und über mehrere Kontroll punkte hinweg wieder verwendet wird.

Diese Methode optimiert die Speicher nutzung, indem sie den redundanten Daten speicher reduziert und Ihr 3D-Modell effizienter macht.