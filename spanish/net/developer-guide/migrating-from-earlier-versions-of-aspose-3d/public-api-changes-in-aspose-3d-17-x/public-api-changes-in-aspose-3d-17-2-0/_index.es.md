---
title: Público API Cambios en Aspose.3D 17.2.0
type: docs
weight: 10
url: /es/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Resumen de contenidos**

- [Importación de archivos DirectX X](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Agrega la clase Aspose.ThreeD.Formats.X.XLoadOptions](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 17.1.0 to 17.2.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
####  **Importación de archivos DirectX X**
Usando la versión reciente (17,02) o superior, los desarrolladores pueden importar archivos X. Las entradas de formato XBinary y XText se agregan para importar archivos binarios y ASCII X.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
####  **Agrega la clase Aspose.ThreeD.Formats.X.XLoadOptions**
Hemos agregado la clase XLoadOptions. Ayuda a importar archivos X en Aspose.3D API.

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
