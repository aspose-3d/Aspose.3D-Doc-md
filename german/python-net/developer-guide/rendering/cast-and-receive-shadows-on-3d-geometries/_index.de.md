---
title: Werfen und empfangen Sie Schatten auf 3D Geometrien
type: docs
weight: 10
url: /de/python-net/cast-and-receive-shadows-on-3d-geometries/
description: Im Allgemeinen können einige 3D-Dateiformate schatten bezogene Einstellungen in Geometrie wie FBX speichern. Mit Aspose.3D for Python via .NET können Entwickler ein Bild rendern, indem sie Schatten aus der Sicht einer Lichtquelle zuordnen. Die Bildqualität hängt von der Lichtquelle, dem Höhenwinkel und dem Abstand zwischen der Kamera und den geometrischen Objekten ab.
---
{{% alert color="primary" %}}

Im Allgemeinen können einige 3D-Dateiformate schatten bezogene Einstellungen in Geometrie wie FBX speichern. Mit [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) können Entwickler ein Bild rendern, indem sie Schatten aus der Sicht einer Lichtquelle zuordnen. Die Bildqualität hängt von der Lichtquelle, dem Höhenwinkel und dem Abstand zwischen der Kamera und den geometrischen Objekten ab.

{{% /alert %}}
##  **Schatten werfen und empfangen**
Standard mäßig werfen alle Objekte in der Szene Schatten von einer Lichtquelle. Entwickler können auch Schatten pro Objekt basis in der Objekt oberfläche erhalten. Dieses Code beispiel zeigt, wie die Position von Licht-und Kamera objekten eingestellt wird. Es erstellt auch eine Ebene und platziert drei Objekte mit unterschied lichen Farben und Schatten einstellungen.

Alle Geometrien haben `cast_shadows = True` und `receive_shadows = True`, die Schatten von Red Box und Torus werden in das Flugzeug geworfen, die rote Box erhält keine Schatten und die blaue Box wirft keine Schatten.
###  **Programmier probe**
Dieses Code beispiel wirft und empfängt Schatten auf 3D Geometrien.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Rendering-CastAndReceiveShadow-CastAndReceiveShadow.py" >}}


**Rendern Ergebnis**

! [Todo: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
