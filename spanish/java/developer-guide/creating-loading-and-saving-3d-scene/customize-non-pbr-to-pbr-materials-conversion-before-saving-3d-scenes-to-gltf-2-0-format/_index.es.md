---
title: Personalizar la conversión de materiales no PBR a PBR antes de guardar escenas 3D en formato GLTF 2,0
type: docs
weight: 50
url: /es/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La clase Scene de Aspose.3D for Java API representa una escena 3D y los desarrolladores pueden construir una escena 3D agregando varias entidades.
---
{{% alert color="primary" %}} 

La clase `Scene` de Aspose.3D for Java API representa una escena 3D y los desarrolladores pueden construir una escena 3D agregando varias entidades. GLTF 2,0 solo admite materiales PBR (Physically Based Rendering), Aspose.3D API convierte internamente materiales que no son PBR en materiales PBR antes de exportar a GLTF 2,0 (los materiales en la escena permanecerán sin cambios durante la exportación), y los desarrolladores pueden proporcionar una función de conversión personalizada para anular el comportamiento predeterminado.

{{% /alert %}} 
##  **Conversión de material no PBR a PBR**
En este ejemplo de código se muestra cómo convertir material en material PBR y, a continuación, guardar la escena 3D en el formato GLTF:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
