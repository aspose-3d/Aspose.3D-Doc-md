---
title: Ihre erste Aspose.3D Bewerbung
type: docs
weight: 30
url: /de/java/your-first-aspose-3d-application/
description: Erstellen, bearbeiten und speichern Sie Ihre erste 3D-Datei in allen unterstützten Formaten mit Aspose.3D for Java, um ihre Einfachheit und Leistung in Java zu erleben.
keywords: Java , Aspose.3D for Java , The first application using Aspose.3D for Java, The first program via Aspose.3D for Java.
---
{{% alert color="primary" %}}

In diesem Tutorial wird erläutert, wie Sie Ihre erste Anwendung mit den einfachen Aspose.3D von API erstellen. Diese einfache Anwendung erstellt eine 3D-Datei in einer angegebenen 3D-Szene.

{{% /alert %}}

##  **So erstellen Sie die Anwendung**

Die folgenden Schritte erstellen die Anwendung mit den Aspose.3D API:

1. Erstellen Sie eine Instanz der [Szene](https://reference.aspose.com/3d/java/com.aspose.threed/scene/)-Klasse.
1. Wenn Sie eine Lizenz haben, dann [Wenden Sie es an](/3d/de/java/licensing/).
Wenn Sie die Bewertungs version verwenden, überspringen Sie die lizenzierten Code zeilen.
1. Erstellen Sie eine neue 3D-Datei oder öffnen Sie eine vorhandene 3D-Datei.
1. Greifen Sie auf den Inhalt der Szene in der Datei 3D zu.
1. Generieren Sie die modifizierte 3D-Datei.

Die Umsetzung der obigen Schritte wird in den folgenden Beispielen gezeigt.

###  **So erstellen Sie ein neues Szenen dokument**

Im folgenden Beispiel wird eine neue 3D-Szenen datei von Grund auf erstellt. Erstellen Sie zunächst eine 3D-Szene und speichern Sie die Datei dann im FBX-Format.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}

###  **So öffnen Sie eine bestehende Datei**

Das folgende Beispiel öffnet eine vorhandene 3D-Vorlagen datei mit dem Namen "document.fbx" und speichert dann die 3D-Szene oder das Dokument in einem Stream in verschiedenen unterstützten 3D-Formaten.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load a 3D document into Aspose.3D
Scene scene = new Scene();
// Open an existing 3D scene
scene.open(MyDir + "document.fbx");
// Save Scene to a stream
try (MemoryStream dstStream = new MemoryStream()) {
    scene.save(dstStream, FileFormat.FBX7500ASCII);
}
// Save Scene to a local path
scene.save(MyDir + "output_out.fbx", FileFormat.FBX7500ASCII);
{{< /highlight >}}
