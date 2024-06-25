---
title: Guardar 3D Escena como HTML
type: docs
weight: 90
url: /es/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,9 o superior.

{{% /alert %}} 
#  **Guardar 3D Escena como HTML**
Aspose.3D for Python via .NET proporciona la clase `Html5SaveOptions` para guardar una escena de 3D como HTML. Cuando exporte la escena a un archivo HTML5, API exportará tres archivos, un archivo `HTML`, un archivo Aspose3DWeb (*.* a3dw **) y un archivo `JavaScript` representado. Para exportar solo el archivo a3dw, puede especificar Aspose3DWeb como el tipo de exportación y reutilizar el archivo JavaScript dentro de su propia página HTML. El siguiente fragmento de código muestra cómo guardar una escena 3D como HTML.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-HtmlSaveOption.py" >}}

{{% alert color="primary" %}} 

Debido a los límites de seguridad del navegador, el archivo HTML exportado no se puede abrir directamente, debe abrirlo a través de un servidor web, si tiene python3 instalado, puede iniciar el servidor web en la línea de comandos en el directorio exportado

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Entonces ábrelo<http://localhost:8000/test.html>... El renderizador web utiliza WebGL2, usted puede utilizar<https://get.webgl.org/webgl2/>Para comprobar si su navegador es compatible o no.


