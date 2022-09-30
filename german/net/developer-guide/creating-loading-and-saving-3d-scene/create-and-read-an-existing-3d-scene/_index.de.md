---
title: Erstellen und Lesen einer bestehenden Szene 3D
type: docs
weight: 10
url: /de/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API unterstützt das Erstellen der neuen 3D-Szenen von Grund auf und speichern Sie dann in einem beliebigen unterstützten Dateiformat. Entwickler können auch eine vorhandene 3D-Szene für Modifizierungs-, Ergänzungs-oder Verarbeitung zwecke laden.
---
## **Übersicht**
Der Artikel erklärt die folgenden Themen unter Verwendung der Manipulation bibliothek C# 3D Dateiformate.
- Erstellen Sie eine leere 3D Szene in C# von Grund auf neu
- Lesen oder Laden Sie bestehende 3D Szene in C#
- Speichern Sie die Szene 3D in den unterstützten Formaten 3D unter Verwendung von C#
- Arbeiten Sie mit 3D Szenen eigenschaften in C#

## **Erstellen Sie eine leere 3D-Szene und speichern Sie in unterstützten 3D-Dateiformaten**
Aspose.3D API unterstützt das Erstellen der neuen 3D-Szenen von Grund auf und speichern Sie dann in einem beliebigen unterstützten Dateiformat. Entwickler können auch eine vorhandene 3D-Szene für Modifizierungs-, Ergänzungs-oder Verarbeitung zwecke laden.

### **Erstellen eines Szenen dokuments 3D**
Bitte führen Sie diese Schritte in C# aus, um ein 3D Szenen dokument mit den APIs Aspose.3D zu erstellen:

1. Erstellen Sie eine Instanz der Klasse [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), die ein Szenen dokument 3D darstellt.
1. Generieren Sie ein 3D Scene-Dokument, indem Sie die [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-Methode des Scene-Klassen objekts aufrufen.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

## **Lesen einer 3D Szene**
Mit Aspose.3D APIkönnen Entwickler alle unterstützten 3D-Dokumente laden. Die verfügbaren Konstruktoren der `Scene`-Klasse erlauben dies und akzeptieren eine gültige Datei pfad zeichenfolge. Die unterstützten lesbaren Dateiformate lauten wie folgt:

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
1. Draco
1. 3MF
1. RVM (Text, binär)
1. ASE

Konstruktoren der `Scene`-Klasse erkennen das Dokument format 3D intern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

## **Arbeiten mit Szenen eigenschaften 3D**
Mit Aspose.3D API können Sie die Eigenschaften 3D Scene mithilfe der unter geordneten Knoten der Szene lesen. Das folgende Code beispiel C# zeigt die Verwendung dieser Funktion.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
