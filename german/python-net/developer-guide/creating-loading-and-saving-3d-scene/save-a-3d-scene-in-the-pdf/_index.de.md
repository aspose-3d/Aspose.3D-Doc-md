---
title: Sparen Sie eine 3D-Szene in der PDF
type: docs
weight: 60
url: /de/python-net/save-a-3d-scene-in-the-pdf/
description: Die Scene-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können eine 3D-Szene erstellen, indem sie Kamera, Licht, Polygone und verschiedene andere Entitäten hinzufügen. Sie können jetzt auch eine 3D-Szene im PDF-Dateiformat speichern.
---
{{% alert color="primary" %}} 

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können eine 3D-Szene erstellen, indem sie Kamera, Licht, Polygone und verschiedene andere Entitäten hinzufügen. Sie können jetzt auch eine 3D-Szene im PDF-Dateiformat speichern.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for Python via .NET schreibt direkt die Informationen über API und Versions nummer in Ausgabe dokumenten. Wenn Sie beispiels weise eine Zeichnung nach PDF rendern, füllt Aspose.3D for Python via .NET das Feld `Application` mit dem Wert 'Aspose auf. Feld 3D' und `PDF Producer` mit Wert, e.g 'Aspose.3D 17,9'.

Bitte beachten Sie, dass Sie Aspose nicht anweisen können. Diagramm für Python via .NET API, diese Informationen aus Ausgabe dokumenten zu ändern oder zu entfernen.

{{% /alert %}} 
##  **Erstellen Sie einen 3D PDF mit einem Zylinder und rendern Sie ihn im schattierten Illustration modus mit einer optimierten Beleuchtung von CAD**
Die Save-Methode der `Scene`-Klasse ermöglicht es, eine 3D-Szene im PDF-Format zu speichern. Entwickler können jede von 3D unterstützte Datei laden oder eine neue 3D-Szene erstellen. Sie können eine 3D-Szene im PDF-Format speichern, wie in diesem Code beispiel gezeigt:

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Cylinder
from aspose.threed.shading import PhongMaterial
from aspose.threed.formats import PdfSaveOptions, PdfLightingScheme, PdfRenderMode
# Create a new scene
scene = Scene()
# Create a cylinder child node
cylinder = scene.root_node.create_child_node("cylinder", Cylinder())
cylinder.material = PhongMaterial()
# Set rendering mode and lighting scheme
opt = PdfSaveOptions()
opt.lighting_scheme = PdfLightingScheme.CAD
opt.render_mode = PdfRenderMode.SHADED_ILLUSTRATION
# Save in the PDF format
scene.save("output_out.pdf", opt)

{{< /highlight >}}
