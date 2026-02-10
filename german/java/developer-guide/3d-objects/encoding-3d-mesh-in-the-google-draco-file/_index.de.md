---
title: Codierung von 3D Mesh in der Google Draco-Datei
type: docs
weight: 30
url: /de/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API unterstützt den Import von 3D-Modell, das Abrufen von Mesh und das Codieren von Mesh in der Google Draco-Datei.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API unterstützt den Import von 3D-Modell, das Abrufen von Mesh und das Codieren von Mesh in der Google Draco-Datei. Entwickler können auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor sie ein Netz codieren.

{{% /alert %}} 
##  **3D Mesh und Codierung in Google Draco Datei abrufen**
Die von der `DracoFormat`-Klasse offen gelegte Codierung methode kann verwendet werden, um ein 3D-Netz in der Google Draco-Datei zu codieren. Als Parameter werden Objekte im Wert von `Mesh` und `DracoSaveOptions` benötigt. Mit den Speicher optionen für Draco können Entwickler auch die Position, die Textur koordinaten, die Farbe und die normalen Bits sowie die Kom primi erungs stufe angeben, bevor ein Netz codiert wird.
###  **Programmier probe**
In diesem Code beispiel wird Mesh of Sphere abgerufen und nach Angabe einer Kom primi erungs stufe in der Datei Google Draco codiert.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Create a sphere
Sphere sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
DracoSaveOptions opt = new DracoSaveOptions();
opt.setCompressionLevel(DracoCompressionLevel.OPTIMAL);
byte[] b = FileFormat.DRACO.encode(sphere.toMesh(), opt);
// Save the raw bytes to file
Files.write(Paths.get(MyDir, "SphereMeshtoDRC_Out.drc"), b);
{{< /highlight >}}
