---
title: Codificación 3D Malla en el archivo Google Draco
type: docs
weight: 60
url: /es/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API permite a los desarrolladores importar un modelo 3D y luego codificar mallas en los archivos Google Draco. Los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API permite a los desarrolladores[Importar un modelo 3D](/3d/es/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), Y luego codifique las mallas en los archivos Google Draco. Los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.

{{% /alert %}}
## **Recuperar una malla 3D y codificar en archivo Google Draco**
El método `Encode` expuesto por la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) se puede utilizar para codificar una malla 3D en el archivo Google Draco. Toma como parámetros los objetos [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) y [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions). Usando las opciones de guardado Draco, los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.
### **Muestra de programación**
Este ejemplo de código recupera un `Mesh` de `Sphere` y, a continuación, codifique en el archivo Google Draco después de especificar un nivel de compresión.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.cs" >}}
