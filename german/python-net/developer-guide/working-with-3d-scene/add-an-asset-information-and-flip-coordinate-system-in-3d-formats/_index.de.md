---
title: Hinzufügen eines Asset-Informations-und Flip-Koordinaten systems in den Formaten 3D
type: docs
weight: 10
url: /de/python-net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: Metadaten sind strukturierte Informationen, die das Abrufen, Verwenden oder Verwalten einer Informations ressource beschreiben, erklären, lokalisieren oder erleichtern. Aspose.3D for Python via .NET API ermöglicht es Entwicklern, eine Metadaten für die Szene zu definieren.
---
##  **Hinzufügen einer Asset-Information zur 3D-Szene**
Metadaten sind strukturierte Informationen, die das Abrufen, Verwenden oder Verwalten einer Informations ressource beschreiben, erklären, lokalisieren oder erleichtern. Aspose.3D for Python via .NET API ermöglicht es Entwicklern, eine Metadaten für die Szene zu definieren.
###  **Definieren Sie eine Metadaten für die Szene**
3D Shows erzeugen riesige Mengen an Metadaten und Bild informationen. Metadaten sind ein Aktiv posten und Teil der Show.

1. Initial isieren Sie eine 3D-Szene mit der `Scene`-Klasse.
1. Legen Sie den Namen der Anwendung/des Werkzeugs fest.
1. Legen Sie den Namen des Anwendungs-/Werkzeug herstellers fest.
1. Maßeinheit einstellen.
1. Maßeinheit Skalierung faktor festlegen.
1. Speichern Sie die 3D-Szene im unterstützten Dateiformat.

In diesem Beispiel nehmen wir an, dass die Szene von einem CAD-Tool namens "Egypt" erstellt wurde und von "Manualdesk" entworfen wurde:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize a 3D scene
scene = Scene()
#  Set application/tool name
scene.asset_info.application_name = "Egypt"
#  Set application/tool vendor name
scene.asset_info.application_vendor = "Manualdesk"
#  We use ancient egyption measurement unit Pole
scene.asset_info.unit_name = "pole"
#  One Pole equals to 60cm
scene.asset_info.unit_scale_factor = 0.6
#  The saved file
output = "out"  + "InformationToScene.fbx"
#  Save scene to 3D supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Flip Coordinate System in 3D Formaten**
Mit Aspose.3D for Python via .NET API können Benutzer das Koordinaten system in den Formaten OBJ, 3DS, STL und U3D umdrehen.

{{% alert color="primary" %}} 

Um eine 3ds-Datei zu importieren und im OBJ-Format zu speichern, wird die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse im Code verwendet.

{{% /alert %}} 

In diesem Beispiel haben wir das Koordinaten system beim Importieren der 3ds-Datei umgedreht und ohne Materialien im OBJ-Format gespeichert.
