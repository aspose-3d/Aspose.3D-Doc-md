---
title: Anpassa icke-PBR- konvertering till PBR- material innan du sparar 3D Scener till GLTF 2. 0 Format i C#
linktitle: Anpassa icke-PBR- konvertering till PBR- material innan du sparar 3D Scener till GLTF 2. 0 Format
type: docs
weight: 70
url: /sv/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Scenklassen för Aspose.3D API representerar en 3D scen. Utvecklare kan redan bygga en 3D scen genom att lägga till olika enheter. GLTF 2.0 stöder endast PBR-material (Fysiskt baserad rendering), Aspose. 3D API konverterar internt icke-PBR-material till PBR-material innan export till GLTF 2.0.
---
{{% alert color="primary" %}} 

Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) för Aspose.3D API representerar en 3D scen. Utvecklare kan redan bygga en 3D scen genom att lägga till olika enheter. GLTF 2.0 stöder endast PBR-material (Fysiskt baserad rendering), Aspose. 3D API omvandlar internt icke-PBR-material till PBR-material innan exporten till GLTF 2.0 (materialet i Scenen kommer att förbli oförändrad under exporten), och utvecklarna kan tillhandahålla anpassad konverteringsfunktion för att åsidosätta standardbeteendet.

{{% /alert %}} 
##  **Omvandling av material som inte omfattas av PBR till PBR**
Det här C#-kodexemplet visar hur man konverterar material till PBR-material, och sparar sedan 3D scenen i GLTF-formatet med C# 3D filmanipulering och konvertering API:

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


##  **Resurser**

1. [Online Tutorial](https://products.aspose.com/3d/tutorial/use-phong-material-to-pbr-material/)
