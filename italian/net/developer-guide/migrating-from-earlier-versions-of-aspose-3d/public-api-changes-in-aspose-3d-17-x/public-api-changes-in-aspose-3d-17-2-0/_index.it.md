---
title: Pubblico API Modifiche nel Aspose.3D 17.2.0
type: docs
weight: 10
url: /it/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Contenuto sommario**

- [Importazione di file DirectX X](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Aggiunge Aspose.ThreeD.Formats.X.XLoadOptions Class](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.3D API dalla versione 17.1.0 alla 17.2.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte nello Aspose.3D.

{{% /alert %}} 
#### **Importazione di file DirectX X**
Utilizzando la versione recente (17.02) o superiore, gli sviluppatori possono importare file X. Le voci in formato XBinary e XText vengono aggiunte per importare file binari e ASCII X.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
#### **Aggiunge Aspose.ThreeD.Formats.X.XLoadOptions Class**
Abbiamo aggiunto XLoadOptions class. Aiuta a importare file X in Aspose.3D API.

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
