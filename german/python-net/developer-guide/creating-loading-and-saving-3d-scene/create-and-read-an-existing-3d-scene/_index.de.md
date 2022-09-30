---
title: Erstellen und Lesen einer bestehenden Szene 3D
type: docs
weight: 10
url: /de/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API unterstützt das Erstellen der neuen 3D-Szenen von Grund auf und speichern Sie dann in einem beliebigen unterstützten Dateiformat. Entwickler können auch eine vorhandene 3D-Szene für Modifizierungs-, Ergänzungs-oder Verarbeitung zwecke laden.
---
## **Erstellen Sie eine leere 3D-Szene und speichern Sie in unterstützten 3D-Dateiformaten**
Aspose.3D API unterstützt das Erstellen der neuen 3D-Szenen von Grund auf und speichern Sie dann in einem beliebigen unterstützten Dateiformat. Entwickler können auch eine vorhandene 3D-Szene für Modifizierungs-, Ergänzungs-oder Verarbeitung zwecke laden.
### **Erstellen eines Szenen dokuments 3D**
Bitte führen Sie diese Schritte aus, um mit den APIs Aspose.3D ein Szenen dokument 3D zu erstellen:

1. Erstellen Sie eine Instanz der Klasse [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), die ein Szenen dokument 3D darstellt.
1. Generieren Sie ein 3D Scene-Dokument, indem Sie die [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-Methode des Scene-Klassen objekts aufrufen.
#### **Erstellen eines Szenen dokuments 3D: Programmieren von Samples**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
## **Lesen einer 3D Szene**
Mit Aspose.3D APIkönnen Entwickler alle unterstützten 3D-Dokumente laden. Die verfügbaren Konstruktoren der**Szene**Klasse dies zulassen, und sie akzeptieren eine gültige Datei pfad zeichenfolge. Die unterstützten lesbaren Dateiformate lauten wie folgt:

1. FBX 7.7 (ASCII, binär)
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
1. RVM (Text, binär)
1. ASE
1. USDZ
1. USD

Konstruktoren der `Scene`-Klasse erkennen das Dokument format 3D intern.
### **Lesen einer 3D Szene: Programming Samples**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
