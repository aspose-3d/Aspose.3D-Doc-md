---
title: Personalizza la conversione da non PBR a PBR materiali prima di salvare 3D scene in GLTF formato 2.0 in C#
linktitle: Personalizza la conversione dei materiali da PBR a PBR prima di salvare 3D scene in GLTF 2.0 Formato
type: docs
weight: 70
url: /it/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scena di Aspose.3D API rappresenta una scena di 3D. Gli sviluppatori possono già creare una scena 3D aggiungendo varie entità. GLTF 2.0 supporta solo materiali PBR (rendering basato sulla fisica), Aspose.3D API converte internamente materiali non PBR in materiali PBR prima di esportare in GLTF 2.0.
---
{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) di Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono già creare una scena 3D aggiungendo varie entità. GLTF 2.0 supporta solo materiali PBR (Rendering basato sulla fisica), Aspose.3D API converte internamente materiali non PBR in materiali PBR prima di esportare in GLTF 2.0 (i materiali nella scena rimarranno invariati durante l'esportazione) e gli sviluppatori possono fornire la funzione di conversione personalizzata per sovrascrivere il comportamento predefinito.

{{% /alert %}} 
##  **Conversione del materiale da non PBR a PBR**
Questo esempio di codice C# mostra come convertire il materiale in materiale PBR, quindi salva la scena 3D nel formato GLTF con C# 3D manipolazione di file e conversione API:

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


##  **Risorse**

1. [Tutorial online](https://products.aspose.com/3d/tutorial/use-phong-material-to-pbr-material/)
