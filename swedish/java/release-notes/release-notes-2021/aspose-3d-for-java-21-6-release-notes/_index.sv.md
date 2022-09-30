---
title: Aspose.3D for Java 21,6 Utgivningsmeddelanden
type: docs
weight: 7
url: /sv/java/aspose-3d-for-java-21-6-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 21.6.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-870 |Lägg till USDC exportstöd.|Ny funktion|
|THREEDNET-891 |Visa zip- arkivfilsystemet|Ny funktion|
|THREEDNET-892 |Låt FBX exportör att inbädda texturer under exporten.|Ny funktion|
|THREEDNET-895 |Fast några tecken i nodens namn orsakar genererad GLB filen misslyckades att godkänna validering|Felrättning|
|THREEDNET-896 |Fast tom scen kan inte exportera till en giltig glb-fil|Felrättning|
|THREEDNET-890 |Lägg till material/texturexport i USDC|Förbättring|
|THREEDNET-899 |Exponera fastigheten av RelativeFilename för FBX Textura|Förbättring|




## API ändringar ##


### Lagt till USD som exporttyp. ###

Från 21.6 kan du exportera scen till en USD fil genom:

{{< highlight "csharp" >}}
    Scene scene = new Scene();
    //...prepare your scene
    scene.save("test.usd", FileFormat.USD);
{{< /highlight >}}

### Lagt till ny klass com.aspose.treed.ZiparkivFileSystemName ###

Det är möjligt för glb/fbx och andra filformat som stöder inbäddad textur för att få tillgång till externa tillgångar genom en zip-fil av . använd ett Ziparkivfilsystem för att spara options. Filsystem.


### Lagt ny egenskap till klassen com.aspose.treed.FbxSaveOptions. ###

{{< highlight "csharp" >}}
    /**
     * Gets whether to embed the texture to the final output file.
     * FBX Exporter will try to find the texture's raw data from {@link com.aspose.threed.IOConfig#getFileSystem}, and embed the file to final FBX file.
     * Default value is false.
     */
    public boolean getEmbedTextures();
    
    /**
     * Sets whether to embed the texture to the final output file.
     * FBX Exporter will try to find the texture's raw data from {@link com.aspose.threed.IOConfig#getFileSystem}, and embed the file to final FBX file.
     * Default value is false.
     * @param value New value
     */
    public void setEmbedTextures(boolean value);
{{< /highlight >}}


Provkod:

{{< highlight "java" >}}
    var scene = new Scene();
    var opt = new FbxSaveOptions(FileFormat.FBX7700ASCII);
    opt.setEmbedTextures(true);
    var tex = new Texture();
    tex.setFileName("test.png");
    var mat = new PhongMaterial();
    mat.setTexture(Material.MAP_DIFFUSE, tex);
    var planeNode = scene.getRootNode().createChildNode(new Plane());
    planeNode.setMaterial(mat);
    scene.save("plane-with-texture.fbx", opt);
{{< /highlight >}}

