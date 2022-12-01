---
title: Aspose.3D for .NET 21,7 Utgivning
type: docs
weight: 6
url: /sv/net/aspose-3d-for-net-21-7-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 21.7.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-870 |Stöd för export till USDZ format.|Ny funktion|
|THREEDNET-901 |Tillåt användaren att ange en fabriksklass för FileSystem för att förbättra säkerhetsnivån|Ny funktion|
|THREEDNET-902 |Lägg till GeomSubset i USDC exportör för att stödja flera material|Förbättring|
|THREEDNET-903 |GLTF Spara stödmaterialnamn|Förbättring|
|THREEDNET-905 |USD filer som innehåller skelett stöds inte.|Felrättning|
|THREEDNET-904 |USD filer som innehåller normala som primvars stöds inte.|Felrättning|
|THREEDNET-909 |USD till GLTF används över 9G-minne.|Felrättning|





## API ändringar ##



### Lagt till USDZ som exporttyp. ###

Från 21.7 kan du exportera scen till USDZ genom:

{{< highlight "csharp" >}}
    Scene scene = new Scene();
    //...prepare your scene
    scene.Save("test.usdz", FileFormat.USDZ);
{{< /highlight >}}


### Tillagd klass Aspose.ThreeD. Format.FilSystemFactory ###


{{< highlight "csharp" >}}
    /// <summary>
    /// <see cref="SaveOptions"/> and <see cref="LoadOptions"/> will create a <see cref="LocalFileSystem"/> for default.
    /// This can be a security issue in server environment.
    /// Use your own <see cref="FileSystemFactory"/> to <see cref="IOConfig.FileSystemFactory"/> to improve server side security.
    /// </summary>
    /// <returns></returns>
    public delegate FileSystem FileSystemFactory();
{{< /highlight >}}


### Tillagd ny egenskap FileSystemFactory to Aspose.ThreeD.Formats.IOConfig:


{{< highlight "csharp" >}}
        /// <summary>
        /// Gets or sets the factory class for FileSystem.
        /// The default factory will create <see cref="LocalFileSystem"/> which is not suitable for server environment.
        /// </summary>
        public static FileSystemFactory FileSystemFactory { get; set; }
{{< /highlight >}}



Det kan vara farligt om användaren gjorde en skadlig 3D fil och laddade upp innehållet till din server, Den nya FileSystemFactory låter dig ange din egen implementering av FileSystem för att ersätta originalet LocalFileSystem som kan läsa ditt känsliga uppgifter vid export av en 3D-fil.







### Lagt ny fastighet till Aspose.ThreeD.FileFormat:

{{< highlight "csharp" >}}
        /// <summary>
        /// Gets whether Aspose.3D supports export scene to current file format.
        /// </summary>
        public bool CanExport { get; set; }
        /// <summary>
        /// Gets whether Aspose.3D supports import scene from current file format.
        /// </summary>
        public bool CanImport { get; set; }
{{< /highlight >}}

Du kan testa om ett filformat stöder import eller export via dessa egenskaper.