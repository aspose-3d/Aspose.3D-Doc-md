---
title: Aspose.3D for .NET 22,6 Utgivningsmeddelanden
type: docs
weight: 7
url: /sv/net/aspose-3d-for-net-22-6-release-notes/
description: Publiceringsnoterna av Aspose.3D for .NET 22.6.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 22.6.

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



### Lagt till ny metod till klass `Aspose.ThreeD.FileFormat`

{{< highlight "csharp" >}}

    /**
     * Gets the preferred file format from the file extension name
     * The extension name should starts with a dot('.').
     * @param extensionName 
     */
    public static FileFormat getFormatByExtension(String extensionName)

{{< /highlight >}}

Du kan få en FilFormat instans med tilläggsnamn, exempelkod:

{{< highlight "csharp" >}}

var scene = new Scene(new Box());
var format = FileFormat.getFormatByExtension(".fbx");
//save the scene to memory stream using FileFormat returned by GetFormatByExtension
var stream = new ByteArrayOutputStream();
scene.save(Stream.wrap(stream), format);


{{< /highlight >}}



### Lagt till ny metod till klass `Aspose.ThreeD.Scene`

{{< highlight "csharp" >}}
        /// <summary>
        /// Saves the scene to specified path using specified file format.
        /// </summary>
        /// <param name="fileName">File name.</param>
        public void Save(string fileName)
{{< /highlight >}}

Den nya metoden låter dig spara scenen till en 3D-fil utan att tillhandahålla ett filformat.

Exempelkod:

{{< highlight "csharp" >}}

var scene = Scene.FromFile("Input.fbx");
scene.Save("Output.usdz);

{{< /highlight >}}


### Lagt till nya metoder till klass `Aspose.ThreeD.Transform`

{{< highlight "csharp" >}}
        public Transform SetGeometricTranslation(double x, double y, double z)
        public Transform SetGeometricScaling(double sx, double sy, double sz)
        public Transform SetGeometricRotation(double rx, double ry, double rz)
        public Transform SetTranslation(double tx, double ty, double tz)
        public Transform SetScale(double sx, double sy, double sz)
        public Transform SetEulerAngles(double rx, double ry, double rz)
        public Transform SetRotation(double rw, double rx, double ry, double rz)
        public Transform SetPreRotation(double rx, double ry, double rz)
        public Transform SetPostRotation(double rx, double ry, double rz)
{{< /highlight >}}

Dessa hjälpmetoder tillhandahålls for Java/Python bindningar, du kan också använda dem för att ge kedja-stil omvandling, Exempelkod:


{{< highlight "csharp" >}}
        var scene = new Scene();
        var node = scene.RootNode.CreateChildNode(new Box());
        node.Transform
                .SetTranslation(10, 0, 0)
                .SetScale(20, 1, 1)
        ;
{{< /highlight >}}
