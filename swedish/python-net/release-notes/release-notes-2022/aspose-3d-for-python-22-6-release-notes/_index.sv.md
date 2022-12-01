---
title: Aspose.3D för Python via .NET 22,6 Utgivning
type: docs
weight: 7
url: /sv/python-net/aspose-3d-for-python-net-22-6-release-notes/
description: Utgivningsnoterna av Aspose.3D för Python via .NET 22,6.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D för Python via .NET 22.6.

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

### Lagt till ny metod till klass `aspose.threed.FileFormat`

{{< highlight "python" >}}
    
    # Gets the preferred file format from the file extension name
    # The extension name should starts with a dot('.').
    def get_format_by_extension(extensionName)

{{< /highlight >}}

Du kan få en FilFormat instans med tilläggsnamn, exempelkod:

{{< highlight "python" >}}

scene = Scene(Box())
format = FileFormat.get_format_by_extension(".fbx")
# save the scene to memory stream using FileFormat returned by GetFormatByExtension
stream = BytesIO()
scene.save(stream, format)

{{< /highlight >}}



### Lagt till ny metod till klass `aspose.threed.Scene`

{{< highlight "python" >}}

    # Saves the scene to specified path using specified file format.
    def save(fileName)

{{< /highlight >}}

Den nya metoden låter dig spara scenen till en 3D-fil utan att tillhandahålla ett filformat.

Exempelkod:

{{< highlight "python" >}}

scene = Scene.from_file("Input.fbx")
scene.save("Output.usdz)

{{< /highlight >}}
