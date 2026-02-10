---
title: Ihre erste Aspose.3D-Anwendung
type: docs
weight: 30
url: /de/python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

Dieses Tutorial erklärt, wie Sie Ihre erste Anwendung mit der einfachen API von Aspose.3D erstellen. Diese einfache Anwendung erstellt eine 3D-Datei in einer angegebenen 3D-Szene.

{{% /alert %}}

## **So erstellen Sie die Anwendung**

Die folgenden Schritte erzeugen die Anwendung mithilfe der Aspose.3D-API:

1. Erstellen Sie eine Instanz der [Scene](https://reference.aspose.com/3d/python-net/aspose.threed/scene/)-Klasse.
1. Falls Sie eine Lizenz haben, [wenden Sie diese an](/3d/python-net/licensing/).  
   Wenn Sie die Evaluationsversion verwenden, überspringen Sie die lizenzbezogenen Codezeilen.
1. Erstellen Sie eine neue 3D-Datei oder öffnen Sie eine vorhandene 3D-Datei.
1. Greifen Sie auf den Szeneninhalt in der 3D-Datei zu.
1. Generieren Sie die modifizierte 3D-Datei.

Die Umsetzung der oben genannten Schritte wird in den folgenden Beispielen demonstriert.

### **So erstellen Sie ein neues Szenendokument**

Das folgende Beispiel erstellt eine neue 3D-Szenendatei von Grund auf. Zunächst wird eine 3D-Szene erstellt und anschließend die Datei im FBX-Format gespeichert.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.
# Create an object of the Scene class
scene = a3d.Scene()
# Save 3D scene document
scene.Save("document.fbx", a3d.FileFormat.FBX7500ASCII)

{{< /highlight >}}

### **So öffnen Sie eine vorhandene Datei**

Das folgende Beispiel öffnet eine vorhandene 3D-Vorlagendatei mit dem Namen „document.fbx“.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.

# Initialize a Scene class object
scene = Scene()
# Load an existing 3D document
scene.open("document.fbx")


{{< /highlight >}}
