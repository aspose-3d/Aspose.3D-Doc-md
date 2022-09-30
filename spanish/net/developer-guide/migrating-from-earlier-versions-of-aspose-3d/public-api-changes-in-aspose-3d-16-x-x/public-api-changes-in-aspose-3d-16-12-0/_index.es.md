---
title: Público API Cambios en Aspose.3D 16.12.0
type: docs
weight: 10
url: /es/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Resumen de contenidos**

- [Agrega Aspose.ThreeD. Clase medida](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [Importación de archivos DXF](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.3D API de la versión 16.11.0 a 16.12.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.3D.

{{% /alert %}} 
### **Agrega Aspose.ThreeD. Clase medida**
Una forma de aplicar una licencia con medida.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
### **Importación de archivos DXF**
Usando la versión reciente (16.12.0) o superior, los desarrolladores pueden importar archivos DXF. La entrada de formato DXF se añade con fines de carga.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
