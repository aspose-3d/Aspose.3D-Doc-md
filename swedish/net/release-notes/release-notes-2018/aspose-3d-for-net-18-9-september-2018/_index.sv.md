---
title: Aspose.3D for .NET 18,9 - september 2018
type: docs
weight: 40
url: /sv/net/aspose-3d-for-net-18-9-september-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 18,9](https://www.nuget.org/packages/Aspose.3D/18.9.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-414|AvbokningToken supportName|Ny funktion|
|THREEDNET-423|FBX ExportException - Hög polygonräkning|FelComment|
|THREEDNET-419|ImportException när du öppnar enorma FBX filer|FelComment|
|THREEDNET-421|Inte alla egenskaper från FBX:s globala inställningar laddas in i AssetInfo|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **API ändringar**
#### **Avlägsnad klass Aspose.ThreeD.Användningar.Tupler**
{{< highlight "java" >}}

 In order to use some advanced features(CancellationToken), we have dropped the support of .net 3.5, so some replacement classes are also removed.

{{< /highlight >}}
#### **Lagt till en fastighet AssetInfo till klass Aspose.ThreeD.Node:**
Vissa filtyper kan ha per-nodens tillgångsinformation.
I FBX, egenskapen AssetInfo av rotnoden innehåller de globala inställningar som definieras i FBX filer.

{{< highlight "java" >}}

         /// <summary>

        /// Per-node asset info

        /// </summary>

        Aspose.ThreeD.AssetInfo AssetInfo{ get;set;}

{{< /highlight >}}

**Provkod:**

{{< highlight "java" >}}

         //Access GlobalSettings in FBX file, more properties can be found by opening the ASCII FBX files in a text editor.

        //And FBXHeaderExtension/SceneInfo inside FBX file will be mapped to Scene.AssetInfo

		Scene scene = new Scene(@"test.fbx");

        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("DefaultCamera"));

        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("UpAxis"));

        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("FrontAxis"));

{{< /highlight >}}
#### **Tillagd avbeställningToken in Open/Spara metoder:**
**Gamla metoder:**

{{< highlight "java" >}}

 		public void Open(System.IO.Stream stream, Aspose.ThreeD.FileFormat format)

        public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options)

        public void Open(System.IO.Stream stream)

        public void Open(string fileName, Aspose.ThreeD.FileFormat format)

        public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options)

        public void Open(string fileName)

        public void Save(System.IO.Stream stream, Aspose.ThreeD.FileFormat format)

        public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options)

        public void Save(string fileName, Aspose.ThreeD.FileFormat format)

        public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options)

{{< /highlight >}}

**Nya metoder:**

{{< highlight "java" >}}

         public void Open(System.IO.Stream stream, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(System.IO.Stream stream, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(string fileName, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(string fileName, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Save(System.IO.Stream stream, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Save(string fileName, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

{{< /highlight >}}

Alla öppna / spara metoder kommer att ha en extra avbokningTokenparameter med ett standardvärde, så koder som använde dessa metoder behöver inte ändra för att kompilera.

Du kan använda CancellationTokenSource för att avbryta spara/öppna uppgiften när som helst du behöver.

**Provkod:**

{{< highlight "java" >}}

         CancellationTokenSource cts = new CancellationTokenSource();

        Scene scene = new Scene();

        cts.CancelAfter(1000);

        try

        {

                scene.Open("test.fbx", cts.Token);

                Console.WriteLine("Import is done within 1000ms");

        }

        catch (ImportException e)

        {

                if (e.InnerException is OperationCanceledException)

                {

                        Console.WriteLine("It takes too long time to import, and we have canceled the importing.");

                }

        }

{{< /highlight >}}
