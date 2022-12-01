---
title: Aspose.3D for .NET 21,5 Utgivning
type: docs
weight: 8
url: /sv/net/aspose-3d-for-net-21-5-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 21.5.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-878 |Rita svart kant runt polygoner|Ny funktion|
|THREEDNET-879 |Konvertera STL till GLB resultat till ogiltigt attribut: ”/mashes/0/primitiva/0/attribut/NORMAL_0”|Felrättning|
|THREEDNET-885 |Aspose.3D renderare kraschade på grund av stora maskar lastade.|Felrättning|
|THREEDNET-884 |Validering i konverterade GLB filer.|Förbättring|
|THREEDNET-882 |Genererad GLB filen renderas inte i Babylon.js|Felrättning|
|THREEDNET-887 |Konvertera bild till jpg/png när användaren exporterar glTF med inbäddade tillgångar|Ny funktion|


## API ändringar ##


### Lagt till ny enum typ Aspose.ThreeD.Formats.GltfEmbeddedImageFormat: ###

{{< highlight "java" >}}
    /// <summary>
    /// How glTF exporter will embed the textures during the exporting.
    /// </summary>
    public enum GltfEmbeddedImageFormat
    {
        /// <summary>
        /// Do not convert the image and keep it as it is.
        /// </summary>
        NoChange,
        /// <summary>
        /// All non-supported images formats will be converted to jpeg if possible.
        /// </summary>
        Jpeg,
        /// <summary>
        /// All non-supported images formats will be converted to png if possible.
        /// </summary>
        Png
    }
{{< /highlight >}}

### Lagt till ny fastighet i Aspose.ThreeD.Formats.GltfSaveOptions: ###

{{< highlight "java" >}}
        public GltfEmbeddedImageFormat ImageFormat { get;set; }
{{< /highlight >}}


Standard glTF stöder endast PNG/JPG som dess texturformat, Detta alternativ kommer att vägleda hur Aspose.3D kommer att konvertera icke-standard bilder till stöd format under exporten.

Standardvärde är GltfEmbeddedImageFormat. Png, sedan den inbäddade texturen kommer att omvandlas till png, vanligtvis behöver du inte ändra detta manuellt.


### Lagt till ny fastighet i Aspose.ThreeD.Formats.GltfSaveOptions:

{{< highlight "java" >}}
        public Vector3? FallbackNormal { get; set; }
{{< /highlight >}}

När exportör av GLTF2 upptäckte ett ogiltigt normalt från platsen, kommer detta att användas istället för sitt ursprungliga värde för att kringgå valideringen. detta händer om scenen importerades från en fil som exporteras med felaktiga data.

Standardvärdet är (0, 1, 0).

Om tilldela detta värde med noll, kommer felaktiga normala data att skickas utan några ändringar.
