---
title: Schatten werfen und empfangen unter 3D Geometries
type: docs
weight: 10
url: /de/python-net/cast-and-receive-shadows-on-3d-geometries/
description: Im Allgemeinen können einige 3D-Dateiformate schatten bezogene Einstellungen in Geometrie wie FBX speichern. Mithilfe von Aspose.3D für Python via .NET können Entwickler ein Bild rendern, indem sie Schatten aus der Sicht einer Lichtquelle abbilden. Die Bildqualität hängt von der Lichtquelle, dem Höhenwinkel und dem Abstand zwischen der Kamera und den geometrischen Objekten ab.
---
{{% alert color="primary" %}}

Im Allgemeinen können einige 3D-Dateiformate schatten bezogene Einstellungen in Geometrie wie FBX speichern. Verwendung[Aspose.3D für Python via .NET](https://products.aspose.com/3d/python-net/)Entwickler können ein Bild rendern, indem sie Schatten aus der Sicht einer Lichtquelle abbilden. Die Bildqualität hängt von der Lichtquelle, dem Höhenwinkel und dem Abstand zwischen der Kamera und den geometrischen Objekten ab.

{{% /alert %}}
## **Schatten werfen und empfangen**
Standard mäßig werfen alle Objekte in der Szene Schatten von einer Lichtquelle. Entwickler können auch Schatten pro Objekt basis in der Objekt oberfläche erhalten. Dieses Code beispiel zeigt, wie die Position von Licht-und Kamera objekten eingestellt wird. Es erstellt auch eine Ebene und platziert drei Objekte mit unterschied lichen Farben und Schatten einstellungen.

Alle Geometrien haben `cast_shadows = True` und `receive_shadows = True`, die Schatten von Red Box und Torus, die auf das Flugzeug geworfen wurden, die rote Box erhält keine Schatten und die blaue Box wirft keine Schatten.
### **Programmier probe**
Dieses Code beispiel wirft und empfängt Schatten auf 3D Geometrien.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Rendering-CastAndReceiveShadow-CastAndReceiveShadow.py" >}}


**Rendern Ergebnis**

![Todo: bild_Alt_Text](cast-and-receive-shadows-on-3d-geometries_1.png)
