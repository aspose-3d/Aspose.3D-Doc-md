---
title: Personalizza la conversione dei materiali da PBR a PBR prima di salvare le scene da 3D al formato GLTF 2.0 in C#
linktitle: Personalizzare la conversione dei materiali da PBR a PBR prima di salvare le scene da 3D al formato 2.0 GLTF
type: docs
weight: 70
url: /it/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scena dello Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono già costruire una scena 3D aggiungendo varie entità. GLTF 2.0 supporta solo materiali PBR (rendering basato sulla fisica), Aspose.3D API converte internamente materiali non PBR in materiali PBR prima di esportare in GLTF 2.0.
---
{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) dello Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono già costruire una scena 3D aggiungendo varie entità. GLTF 2.0 supporta solo materiali PBR (Physically Based Rendering), Aspose.3D API converte internamente materiali non PBR in materiali PBR prima di esportare in GLTF 2.0 (i materiali nella scena rimarranno invariati durante l'esportazione) e gli sviluppatori possono fornire funzione di conversione personalizzata per sovrascrivere il comportamento predefinito.

{{% /alert %}} 
## **Conversione del materiale da non PBR a PBR**
Questo esempio di codice C# dimostra come convertire il materiale in materiale PBR, quindi salvare la scena 3D nel formato GLTF con C# manipolazione e conversione di file 3D:

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
