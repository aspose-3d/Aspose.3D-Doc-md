---
title: Su primera aplicación Aspose.3D
type: docs
weight: 30
url: /es/python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

Este tutorial explica cómo crear su primera aplicación utilizando la API sencilla de Aspose.3D. Esta aplicación simple crea un archivo 3D en una escena 3D especificada.

{{% /alert %}}

## **Cómo Crear la Aplicación**

Los siguientes pasos crean la aplicación utilizando la API de Aspose.3D:

1. Cree una instancia de la clase [Scene](https://reference.aspose.com/3d/es/python-net/aspose.threed/scene/).
1. Si tiene una licencia, entonces [aplíquela](/3d/es/python-net/licensing/).
   Si está utilizando la versión de evaluación, omita las líneas de código relacionadas con la licencia.
1. Cree un nuevo archivo 3D o abra un archivo 3D existente.
1. Acceda al contenido de la escena en el archivo 3D.
1. Genere el archivo 3D modificado.

La implementación de los pasos anteriores se muestra en los ejemplos siguientes.

### **Cómo Crear un Nuevo Documento de Escena**

El siguiente ejemplo crea un nuevo archivo de escena 3D desde cero. Primero, se crea una escena 3D y luego se guarda el archivo en formato FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}

### **Cómo Abrir un Archivo Existente**

El siguiente ejemplo abre un archivo de plantilla 3D existente llamado "document.fbx".

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
