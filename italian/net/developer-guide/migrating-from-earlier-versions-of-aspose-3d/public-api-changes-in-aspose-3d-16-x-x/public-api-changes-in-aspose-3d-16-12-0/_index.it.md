---
title: Variazioni pubbliche di API in Aspose.3D 16.12.0
type: docs
weight: 10
url: /it/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Contenuto sommario**

- [Aggiunge Aspose.ThreeD. Classe misurata](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [Importazione di file DXF](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche a Aspose.3D API dalla versione 16.11.0 alla 16.12.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.3D.

{{% /alert %}} 
###  **Aggiunge Aspose.ThreeD. Classe misurata**
Un modo per applicare una licenza a pagamento.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
###  **Importazione di file DXF**
Utilizzando la versione recente (16.12.0) o superiore, gli sviluppatori possono importare file DXF. La voce del formato DXF viene aggiunta ai fini del caricamento.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
