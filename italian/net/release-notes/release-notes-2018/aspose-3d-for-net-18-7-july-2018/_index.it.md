---
title: Aspose.3D for .NET 18.7-luglio 2018
type: docs
weight: 60
url: /it/net/aspose-3d-for-net-18-7-july-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 18.7](https://www.nuget.org/packages/Aspose.3D/18.7.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-405|Aggiungi il supporto per l'importazione di Draco 2.2|Nuova funzione|
|THREEDNET-406|Aggiungi supporto per l'esportazione Draco 2.2|Nuova funzione|
|THREEDNET-408|Importare i file glTF con compressione draco|Nuova funzione|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **API modifiche**
Ci sono due cambiamenti principali:

1. Rimosse alcune classi e metodi obsoleti in base alla pianificazione, le classi XXXXConfig vengono tutte rimosse, l'utente deve utilizzare XXXXSaveOptions e XXXXLoadOptions che sono state introdotte nel 2016.
1. Importazione/esportazione di file, queste modifiche non apportano modifiche all'interfaccia.
1. Il supporto import/export Google Draco è stato aggiornato all'ultima versione.
1. Aspose.3D 18.7 Può importare glTF 2.0 che ha permesso la compressione draco.
#### **Classe rimossa Aspose.ThreeD. Formati. Discreet3DSConfig**
#### **Classe rimossa Aspose.ThreeD. Formati. FBXConfig**
#### **Classe rimossa Aspose.ThreeD. Formati. ObjConfig**
#### **Classe rimossa Aspose.ThreeD. Formati. STLConfig**
#### **Classe rimossa Aspose.ThreeD. Formati. Universal3DConfig**
#### **3 membri rimossi dalla classe Aspose.ThreeD.A3DObject**
{{< highlight "java" >}}

         public Aspose.ThreeD.Property CreateDynamicProperty(string propName, System.Type type)

        public Aspose.ThreeD.Property CreateDynamicProperty(string propName)

        public Aspose.ThreeD.Property GetDynamicProperty(string propName)

{{< /highlight >}}

Usa invece GetProperty/SetProperty, GetProperty/SetProperty vengono aggiunti in 17.12.
#### **3 membri rimossi dalla classe Aspose.ThreeD. Animazione. Curva:**
{{< highlight "java" >}}

         public Aspose.ThreeD.Animation.KeyFrame CreateKeyFrame(double time)

        public Aspose.ThreeD.Animation.KeyFrame CreateKeyFrame(double time, float value)

        public Aspose.ThreeD.Animation.KeyFrame CreateKeyFrame(double time, float value, Aspose.ThreeD.Animation.Interpolation interpolation)

{{< /highlight >}}

Usa Aggiungi invece, Aggiungi viene aggiunto in 17.9, usa Aggiungi invece di un altro nome può utilizzare la sintassi dell'inizializzatore di raccolta C# (<https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/object-and-collection-initializers>)
#### **3 membri rimossi dalla classe Aspose.ThreeD. Proprietà:**
{{< highlight "java" >}}

         public bool HasFlags(Aspose.ThreeD.PropertyFlags f)

        string ExtraData{ get;set;}

        Aspose.ThreeD.PropertyFlags Flags{ get;}

{{< /highlight >}}

Questi sono contrassegnati come obsoleti dal 18,2, questi sono principalmente per uso interno.
#### **4 metodi rimossi dalla classe Aspose.ThreeD. Scena:**
{{< highlight "java" >}}

         public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.IOConfig config)

        public void Open(string fileName, Aspose.ThreeD.Formats.IOConfig config)

        public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.IOConfig config)

        public void Save(string fileName, Aspose.ThreeD.Formats.IOConfig config)

{{< /highlight >}}

Poiché abbiamo XXXXSaveOptions/XXXXLoadOptions per sostituire XXXXConfig, questi metodi diventano inutili dopo aver rimosso XXXXConfig.
#### **3 metodi rimossi dalla classe Aspose.ThreeD.Utilities.Quaternion:**
{{< highlight "java" >}}

         public double GetPitch()

        public double GetYaw()

        public double GetRoll()

{{< /highlight >}}

Questi sono contrassegnati come obsoleti in 18.2, c' è il metodo di sostituzione EulerAngles().
#### **1 proprietà aggiunta alla classe Aspose.ThreeD. Formati. ObjLoadOptions:**
{{< highlight "java" >}}

         bool NormalizeNormal{ get;set;}

{{< /highlight >}}

Ottiene o imposta se normalizzare il vettore normale durante il caricamento, il valore predefinito è vero.
##### **Codice del campione:**
{{< highlight "java" >}}

         Scene scene = new Scene();

        scene.Open("test.obj", new ObjLoadOptions() {NormalizeNormal = false});

{{< /highlight >}}

Questo caricherà il file obj e lascerà i vettori normali non normalizzati, la vecchia versione normalizzerà i vettori normali quando il file obj viene caricato.
