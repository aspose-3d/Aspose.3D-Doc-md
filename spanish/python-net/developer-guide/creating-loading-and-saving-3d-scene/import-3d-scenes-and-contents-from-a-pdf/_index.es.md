---
title: Importar 3D Escenas y contenidos de un PDF
type: docs
weight: 50
url: /es/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: La clase Escena del Aspose.3D API representa una escena 3D. Los desarrolladores pueden extraer 3D escenas y contenidos de un archivo PDF.
---
{{% alert color="primary" %}}

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) del Aspose.3D API representa una escena 3D. Los desarrolladores pueden extraer 3D escenas y contenidos de un archivo PDF.

{{% /alert %}}
## **Escena abierta desde una contraseña protegida PDF**
El método `open` de la clase `Scene` permite cargar la escena 3D desde un archivo de entrada PDF. Los desarrolladores también pueden aplicar la contraseña para los archivos PDF protegidos usando la clase [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) como se muestra en este ejemplo de código:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
## **Extraer todos los contenidos en bruto 3D de un PDF**
El método `extract` de la clase [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) permite extraer el contenido de 3D de un archivo PDF. Los desarrolladores pueden recorrer el contenido y guardarlos en los archivos separados como se muestra en este ejemplo de código:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
## **Extraiga todas las escenas 3D y guárdelas en formatos compatibles 3D**
El método `extract_scene` de la clase `PdfFormat` permite extraer 3D escenas de un archivo PDF. Los desarrolladores pueden iterar a través de las escenas y guardarlas en los formatos de archivo 3D compatibles como se muestra en este ejemplo de código:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

Todos los formatos de archivo soportados 3D se enumeran en el[Descripción general del producto](/3d/es/python-net/product-overview/)Página.

{{% /alert %}}
