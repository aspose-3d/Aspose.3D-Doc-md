---
title: Personalizar la conversión de materiales que no son PBR a PBR antes de guardar escenas 3D en formato GLTF 2,0 en C#
linktitle: Personalizar la conversión de materiales no PBR a PBR antes de guardar escenas 3D en formato GLTF 2,0
type: docs
weight: 70
url: /es/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La clase Scene de Aspose.3D API representa una escena 3D. Los desarrolladores ya pueden construir una escena 3D añadiendo varias entidades. GLTF 2,0 solo admite materiales de PBR (renderización basada en la física), Aspose.3D API convierte internamente materiales que no son PBR en materiales de PBR antes de exportarlos a GLTF 2,0.
---
{{% alert color="primary" %}} 

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la Aspose.3D API representa una escena 3D. Los desarrolladores ya pueden construir una escena 3D añadiendo varias entidades. GLTF 2,0 solo admite materiales PBR (Physically Based Rendering), Aspose.3D API convierte internamente materiales que no son PBR en materiales PBR antes de exportar a GLTF 2,0 (los materiales en la escena permanecerán sin cambios durante la exportación), y los desarrolladores pueden proporcionar una función de conversión personalizada para anular el comportamiento predeterminado.

{{% /alert %}} 
##  **Conversión de material no PBR a PBR**
Este ejemplo de código C# demuestra cómo convertir material en material PBR y luego guarda 3D escena en el formato GLTF con C# 3D manipulación de archivos y conversión API:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = (Material material) => {
    var pbr = PbrMaterial.FromMaterial(material);
    //customize your own PBR material here, you can get the original OBJ's material from the parameter mat.
    //to create a compatible material with obj2gltf, use following definition:
    pbr.MetallicFactor = 0;
    pbr.RoughnessFactor = 0.98;
    return pbr;
};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}


##  **Recursos**

1. [Tutorial en línea](https://products.aspose.com/3d/tutorial/use-phong-material-to-pbr-material/)
