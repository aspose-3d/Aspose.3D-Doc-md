---
title: Erkennen Sie das Format der 3D-Datei
type: docs
weight: 10
url: /de/java/detect-format-of-3d-file/
description: Aspose.3D for Java API unterstützt vor dem Öffnen die Erkennung von 3D unterstützten Formaten, da die Datei erweiterung nicht garantiert, dass der Datei inhalt geeignet ist.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API unterstützt vor dem Öffnen die Erkennung von 3D unterstützten Formaten, da die Datei erweiterung nicht garantiert, dass der Datei inhalt geeignet ist.

{{% /alert %}} 
##  **Muster für die Format programmierung erkennen**
Dieser Quellcode ver anschaulicht, wie Sie das Dateiformat erkennen (mit dem Datei pfad oder-stream) und die Erweiterung überprüfen.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// detect format of 3D file
FileFormat inputFormat = FileFormat.detect(MyDir + "document.fbx");
// display the file format
System.out.println("File Format: " + inputFormat.toString());
{{< /highlight >}}




