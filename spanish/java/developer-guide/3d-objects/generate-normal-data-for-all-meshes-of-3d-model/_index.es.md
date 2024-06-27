---
title: Generar datos normales para todas las mallas del modelo 3D
type: docs
weight: 40
url: /es/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API tiene soporte para generar datos normales para todas las mallas del modelo 3D (sin los datos normales).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API tiene soporte para generar datos normales para todas las mallas del modelo 3D (sin los datos normales).

{{% /alert %}} 
##  **Generar datos normales para todas las mallas del modelo 3DS**
El método generateNormal expuesto por la clase `PolygonModifier` se puede usar para generar datos normales para todas las mallas en un archivo 3DS. Si el elemento VertexElementSmoothingGroup se definió en la malla, los datos normales generados serán suavizados por VertexElementSmoothingGroup.
###  **Muestra de programación**
Este ejemplo de código carga un archivo 3DS, visita todos los nodos y crea datos normales para todas las mallas.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-GenerateDataForMeshes.java" >}}
