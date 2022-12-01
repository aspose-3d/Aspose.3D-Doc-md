---
title: Aspose.3D for .NET 22,9 Utgivning
type: docs
weight: 4
url: /sv/net/aspose-3d-for-net-22-9-release-notes/
description: Publiceringsnoterna av Aspose.3D for .NET 22.9.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 22.9.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1232 |Lägg till internt stöd för tillfälligt filsystem för importör FBX|Förbättring|
|THREEDNET-1111 |GLTF exporten är inte bra.|Felrättning|
|THREEDNET-1215 |När man importerar en OBJ-fil, kan en nod bara läsa ett material?|Felrättning|
|THREEDNET-1216 |Konvertera GLB till GLB förlorar texturer|Felrättning|
|THREEDNET-1225 |Analysera problem som hittats i App-servern - 2022 September 2027|Felrättning|
|THREEDNET-1227 |Alternativ som inte stöds i ASE filer: MATERIAL_SOFTEN/FYSIKK/MATERIEL_SHINE|Felrättning|
|THREEDNET-1228 |Undantag vid import av JT filer: Ett objekt med samma nyckel har redan lagts till.|Felrättning|
|THREEDNET-1230 |STL filer med fyra sidor stöds inte.|Felrättning|
|THREEDNET-1231 |Inte stödd USD typ StringVector, lageröverföringVector.|Felrättning|


## API ändringar ##


### Lagt till ny metod i klass `Aspose.ThreeD.Shading.PbrMaterial`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Allow convert other material to PbrMaterial
        /// </summary>
        /// <param name="material"></param>
        /// <returns></returns>
        public static PbrMaterial FromMaterial(Material material)
{{< /highlight >}}


Denna verktygsmetod tillåter konvertera andra typer av material till PbrMaterial instans, och försöka reservera information så mycket som möjligt.


