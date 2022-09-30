---
title: Aspose.3D for Java 22,6 Utgivningsmeddelanden
type: docs
weight: 7
url: /sv/java/aspose-3d-for-java-22-6-release-notes/
description: Publiceringsnoterna av Aspose.3D for Java 22.6.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 22.6.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1152 |Tillåt spara 3D scen utan att ange filformatet|Ny funktion|
|THREEDNET-1157 |Import av SdfValueBlock stöds inte i USDZ|Förbättring|
|THREEDNET-1156 |Undantag av GLF: Misslyckades importera glTF, byteOffset är inte definierat i accessor|Felrättning|
|THREEDNET-1154 |Aspose.ThreeD.ExportExportException: Spec duplicerat medan omvandlingen DAE till USDZ|Felrättning|
|THREEDNET-1153 |Undantag sker när man sparar USDZ till GLTF|Felrättning|



## API ändringar ##

### Lagt till ny metod till klass `com.aspose.threed.FileFormat`:

{{< highlight "csharp" >}}
    /**
     * Gets the preferred file format from the file extension name
     * The extension name should starts with a dot('.').
     * @param extensionName 
     */
    public static FileFormat getFormatByExtension(String extensionName)
{{< /highlight >}}

Du kan få en FilFormat instans med tilläggsnamn, exempelkod:

{{< highlight "java" >}}

var scene = new Scene(new Box());
var format = FileFormat.getFormatByExtension(".fbx");
//save the scene to memory stream using FileFormat returned by GetFormatByExtension
var stream = new ByteArrayOutputStream();
scene.save(Stream.wrap(stream), format);

{{< /highlight >}}



### Lagt till ny metod till klass `com.aspose.threed.Scene`:

{{< highlight "java" >}}
    /**
     * Saves the scene to specified path using specified file format.
     * @param fileName File name.
     */
    public void save(String fileName)
        throws IOException;

{{< /highlight >}}

Den nya metoden låter dig spara scenen till en 3D-fil utan att tillhandahålla ett filformat.

Exempelkod:

{{< highlight "java" >}}

var scene = Scene.fromFile("Input.fbx");
scene.save("Output.usdz);

{{< /highlight >}}
