---
title: Exportieren Sie Textur dateien, während Sie die 3D-Szene sparen
type: docs
weight: 10
url: /de/net/export-texture-files-while-saving-3d-scene
description: Mit Aspose.3D for .NET können Entwickler Textur dateien in das Dateisystem exportieren und gleichzeitig 3D Szene speichern.
---
{{% alert color="primary" %}}

Wenn Sie [Aspose.3D for .NET](https://products.aspose.com/3d/net/) verwenden, müssen Sie beim Exportieren einer Szene in Dateien häufig die Texturen, ob eingebettet oder extern, in dasselbe Verzeichnis exportieren. Aspose.3D for .NET erleichtert diesen Prozess, um sicher zustellen, dass alle Texturen ordnungs gemäß verwaltet und zusammen mit der exportierten Szene gespeichert werden. Dieser Leitfaden zeigt, wie dies erreicht werden kann.

{{% /alert %}}

Führen Sie die folgenden Schritte aus, um eine Szene zu exportieren und sicher zustellen, dass alle zugehörigen Texturen in demselben Verzeichnis gespeichert werden:


{{% highlight "csharp" %}}

Scene scene = Scene.FromFile(@"BoomBox.glb");
var opt = new ObjSaveOptions();
opt.ExportTextures = true;
scene.Save(@"D:\tmp\boombox\output.obj", opt);

{{% /highlight %}}


Alle `SaveOptions`-Objekte in Aspose.3D enthalten die `ExportTextures`-Eigenschaft, die das Verwalten von Texturen während des Exports vereinfacht. Diese Eigenschaft stellt sicher, dass alle Texturen, ob extern oder eingebettet, im angegebenen Ausgabe verzeichnis gespeichert werden. Diese Funktion ist mit verschiedenen Dateiformaten kompatibel, die den Texture xport unterstützen, wie z. B. FBX, 3DS, OBJ, USD, GLTF und DAE.



Erklärung

1. Szene laden: Die Szene wird aus der Eingabe datei geladen.
1. Speichern Optionen konfigurieren: Legen Sie `ExportTextures` auf `true` fest.
1. Szene exportieren: Die Szene wird im Ausgabe verzeichnis mit den aktualisierten Textur pfaden gespeichert.


Durch die Nutzung der `ExportTextures`-Eigenschaft in `SaveOptions` können Sie nahtlos 3D-Szenen zusammen mit ihren Texturen exportieren, um sicher zustellen, dass alle erforderlichen Assets in einem einzigen Verzeichnis organisiert sind. Diese Funktion verbessert die Portabilität und Benutzer freundlich keit von 3D-Dateien auf verschiedenen Plattformen und Anwendungen.

##  **Ressourcen**

1. [Online-Tutorial](https://products.aspose.com/3d/tutorial/)
1. [SaveOptions](https://reference.aspose.com/3d/net/aspose.threed.formats/saveoptions/)
