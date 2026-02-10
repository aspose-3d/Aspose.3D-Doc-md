---
title: Sparen Sie ein 3D-Dokument
type: docs
weight: 20
url: /de/python-net/save-a-3d-document/
description: Die Scene-Klasse der Aspose.3D API stellt ein 3D-Dokument dar, und Entwickler können sein Objekt in jedem unterstützten Dateiformat speichern.
---
{{% alert color="primary" %}} 

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API stellt ein 3D-Dokument dar, und Entwickler können sein Objekt in jedem unterstützten Dateiformat speichern. Um eine 3D-Szene zu speichern, verwenden Sie einfach die [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-Methode. Sie akzeptiert einen Dateinamen mit vollständigem Pfad oder ein Dateistream-Objekt. Aspose.3D API bietet einen weiteren `FileFormat` Parameter, um das Ausgabe dateiformat anzugeben.

{{% /alert %}} 
##  **Sparen Sie eine 3D-Szene**


Das folgende Code beispiel zeigt, wie ein Dokument in einem Stream gespeichert wird.

{{< highlight "python" >}}
import aspose.threed as a3d
import io
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
# Load a 3D document into Aspose.3D
scene = a3d.Scene.from_file("document.fbx")

# Save Scene to a stream
dstStream = io.BytesIO()
scene.save(dstStream, a3d.FileFormat.FBX7500ASCII);

{{< /highlight >}}
