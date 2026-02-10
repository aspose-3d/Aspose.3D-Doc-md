---
title: Speichern Sie ein 3D-Dokument in verschiedenen 3D-Formaten mit C#
linktitle: Sparen Sie ein 3D-Dokument
type: docs
weight: 20
url: /de/net/save-a-3d-document/
description: Die Scene-Klasse der Aspose.3D API stellt ein 3D-Dokument dar, und Entwickler können sein Objekt in jedem unterstützten Dateiformat speichern.
---
##  **Übersicht**
Der Artikel erklärt, wie Sie 3D-Dokumente in verschiedenen Formaten mit einer C# 3D-Dokument verarbeitung bibliothek speichern können, einschl ießlich

- Sparen Sie ein 3D-Dokument im FBX-Format mit C# - AutoDesk
- Sparen Sie ein 3D-Dokument im DAE-Format mit C# - Collada
- Sparen Sie ein 3D-Dokument im 3DS-Format mit C# - Discreet 3D Studio
- Sparen Sie ein 3D-Dokument im DRC-Format mit C# - Google Draco

{{% alert color="primary" %}} 

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API stellt ein 3D-Dokument dar, und Entwickler können sein Objekt in jedem unterstützten Dateiformat speichern. Um eine 3D-Szene zu speichern, verwenden Sie einfach die [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-Methode. Sie akzeptiert einen Dateinamen mit vollständigem Pfad oder ein Dateistream-Objekt. Aspose.3D API bietet einen weiteren `FileFormat` Parameter, um das Ausgabe dateiformat anzugeben.

{{% /alert %}} 

##  **Sparen Sie eine 3D-Szene in den unterstützten 3D-Formaten**

Das unten stehende Code-Beispiel für C# zeigt, wie Sie eine 3D-Szene oder ein Dokument in einem Stream in verschiedenen unterstützten 3D-Formaten speichern.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
