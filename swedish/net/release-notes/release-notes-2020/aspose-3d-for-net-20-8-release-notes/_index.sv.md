---
title: Aspose.3D for .NET 20,8 Utgivning
type: docs
weight: 9
url: /sv/net/aspose-3d-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 20.8.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-698|Tillagt stöd för att importera zippade 3D-filer|
|THREEDNET-697|Fast PBR-material med spekulärt stöddes inte GLTF|
|THREEDNET-705|Tillagd FBX 6.0 importstöd|
|THREEDNET-706|Tillagd FBX 6.1 importstöd|
|THREEDNET-707|Tillagd FBX 7.0/7.1 importstöd|
|THREEDNET-708|Egenskaper som inte stöds i FBX stöds inte.|
|THREEDNET-703|Lagt FBX 7.7 importstöd|
|THREEDNET-704|OBJ fil med negativt element index stöds inte.|
|THREEDNET-700|Fast Aspose.3D hänger vid tolkning ofullständig PDF fil.|
|THREEDNET-699|Fast Aspose.3D avsluta alla minne vid tolkning PDF fil PDF|
|THREEDNET-714|Aspose.3D kräver mycket minne och processor för att ladda en GLB-fil.|
|THREEDNET-715|Fast återgivning av den enkla masken (med endast normala data) med materialet PBR var felaktig|
|THREEDNET-711|Aspose.3D hänger på att importera en FBX fil.|
|THREEDNET-710|Rendering fungerar inte under vissa AMD hårdvara.|

## API ändringar ##
Denna version är främst en felfix version, så inga kodprover.

### Tillagda klasser ###
  * Klass Aspose.ThreeD. Skuggande.PbrSpecularMaterial - Detta används för att representera den spekulära pbr-materialet, just nu endast stöds i GLTF 2.0.
  * Tillad klass Aspose.ThreeD Enheter.VertexElementHål - för stöd hål i FBX:s nät
### Tilläggsmedlemmar ###
  * Tillagd medlem till enumtyp Aspose.ThreeD.Entiteter.VertexElementType.
```
public static Aspose.ThreeD.Entities.VertexElementType Hole;
```
  * Tillagda medlemmar i klass Aspose.ThreeD.FileFormatt
```
public static readonly Aspose.ThreeD.FileFormat Zip;
```
Med detta nya filformat stöd kan Aspose.3D importera en zip-fil som innehåller en fil 3D. Vanligtvis behöver du inte använda detta manuellt.

