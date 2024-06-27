---
title: Guardar 3D escena como HTML en C#
linktitle: Guardar 3D Escena como HTML
type: docs
weight: 90
url: /es/net/save-3d-scene-as-html/
---
##  **Descripción general**

Este artículo explica cómo puede convertir archivos 3D a HTML después de [Cargándolos en objeto de escena](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) usando C# y cubre una amplia gama de temas (considerando [Formatos de archivo compatibles](https://docs.aspose.com/3d/net/supported-file-formats/)).

- Convierta 3DS a HTML usando C#
- Convierte FBX a HTML en C#
- Convierte STL a HTML en C#
- Convierte U3D a HTML en C#
- Convierte OBJ a HTML en C#


{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,9 o superior.

{{% /alert %}} 
##  **Guardar 3D Escena como HTML**
Aspose.3D for .NET proporciona la clase `Html5SaveOptions` para guardar una escena 3D guardada como HTML. Cuando exporte la escena en un archivo HTML5, API exportará tres archivos, un archivo `HTML`, un archivo Aspose3DWeb (*.* a3dw **) y un archivo `JavaScript` representado. Para exportar sólo el archivo a3dw, puede especificar Aspose3DWeb como el tipo de exportación y reutilizar el archivo JavaScript dentro de su propia página HTML. El siguiente fragmento de código C# muestra cómo guardar una escena 3D como HTML.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

Debido a los límites de seguridad del navegador, el archivo HTML exportado no se puede abrir directamente, debe abrirlo a través de un servidor web, si tiene python3 instalado, puede iniciar el servidor web en la línea de comandos en el directorio exportado

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Entonces ábrelo<http://localhost:8000/test.html>... El renderizador web utiliza WebGL2, usted puede utilizar<https://get.webgl.org/webgl2/>Para comprobar si su navegador es compatible o no.


