---
title: Exportar archivos de textura mientras se guarda la escena 3D
type: docs
weight: 10
url: /es/net/export-texture-files-while-saving-3d-scene
description: Usando Aspose.3D for .NET, los desarrolladores pueden exportar archivos de textura al sistema de archivos mientras guardan la escena 3D.
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), When exporting a scene to files, it's often necessary to export the textures, whether embedded or external, to the same directory. Aspose.3D for .NET facilitates this process, ensuring that all textures are properly managed and stored along with the exported scene. This guide demonstrates how to achieve this.

{{% /alert %}}

Para exportar una escena y asegurarse de que todas las texturas asociadas se guardan en el mismo directorio, siga estos pasos:


{{% highlight "csharp" %}}

Scene scene = Scene.FromFile(@"BoomBox.glb");
var opt = new ObjSaveOptions();
opt.ExportTextures = true;
scene.Save(@"D:\tmp\boombox\output.obj", opt);

{{% /highlight %}}


Todos los objetos `SaveOptions` en Aspose.3D incluyen la propiedad `ExportTextures`, que simplifica el proceso de administración de texturas durante la exportación. Esta propiedad garantiza que todas las texturas, externas o incrustadas, se guardan en el directorio de salida especificado. Esta característica es compatible con varios formatos de archivo que admiten la exportación de texturas, como FBX, 3DS, OBJ, USD, GLTF y DAE.



Explicación

1. Cargar la escena: La escena se carga desde el archivo de entrada.
1. Configurar opciones de guardado: Establezca `ExportTextures` en `true`.
1. Exportar la escena: la escena se guarda en el directorio de salida con las rutas de textura actualizadas.


Al aprovechar la propiedad `ExportTextures` en `SaveOptions`, puede exportar sin problemas escenas 3D junto con sus texturas, asegurando que todos los activos necesarios estén organizados en un solo directorio. Esta característica mejora la portabilidad y la facilidad de uso de los archivos 3D en diversas plataformas y aplicaciones.

##  **Recursos**

1. [Tutorial en línea](https://products.aspose.com/3d/tutorial/)
1. [SaveOptions (Opciones de ahorro)](https://reference.aspose.com/3d/net/aspose.threed.formats/saveoptions/)
