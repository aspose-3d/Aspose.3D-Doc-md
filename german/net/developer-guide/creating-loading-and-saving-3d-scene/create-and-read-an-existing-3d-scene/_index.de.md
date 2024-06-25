---
title: Erstellen und Lesen einer bestehenden 3D-Szene
type: docs
weight: 10
url: /de/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API unterstützt das Erstellen der neuen 3D Szenen von Grund auf und speichern Sie dann in jedem unterstützten Dateiformat. Entwickler können auch eine vorhandene 3D-Szene für Änderungs-, Ergänzungs-oder Verarbeitung zwecke laden.
---
##  **Übersicht**
Der Artikel erklärt die folgenden Themen unter Verwendung der Manipulation bibliothek für Dateiformate C# 3D.
- Erstellen Sie eine leere 3D-Szene in C# von Grund auf neu
- Vorhandene 3D-Szene in C# lesen oder laden
- Speichern Sie die 3D-Szene in unterstützten 3D-Formaten mit C#
- Arbeiten Sie mit 3D Szenen eigenschaften in C#

##  **Erstellen Sie eine leere 3D-Szene und speichern Sie in unterstützten 3D-Dateiformaten**
Aspose.3D API unterstützt das Erstellen der neuen 3D Szenen von Grund auf und speichern Sie dann in jedem unterstützten Dateiformat. Entwickler können auch eine vorhandene 3D-Szene für Änderungs-, Ergänzungs-oder Verarbeitung zwecke laden.

###  **Erstellen eines 3D-Szenen dokuments**
Bitte folgen Sie diesen Schritten in C#, um ein 3D Szenen dokument mit den Aspose.3D APIs zu erstellen:

1. Erstellen Sie eine Instanz der [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse, die ein 3D-Szenen dokument darstellt.
1. Generieren Sie ein 3D-Szenen dokument, indem Sie die [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-Methode des Scene-Klassen objekts aufrufen.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

##  **Eine 3D-Szene lesen**
Mit Aspose.3D API können Entwickler alle unterstützten 3D-Dokumente laden. Die verfügbaren Konstruktoren der `Scene`-Klasse erlauben dies und sie akzeptieren eine gültige Datei pfad zeichenfolge. Die unterstützten lesbaren Dateiformate lauten wie folgt:

1. FBX 7.5 (ASCII, Binär)
1. FBX 7.4 (ASCII, Binär)
1. FBX 7.3 (ASCII, Binär)
1. FBX 7.2 (ASCII, Binär)
1. FBX 6.1 (ASCII, Binär)
1. STL (ASCII, Binär)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII, Binär)
1. Maya (ASCII, Binär)
1. OpenUSD (USD, USDZ)
1. Mixer
1. DXF
1. PLY (ASCII, Binär)
1. X (ASCII, Binär)
1. Draco
1. 3MF
1. RVM (Text, Binär)
1. ASE

Konstruktoren der `Scene`-Klasse erkennen das Dokument format 3D intern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

##  **Arbeiten mit 3D Szenen eigenschaften**
Aspose.3D API ermöglicht es Ihnen, die Szene eigenschaften von 3D mithilfe der unter geordneten Knoten der Szene zu lesen. Das folgende Code beispiel für C# zeigt die Verwendung dieser Funktion.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
