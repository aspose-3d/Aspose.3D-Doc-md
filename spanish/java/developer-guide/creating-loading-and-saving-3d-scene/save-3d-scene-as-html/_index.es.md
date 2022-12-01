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
# **Guardar 3D Escena como HTML**
Aspose.3D for Java proporciona la clase `HtmlSaveOptions` para guardar una escena de guardado 3D como HTML. Al exportar la escena al archivo HTML5, API exportará tres archivos, un archivo `HTML`, un archivo DWeb Aspose3 (*.**A3dw**) Y un archivo 'JavaScript' renderizado. Para exportar el archivo a3dw solamente, usted puede especificar el DWeb Aspose3 como el tipo de la exportación, y reutilizar el archivo de JavaScript dentro de su página HTML. El siguiente fragmento de código muestra cómo guardar una escena 3D como HTML.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-html5SaveOption.java" >}}

{{% alert color="primary" %}} 

Debido a los límites de seguridad del navegador, el archivo exportado HTML no se puede abrir directamente, debe abrirlo a través de un servidor web, si tiene python3 instalado, puede iniciar el servidor web en la línea de comandos en el directorio exportado

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Entonces ábrelo<http://localhost:8000/test.html>... El renderizador web utiliza WebGL2, usted puede utilizar<https://get.webgl.org/webgl2/>Para comprobar si su navegador es compatible o no.


