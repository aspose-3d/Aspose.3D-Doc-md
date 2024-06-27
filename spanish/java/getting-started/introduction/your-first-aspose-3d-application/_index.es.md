---
title: Su primera aplicación Aspose.3D
type: docs
weight: 30
url: /es/java/your-first-aspose-3d-application/
description: Cree, edite y guarde su primer archivo 3D en cualquier formato compatible con Aspose.3D for Java para experimentar su simplicidad y potencia en Java.
keywords: Java , Aspose.3D for Java , The first application using Aspose.3D for Java, The first program via Aspose.3D for Java.
---
{{% alert color="primary" %}}

Este tutorial explica cómo crear su primera aplicación usando Aspose.3D's simple API. Esta sencilla aplicación crea un archivo 3D en una escena 3D especificada.

{{% /alert %}}

##  **Cómo crear la aplicación**

Los pasos siguientes crean la aplicación usando el Aspose.3D API:

1. Crear una instancia de la clase [Escena](https://reference.aspose.com/3d/java/com.aspose.threed/scene/).
1. Si tiene una licencia, entonces [Aplicarlo](/3d/es/java/licensing/).
Si está utilizando la versión de evaluación, omita las líneas de código relacionadas con la licencia.
1. Cree un nuevo archivo 3D o abra un archivo 3D existente.
1. Acceda al contenido de la escena en el archivo 3D.
1. Genere el archivo 3D modificado.

La implementación de las etapas anteriores se demuestra en los ejemplos a continuación.

###  **Cómo crear un nuevo documento de escena**

El ejemplo siguiente crea un nuevo archivo de escena 3D desde cero. Primero, cree una escena 3D y luego guarde el archivo en formato FBX.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-CreateEmpty3DDocument.java" >}}

###  **Cómo abrir un archivo existente**

El siguiente ejemplo abre un archivo de plantilla 3D existente denominado "document.fbx" y, a continuación, guarda la escena o el documento 3D en una secuencia en varios formatos 3D compatibles.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Save3DScene.java" >}}
