---
title: Schatten werfen und empfangen unter 3D Geometries
type: docs
weight: 10
url: /de/net/cast-and-receive-shadows-on-3d-geometries/
description: Im Allgemeinen können einige 3D-Dateiformate schatten bezogene Einstellungen in Geometrie wie FBX speichern. Mithilfe von Aspose.3D for .NETkönnen Entwickler ein Bild rendern, indem sie Schatten aus der Sicht einer Lichtquelle abbilden. Die Bildqualität hängt von der Lichtquelle, dem Höhenwinkel und dem Abstand zwischen der Kamera und den geometrischen Objekten ab.
---
{{% alert color="primary" %}}

Im Allgemeinen können einige 3D-Dateiformate schatten bezogene Einstellungen in Geometrie wie FBX speichern. Verwendung[Aspose.3D for .NET](https://products.aspose.com/3d/net/)Entwickler können ein Bild rendern, indem sie Schatten aus der Sicht einer Lichtquelle abbilden. Die Bildqualität hängt von der Lichtquelle, dem Höhenwinkel und dem Abstand zwischen der Kamera und den geometrischen Objekten ab.

{{% /alert %}}
## **Schatten werfen und empfangen**
Standard mäßig werfen alle Objekte in der Szene Schatten von einer Lichtquelle. Entwickler können auch Schatten pro Objekt basis in der Objekt oberfläche erhalten. Dieses Code beispiel zeigt, wie die Position von Licht-und Kamera objekten eingestellt wird. Es erstellt auch eine Ebene und platziert drei Objekte mit unterschied lichen Farben und Schatten einstellungen.

Alle Geometrien haben `CastShadows = true` und `ReceiveShadows=true`, die Schatten von Red Box und Torus, die auf das Flugzeug geworfen wurden, die rote Box erhält keine Schatten und die blaue Box wirft keine Schatten.
### **Programmier probe**
Dieses Code beispiel wirft und empfängt Schatten auf 3D Geometrien.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Rendering-CastAndReceiveShadow-CastAndReceiveShadow.cs" >}}


**Rendern Ergebnis**

![Todo: bild_Alt_Text](cast-and-receive-shadows-on-3d-geometries_1.png)
