---
title: Aspose.3D for Java 21,7 Utgivning
type: docs
weight: 6
url: /sv/java/aspose-3d-for-java-21-7-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 21.7.

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

{{< highlight "java" >}}
    Scene scene = new Scene();
    //...prepare your scene
    scene.Save("test.usdz", FileFormat.USDZ);
{{< /highlight >}}


### Tillagd klass com.pose.3.FileSystemFactory ###


{{< highlight "java" >}}
    /**
    * {@link com.aspose.threed.SaveOptions} and {@link com.aspose.threed.LoadOptions} will create a {@link com.aspose.threed.LocalFileSystem} for default.
    * This can be a security issue in server environment.
    * Use your own {@link com.aspose.threed.FileSystemFactory} to {@link com.aspose.threed.IOConfig#getFileSystemFactory} to improve server side security.
    */
    public interface FileSystemFactory
    {    
        FileSystem call();
        
    }
{{< /highlight >}}


### Tillagd ny egenskap FileSystemFaktig till com.aspose.3reed.IOConfig:


{{< highlight "java" >}}
    /**
     * Gets the factory class for FileSystem.
     * The default factory will create {@link com.aspose.threed.LocalFileSystem} which is not suitable for server environment.
     */
    public static FileSystemFactory getFileSystemFactory();
    
    /**
     * Sets the factory class for FileSystem.
     * The default factory will create {@link com.aspose.threed.LocalFileSystem} which is not suitable for server environment.
     * @param value New value
     */
    public static void setFileSystemFactory(FileSystemFactory value);

{{< /highlight >}}



Det kan vara farligt om användaren gjorde en skadlig 3D fil och laddade upp innehållet till din server, Den nya FileSystemFactory låter dig ange din egen implementering av FileSystem för att ersätta originalet LocalFileSystem som kan läsa ditt känsliga uppgifter vid export av en 3D-fil.







### Lagt till ny egenskap i com.aspose.3.FileFormat:

{{< highlight "java" >}}
    /**
     * Gets whether Aspose.3D supports export scene to current file format.
     */
    public boolean getCanExport();
    
    /**
     * Gets whether Aspose.3D supports import scene from current file format.
     */
    public boolean getCanImport();

{{< /highlight >}}

Du kan testa om ett filformat stöder import eller export via dessa egenskaper.