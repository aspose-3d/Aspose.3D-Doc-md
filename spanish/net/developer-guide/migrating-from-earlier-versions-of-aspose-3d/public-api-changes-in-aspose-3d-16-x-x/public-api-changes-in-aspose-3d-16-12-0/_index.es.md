---
title: Público API Cambios en Aspose.3D 16.12.0
type: docs
weight: 10
url: /es/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Resumen de contenidos**

- [Agrega la clase Aspose.ThreeD.Metered](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [Importación de archivos DXF](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 16.11.0 to 16.12.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Agrega la clase Aspose.ThreeD.Metered**
Una forma de aplicar una licencia con medida.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
###  **Importación de archivos DXF**
Con la versión reciente (16.12.0) o superior, los desarrolladores pueden importar archivos DXF. La entrada de formato DXF se agrega para fines de carga.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
