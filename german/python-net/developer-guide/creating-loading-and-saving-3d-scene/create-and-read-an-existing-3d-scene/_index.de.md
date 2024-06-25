---
title: Erstellen und Lesen einer bestehenden 3D-Szene
type: docs
weight: 10
url: /de/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API unterstützt das Erstellen der neuen 3D Szenen von Grund auf und speichern Sie dann in jedem unterstützten Dateiformat. Entwickler können auch eine vorhandene 3D-Szene für Änderungs-, Ergänzungs-oder Verarbeitung zwecke laden.
---
##  **Erstellen Sie eine leere 3D-Szene und speichern Sie in unterstützten 3D-Dateiformaten**
Aspose.3D API unterstützt das Erstellen der neuen 3D Szenen von Grund auf und speichern Sie dann in jedem unterstützten Dateiformat. Entwickler können auch eine vorhandene 3D-Szene für Änderungs-, Ergänzungs-oder Verarbeitung zwecke laden.
###  **Erstellen eines 3D-Szenen dokuments**
Bitte führen Sie diese Schritte aus, um ein 3D-Szenen dokument mit den Aspose.3D-APIs zu erstellen:

1. Erstellen Sie eine Instanz der [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse, die ein 3D-Szenen dokument darstellt.
1. Generieren Sie ein 3D-Szenen dokument, indem Sie die [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-Methode des Scene-Klassen objekts aufrufen.
####  **Erstellen eines 3D-Szenen dokuments: Programmieren von Samples**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
##  **Eine 3D-Szene lesen**
Mit Aspose.3D API können Entwickler alle unterstützten 3D-Dokumente laden. Die verfügbaren Konstruktoren der**Szene**Klasse dies zulassen, und sie akzeptieren eine gültige Datei pfad zeichenfolge. Die unterstützten lesbaren Dateiformate lauten wie folgt:

1. FBX 7,7 (ASCII, Binär)
1. FBX 7.6 (ASCII, Binär)
1. FBX 7.5 (ASCII, Binär)
1. FBX 7.4 (ASCII, Binär)
1. FBX 7.3 (ASCII, Binär)
1. FBX 7.2 (ASCII, Binär)
1. STL (ASCII, Binär)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binär)
1. X (ASCII, Binär)
1. XYZ
1. Draco
1. 3MF
1. RVM (Text, Binär)
1. ASE
1. USDZ
1. USD

Konstruktoren der `Scene`-Klasse erkennen das Dokument format 3D intern.
###  **Lesen einer 3D-Szene: Samples programmieren**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
