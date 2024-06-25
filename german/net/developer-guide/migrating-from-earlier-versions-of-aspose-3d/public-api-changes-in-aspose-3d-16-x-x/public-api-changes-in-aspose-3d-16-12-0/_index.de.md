---
title: Öffentliche API Änderungen in Aspose.3D 16.12.0
type: docs
weight: 10
url: /de/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Inhalts übersicht**

- [Fügt Aspose hinzu. ThreeD. Gezählte Klasse](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [DXF Dateien importieren](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 16.11.0 bis 16.12.0, die für Modul-/Anwendungs entwickler von Interesse sein könnten. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
###  **Fügt Aspose hinzu. ThreeD. Gezählte Klasse**
Eine Möglichkeit, eine gemetzte Lizenz anzuwenden.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
###  **DXF Dateien importieren**
Mit der aktuellen Version (16.12.0) oder höher können Entwickler DXF-Dateien importieren. Der DXF-Format eintrag wird zum Laden hinzugefügt.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
