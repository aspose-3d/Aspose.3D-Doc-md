---
title: Aspose.3D for .NET 22,2 Utgivning
type: docs
weight: 11
url: /sv/net/aspose-3d-for-net-22-2-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 22.2.2

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1054 |Tillåt inbädda texturer i filen U3D och PDF|Ny funktion|
|THREEDNET-1058 |Primitiven kan inte binda till material under USD exportör/importör|Felrättning|
|THREEDNET-1051 |Tillåt åtkomst tillägg och tillägg i filen GLTF|Förbättring|
|THREEDNET-1048 |Tillåt att koda scen och nodens metadata till usd|Ny funktion|
|THREEDNET-1049 |Tillåt avkoda scen och nodens metadata från usd|Ny funktion|

## API ändringar ##


### Medlemmar till `Aspose.ThreeD.AssetInfo`:

{{< highlight "csharp" >}}
        public string Copyright{ get;set;}
{{< /highlight >}}

Får filens upphovsrätt, kan detta värde vara noll eller definierat i filen 3D.
Endast USDC/USDZ stöder denna fastighet nu.

OBS: Ändringar i denna egenskap kommer inte att ändra upphovsrättssnittet i output 3D-filen.


### Medlemmar till `Aspose.ThreeD.Formats.UsdSaveOptions`:

{{< highlight "csharp" >}}
        public bool ExportMetaData{ get;set;}
{{< /highlight >}}

Får eller ställer in om att exportera scenens tillgång info och nodens egenskaper till utgången USDC/USDZ-filen.



### Medlemmar till `Aspose.ThreeD.Formats.PdfSaveOptions`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Embed the external textures into the PDF file, default value is false.
        /// </summary>
        public bool EmbedTextures{ get;set;}
{{< /highlight >}}

Ställ in detta till true för att skapa 3D PDF fil med inbäddade texturfiler.

Exempelkod:

{{< highlight "csharp" >}}
        var scene = new Scene();
        scene.Open($"test.obj");
        var opt = new PdfSaveOptions();
        //embed the external textures in the output PDF file.
        opt.EmbedTextures = true;
        //Look up external textures in the  common/textures directory
        opt.LookupPaths.Add("common/textures");
        scene.Save("test.pdf", opt);
{{< /highlight >}}


### Medlemmar till `Aspose.ThreeD.Formats.U3dSaveOptions`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Embed the external textures into the U3D file, default value is false.
        /// </summary>
        public bool EmbedTextures{ get;set;}
{{< /highlight >}}

Ställ in detta till true för att skapa 3D U3D fil med inbäddade texturfiler.

Exempelkod:

{{< highlight "csharp" >}}
        var scene = new Scene();
        scene.Open($"test.obj");
        var opt = new U3dSaveOptions();
        //embed the external textures in the output PDF file.
        opt.EmbedTextures = true;
        //Look up external textures in the  common/textures directory
        opt.LookupPaths.Add("common/textures");
        scene.Save("test.u3d", opt);
{{< /highlight >}}



