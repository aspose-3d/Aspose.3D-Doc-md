---
title: Aspose.3D for Java 22,2 Utgivning
type: docs
weight: 11
url: /sv/java/aspose-3d-for-java-22-2-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 22.2.2

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|TREJAJAVA-10545|Tillåt inbädda texturer i filen U3D och PDF|Ny funktion|
|TRE JAVA|Primitiven kan inte binda till material under USD exportör/importör|Felrättning|
|TRE JAVA-10511|Tillåt åtkomst tillägg och tillägg i filen GLTF|Förbättring|
|TREJAVA-10488|Tillåt att koda scen och nodens metadata till usd|Ny funktion|
|TRE JAVA-1049.|Tillåt avkoda scen och nodens metadata från usd|Ny funktion|

## API ändringar ##


### Lagt till medlemmar i klassen com.aspose.3reed.AssetInfo:

{{< highlight "java" >}}
    /**
     * Gets the document's copyright
     */
    public String getCopyright();

{{< /highlight >}}

Får filens upphovsrätt, kan detta värde vara noll eller definierat i filen 3D.
Endast USDC/USDZ stöder denna fastighet nu.

OBS: Ändringar i denna egenskap kommer inte att ändra upphovsrättssnittet i output 3D-filen.


### Medlemmar till `com.aspose.threed.UsdSaveOptions`:

{{< highlight "csharp" >}}
    /**
     * Export meta data associated with Scene/Node to client
     * Default value is true
     */
    public boolean getExportMetaData();
    
    /**
     * Export meta data associated with Scene/Node to client
     * Default value is true
     * @param value New value
     */
    public void setExportMetaData(boolean value);

{{< /highlight >}}

Får eller ställer in om att exportera scenens tillgång info och nodens egenskaper till utgången USDC/USDZ-filen.



### Medlemmar till `com.aspose.threed.PdfSaveOptions`:

{{< highlight "java" >}}
    /**
     * Embed the external textures into the PDF file, default value is false.
     */
    public boolean getEmbedTextures();
    
    /**
     * Embed the external textures into the PDF file, default value is false.
     * @param value New value
     */
    public void setEmbedTextures(boolean value);
{{< /highlight >}}

Ställ in detta till true för att skapa 3D PDF fil med inbäddade texturfiler.

Exempelkod:

{{< highlight "java" >}}
        var scene = new Scene();
        scene.open("test.obj");
        var opt = new PdfSaveOptions();
        //embed the external textures in the output PDF file.
        opt.setEmbedTextures(true);
        //Look up external textures in the  common/textures directory
        opt.getLookupPaths().add("common/textures");
        scene.save("test.pdf", opt);
{{< /highlight >}}


### Medlemmar till `com.aspose.threed.U3dSaveOptions`:

{{< highlight "java" >}}
    /**
     * Embed the external textures into the U3D file, default value is false.
     */
    public boolean getEmbedTextures();
    
    /**
     * Embed the external textures into the U3D file, default value is false.
     * @param value New value
     */
    public void setEmbedTextures(boolean value);

{{< /highlight >}}

Ställ in detta till true för att skapa 3D U3D fil med inbäddade texturfiler.

Exempelkod:

{{< highlight "java" >}}
        var scene = new Scene();
        scene.open("test.obj");
        var opt = new U3dSaveOptions();
        //embed the external textures in the output PDF file.
        opt.setEmbedTextures(true);
        //Look up external textures in the  common/textures directory
        opt.getLookupPaths().add("common/textures");
        scene.save("test.u3d", opt);
{{< /highlight >}}



