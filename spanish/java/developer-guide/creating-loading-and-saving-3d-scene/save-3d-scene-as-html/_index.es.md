---
title: Guardar 3D Escena como HTML
type: docs
weight: 70
url: /es/java/save-3d-scene-as-html/
description: Aspose.3D for Java proporciona la clase ** HtmlSaveOptions ** para guardar una escena 3D como HTML.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,9 o superior.

{{% /alert %}} 
#  **Guardar 3D Escena como HTML**
Aspose.3D for Java proporciona la clase `HtmlSaveOptions` para guardar una escena 3D guardada como HTML. Cuando exporte la escena en un archivo HTML5, API exportará tres archivos, un archivo `HTML`, un archivo Aspose3DWeb (*.* a3dw **) y un archivo `JavaScript` representado. Para exportar sólo el archivo a3dw, puede especificar Aspose3DWeb como el tipo de exportación y reutilizar el archivo JavaScript dentro de su propia página HTML. El siguiente fragmento de código muestra cómo guardar una escena 3D como HTML.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-html5SaveOption.java" >}}

{{% alert color="primary" %}} 

Debido a los límites de seguridad del navegador, el archivo HTML exportado no se puede abrir directamente, debe abrirlo a través de un servidor web, si tiene instalado python3, puede iniciar el servidor web en la línea de comandos en el directorio exportado

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Entonces ábrelo<http://localhost:8000/test.html>... El renderizador web utiliza WebGL2, usted puede utilizar<https://get.webgl.org/webgl2/>Para comprobar si su navegador es compatible o no.


