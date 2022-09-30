---
title: Aspose.3D for .NET 21,6 Utgivningsmeddelanden
type: docs
weight: 7
url: /sv/net/aspose-3d-for-net-21-6-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 21.6.

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
    scene.Save("test.usd", FileFormat.USD);
{{< /highlight >}}

### Lagt till ny klass Aspose.ThreeD.Användningar. ###

Det är möjligt för glb/fbx och andra filformat som stöder inbäddad textur för att få tillgång till externa tillgångar genom en zip-fil av . använd ett Ziparkivfilsystem för att spara options. Filsystem.


### Lagt ny egenskap till klass Aspose.ThreeD.Formats.FbxSaveOptions. ###

{{< highlight "csharp" >}}
    /// <summary>
    /// Gets or sets whether to embed the texture to the final output file.
    /// FBX Exporter will try to find the texture's raw data from <see cref="IOConfig.FileSystem"/>, and embed the file to final FBX file.
    /// Default value is false.
    /// </summary>
    public bool EmbedTextures{ get;set;}
{{< /highlight >}}


Provkod:

{{< highlight "java" >}}
    var scene = new Scene();
    var opt = new FbxSaveOptions(FileFormat.FBX7700ASCII);
    opt.EmbedTextures = true;
    var tex = new Texture();
    tex.FileName = "test.png";
    tex.SetProperty("RelativeFilename", "test.png");
    var mat = new PhongMaterial();
    mat.SetTexture(Material.MapDiffuse, tex);
    var planeNode = scene.RootNode.CreateChildNode(new Plane());
    planeNode.Material = mat;
    scene.Save("plane-with-texture.fbx", opt);

{{< /highlight >}}


### Ta bort föråldrad klass Aspose.ThreeD.Formats.A3DWSaveOptions. ###
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.AMFSaveOptions
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.Discreet3DSLoadOptions.
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.Discreet3DSSaveOptions. ###
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.FBXLoadOptions. ###
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.FBXSaveOptions. ###
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.GLTFLoadOptions. ###
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.GLTFSaveOptions ###
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.HTML5SparaOptions. ###
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.STLLoadOptions. ###
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.STLSaveOptioner ###
Denna klass markerades som föråldrad månader tidigare.

### Ta bort föråldrad klass Aspose.ThreeD.Formats.U3DLoadOptions. ###
Denna klass markerades som föråldrad månader tidigare.
