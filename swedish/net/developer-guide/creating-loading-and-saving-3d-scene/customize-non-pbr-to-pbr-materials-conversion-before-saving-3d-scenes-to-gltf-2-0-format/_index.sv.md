---
title: Anpassa icke-PBR till PBR material konvertering innan Spara 3D Scener till GLTF 2.0 Format i GLTF C#
linktitle: Anpassa icke-PBR till PBR material konvertering innan Spara 3D Scener till GLTF 2.0 Format
type: docs
weight: 70
url: /sv/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Scenklassen av Aspose.3D API representerar en 3D scen. Utvecklare kan redan bygga en 3D scen genom att lägga till olika enheter. GLTF 2.0 stöder endast PBR-material (Fysiskt baserad rendering). Aspose.3D API internt omvandlar icke-PBR-material till PBR-material före export till GLTF 2,0 ..
---
{{% alert color="primary" %}} 

Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) Aspose.3D API representerar en 3D scen. Utvecklare kan redan bygga en 3D scen genom att lägga till olika enheter. GLTF 2.0 stöder endast PBR-material (Fysiskt baserad rendering). Aspose.3D API internt omvandlar icke-PBR-material till PBR-material före export till GLTF 2,0 (materialet i scenen kommer att förbli oförändrat under exporten), och utvecklarna kan ge anpassad konvertera funktion för att åsidosätta standardben Beteende.

{{% /alert %}} 
## **Omvandling av material som inte omfattas av PBR till PBR**
Detta exempel C# kod visar hur man konverterar material till PBR-material, och sparar sedan 3D scen i GLTF format med C# 3D filhantering och omvandling API:

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
