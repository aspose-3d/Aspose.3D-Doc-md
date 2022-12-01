---
title: Aspose.3D for .NET 18.9-settembre 2018
type: docs
weight: 40
url: /it/net/aspose-3d-for-net-18-9-september-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 18.9](https://www.nuget.org/packages/Aspose.3D/18.9.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-414|Supporto CancellationToken|Nuova funzione|
|THREEDNET-423|FBX ExportExportExportException-Alto numero di poligonali|Bug|
|THREEDNET-419|Eccezione di importanza durante l'apertura di enormi file FBX|Bug|
|THREEDNET-421|Non tutte le proprietà delle impostazioni globali dello FBX vengono caricate in AssetInfo|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **API modifiche**
#### **Classe rimossa Aspose.ThreeD.Utilities.Tuple**
{{< highlight "java" >}}

 In order to use some advanced features(CancellationToken), we have dropped the support of .net 3.5, so some replacement classes are also removed.

{{< /highlight >}}
#### **Aggiunta una proprietà AssetInfo alla classe Aspose.ThreeD. Nodo:**
Alcuni tipi di file possono avere informazioni sulle risorse per nodo.
In FBX, la proprietà AssetInfo del nodo radice contiene le impostazioni globali definite nei file FBX.

{{< highlight "java" >}}

         /// <summary>

        /// Per-node asset info

        /// </summary>

        Aspose.ThreeD.AssetInfo AssetInfo{ get;set;}

{{< /highlight >}}

**Codice del campione:**

{{< highlight "java" >}}

         //Access GlobalSettings in FBX file, more properties can be found by opening the ASCII FBX files in a text editor.

        //And FBXHeaderExtension/SceneInfo inside FBX file will be mapped to Scene.AssetInfo

		Scene scene = new Scene(@"test.fbx");

        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("DefaultCamera"));

        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("UpAxis"));

        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("FrontAxis"));

{{< /highlight >}}
#### **Aggiunto CancellationToken nei metodi Open/Save:**
**Vecchi metodi:**

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

**Nuovi metodi:**

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

Tutti i metodi di open/save avranno un parametro di cancellazione extra Token con un valore predefinito, quindi i codici che hanno utilizzato questi metodi non devono essere modificati per essere compilati.

È possibile utilizzare CancellationTokenSource per annullare l'attività di salvataggio/apertura in qualsiasi momento necessario.

**Codice del campione:**

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
