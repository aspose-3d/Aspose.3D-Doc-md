---
title: Guardar 3D Escena como HTML en C#
linktitle: Guardar 3D Escena como HTML
type: docs
weight: 90
url: /es/net/save-3d-scene-as-html/
---
## **Visión de conjunto**

Este artículo explica cómo puede convertir archivos 3D a HTML después[Cargándolos en objeto de escena](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/)Utilizando C# y cubre una amplia gama de temas (considerando[Formatos de archivo compatibles](https://docs.aspose.com/3d/net/supported-file-formats/)) P. ej.

- Convertir 3DS a HTML usando C#
- Convertir FBX a HTML en C#
- Convertir STL a HTML en C#
- Convertir U3D a HTML en C#
- Convertir OBJ a HTML en C#


{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,9 o superior.

{{% /alert %}} 
## **Guardar 3D Escena como HTML**
Aspose.3D for .NET proporciona la clase `Html5SaveOptions` para guardar una escena de guardado 3D como HTML. Al exportar la escena al archivo HTML5, API exportará tres archivos, un archivo `HTML`, un archivo DWeb Aspose3 (*.**A3dw**) Y un archivo 'JavaScript' renderizado. Para exportar el archivo a3dw solamente, usted puede especificar el DWeb Aspose3 como el tipo de la exportación, y reutilizar el archivo de JavaScript dentro de su página HTML. El siguiente fragmento de código C# muestra cómo guardar una escena 3D como HTML.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

Debido a los límites de seguridad del navegador, el archivo exportado HTML no se puede abrir directamente, debe abrirlo a través de un servidor web, si tiene python3 instalado, puede iniciar el servidor web en la línea de comandos en el directorio exportado

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Entonces ábrelo<http://localhost:8000/test.html>... El renderizador web utiliza WebGL2, usted puede utilizar<https://get.webgl.org/webgl2/>Para comprobar si su navegador es compatible o no.


