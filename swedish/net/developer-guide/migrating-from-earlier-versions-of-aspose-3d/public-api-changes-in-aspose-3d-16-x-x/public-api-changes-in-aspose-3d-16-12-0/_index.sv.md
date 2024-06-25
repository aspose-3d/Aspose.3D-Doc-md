---
title: Offentlig API Ändrar i Aspose.3D 16.12.0
type: docs
weight: 10
url: /sv/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Innehåll**

- [Adds Aspose.ThreeD.Metered Class](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [Importing DXF Files](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar i Aspose. 3D API från version 16.11. 0 till 16.12. 0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose. 3D.

{{% /alert %}} 
###  **Lägger till Aspose.ThreeD.Meterad klass**
Ett sätt att applicera en mäter licens.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
###  **Importerar DXF filer**
Genom att använda den senaste versionen (16.12.0) eller högre, kan utvecklare importera DXF-filer. Posten DXF-formatet läggs till för lastning.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
