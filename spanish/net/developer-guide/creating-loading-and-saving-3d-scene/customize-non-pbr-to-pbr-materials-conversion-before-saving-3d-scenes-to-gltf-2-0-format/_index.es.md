---
title: Personalizar la conversión de materiales no PBR a PBR antes de guardar las escenas 3D al formato GLTF 2,0 en C#
linktitle: Personalizar la conversión de materiales no PBR a PBR antes de guardar las escenas 3D en formato GLTF 2,0
type: docs
weight: 70
url: /es/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La clase Escena del Aspose.3D API representa una escena 3D. Los desarrolladores ya pueden construir una escena 3D agregando varias entidades. GLTF 2,0 solo admite materiales PBR (Rendering Físicamente Based), Aspose.3D API convierte internamente materiales que no son PBR en materiales PBR antes de exportarlos a GLTF 2,0.
---
{{% alert color="primary" %}} 

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) del Aspose.3D API representa una escena 3D. Los desarrolladores ya pueden construir una escena 3D agregando varias entidades. GLTF 2,0 solo admite materiales PBR (Rendering Físicamente Based), Aspose.3D API convierte internamente materiales que no son PBR en materiales PBR antes de exportar a GLTF 2,0 (los materiales en la escena permanecerán sin cambios durante la exportación), y los desarrolladores pueden proporcionar una función de conversión personalizada para anular el comportamiento predeterminado.

{{% /alert %}} 
## **Conversión de material no PBR a PBR**
Este ejemplo de código C# demuestra cómo convertir material a material PBR y luego guarda la escena 3D en el formato GLTF con la manipulación y conversión de archivos C# 3D API:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = delegate(Material material)

{

    PhongMaterial m = (PhongMaterial) material;

    return new PbrMaterial() {Albedo = new Vector3(m.DiffuseColor.x, m.DiffuseColor.y, m.DiffuseColor.z)};

};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}
