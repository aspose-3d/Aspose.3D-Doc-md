---
title: Offentlig API Förändringar Aspose.3D 17.2.0
type: docs
weight: 10
url: /sv/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Innehåll**

- [Importera DirectX X-filer](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Lägger till Aspose.ThreeD. Format.X.X.XLoadOptions ClassName](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

Detta dokument beskriver ändringar i Aspose.3D API från version 17.1. 0 till 17.2.0, som kan vara av intresse för modul/applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteende bakom kulisserna i Aspose.3D.

{{% /alert %}} 
#### **Importera DirectX X-filer**
Med den senaste versionen (17.02) eller högre kan utvecklare importera X-filer. Posterna XBinary och XText-formatet läggs till att importera binära och ASCII X-filer.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
#### **Lägger till Aspose.ThreeD. Format.X.X.XLoadOptions ClassName**
Vi har lagt till XLoadOptions klass. Det hjälper till att importera X-filer till Aspose.3D API.

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
