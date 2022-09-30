---
title: Aspose.3D for .NET 17,6 Utgivningsmeddelanden
type: docs
weight: 70
url: /sv/net/aspose-3d-for-net-17-6-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 17,6](https://www.nuget.org/packages/Aspose.3D/17.6.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-257|Exportera 3D scen till GLTF 2.0 ASCII filer|Ny funktion|
|THREEDNET-258|Exportera 3D scen till GLTF 2.0 Binära filer|Ny funktion|
|THREEDNET-264|Modeller har tangent men har inget bi-normalt visar inte korrekt|FelComment|
|THREEDNET-267|Material i Collada filer kan inte laddas korrekt.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till materialConverter medlem till Aspose.ThreeD.Formats.GLTFSparaOptions klass**
GLTF 2,0 stöder endast PBR-material, Aspose.3D kommer internt att omvandla icke-PBR-material till PBR-material innan de exporteras till GLTF 2.0 (materialet i Scenen förblir oförändrad under exporten), och användaren kan tillhandahålla anpassad konverteringsfunktion för att åsidosätta standardbeteendet.

Detta kodexempel visar hur man konverterar material till PBR material, och sedan spara 3D scen till GLTF 2.0 format:

**.NET, C#**

{{< highlight "java" >}}

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

s.Save("test.gltf", opt);

{{< /highlight >}}
### **Exempel**
Kontrollera listan över hjälpämnen som lagts till eller uppdaterats i Wiki-dokumenten Aspose.3D:

1. [Anpassa icke-PBR till PBR material konvertering innan Spara 3D Scener till GLTF 2.0 Format](/3d/sv/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/)
