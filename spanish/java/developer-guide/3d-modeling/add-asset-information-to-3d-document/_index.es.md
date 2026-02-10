---
title: Agregar información de activos al documento 3D
type: docs
weight: 10
url: /es/java/add-asset-information-to-3d-document/
description: Los metadatos son información estructurada que describe, explica, localiza o facilita la recuperación, el uso o la gestión de un recurso de información. Aspose.3D for Java API tiene soporte para definir metadatos para la escena.
---
##  **Agregar información de activos al documento 3D**
Los metadatos son información estructurada que describe, explica, localiza o facilita la recuperación, el uso o la gestión de un recurso de información. Aspose.3D for Java API tiene soporte para definir metadatos para la escena.
###  **Definir metadatos para la escena**
3D muestra producir cantidades masivas de metadatos e información de imagen. Los metadatos son un activo y parte del programa.

1. Inicialice una escena 3D usando la clase `Scene`.
1. Establecer el nombre de la aplicación/herramienta.
1. Establezca el nombre del proveedor de la aplicación/herramienta.
1. Establecer unidad de medición.
1. Establezca el factor de escala de la unidad de medición.
1. Guarde la escena 3D en el formato de archivo compatible.

En este ejemplo, asumimos que la escena es creada por una herramienta CAD llamada “Egypt” y está diseñada por “Manualdesk”:

{{< highlight "java" >}}
// Initialize a 3D scene
Scene scene = new Scene();
// Set application/tool name
scene.getAssetInfo().setApplicationName("Egypt");
// Set application/tool vendor name
scene.getAssetInfo().setApplicationVendor("Manualdesk");
// We use ancient egyption measurement unit Pole
scene.getAssetInfo().setUnitName("pole");
// One Pole equals to 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("InformationToScene.fbx");
// Save scene to 3D supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
