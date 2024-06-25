---
title: Öffentliche API Änderungen in Aspose.3D 17.2.0
type: docs
weight: 10
url: /de/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Inhalts übersicht**

- [DirectX X-Dateien importieren](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Fügt Aspose hinzu. ThreeD. Formate. X.XLoadOptions-Klasse](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 17.1.0 bis 17.2.0, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
####  **DirectX X-Dateien importieren**
Mit der aktuellen Version (17.02) oder höher können Entwickler X-Dateien importieren. Die Einträge im XBinary-und XText-Format werden hinzugefügt, um Binär-und ASCII-X-Dateien zu importieren.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
####  **Fügt Aspose hinzu. ThreeD. Formate. X.XLoadOptions-Klasse**
Wir haben die XLoad Options-Klasse hinzugefügt. Es hilft beim Importieren von X-Dateien in Aspose.3D API.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// initialize Scene class object

Scene scene = new Scene();

// initialize an object

XLoadOptions loadXOpts = new XLoadOptions();

// load X file

scene.Open( "3DX.x", loadXOpts);

{{< /highlight >}}
