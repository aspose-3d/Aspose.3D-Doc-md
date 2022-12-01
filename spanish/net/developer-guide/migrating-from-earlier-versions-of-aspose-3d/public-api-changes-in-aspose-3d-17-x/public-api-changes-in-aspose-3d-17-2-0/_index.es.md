---
title: Público API Cambios en Aspose.3D 17.2.0
type: docs
weight: 10
url: /es/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Resumen de contenidos**

- [Importación de archivos DirectX X](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Añade Aspose.ThreeD. Formatos. X. Clase XLoadOptions](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.3D API de la versión 17.1.0 a 17.2.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.3D.

{{% /alert %}} 
#### **Importación de archivos DirectX X**
Usando la versión reciente (17,02) o superior, los desarrolladores pueden importar archivos X. Las entradas de formato XBinary y XText se agregan para importar archivos binarios y ASCII X.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
#### **Añade Aspose.ThreeD. Formatos. X. Clase XLoadOptions**
Hemos añadido XLoadOptions clase. Ayuda a importar archivos X en Aspose.3D API.

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
