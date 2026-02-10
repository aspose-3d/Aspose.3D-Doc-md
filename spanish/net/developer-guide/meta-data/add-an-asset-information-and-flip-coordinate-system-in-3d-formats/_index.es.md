---
title: Adición de información de activos a una escena
type: docs
weight: 10
url: /es/net/add-an-asset-information-to-scene
description: Los metadatos son información estructurada que describe, explica, localiza o facilita la recuperación, el uso o la gestión de un recurso de información. Aspose.3D for .NET API permite a los desarrolladores definir un Metadato para la escena.
---
##  **Agregar información de activos a la escena 3D**
Los metadatos son información estructurada que describe, explica, localiza o facilita la recuperación, el uso o la gestión de un recurso de información. Aspose.3D for .NET API permite a los desarrolladores definir un Metadato para la escena.
###  **Definir metadatos para la escena**
3D muestra producir cantidades masivas de metadatos e información de imagen. Los metadatos son un activo y parte del programa.

1. Inicialice una escena 3D usando la clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene).
1. Establecer el nombre de la aplicación/herramienta.
1. Establezca el nombre del proveedor de la aplicación/herramienta.
1. Establecer unidad de medición.
1. Establezca el factor de escala de la unidad de medición.
1. Guarde la escena 3D en el formato de archivo compatible.

En este ejemplo, asumimos que la escena es creada por una herramienta CAD llamada “Egypt” y está diseñada por “Manualdesk”:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a 3D scene
Scene scene = new Scene();

// Set application/tool name
scene.AssetInfo.ApplicationName = "Egypt";

// Set application/tool vendor name
scene.AssetInfo.ApplicationVendor = "Manualdesk";

// We use ancient egyption measurement unit Pole
scene.AssetInfo.UnitName = "pole";

// One Pole equals to 60cm
scene.AssetInfo.UnitScaleFactor = 0.6;

// Save scene to 3D supported file formats
scene.Save("InformationToScene.fbx");

{{< /highlight >}}
