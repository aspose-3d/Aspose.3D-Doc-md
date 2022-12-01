---
title: Aspose.3D for .NET 20.2 Note di rilascio
type: docs
weight: 60
url: /it/net/aspose-3d-for-net-20-2-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 20.2

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-612 |Generazione di forma I procedurale compatibile con ` `IFC|` `Nuova funzionalità|
|THREEDNET-615 |Generazione di forma C procedurale compatibile con ` `IFC|` `Nuova funzionalità|
|THREEDNET-616 |Generazione di forma Z procedurale compatibile ` `IFC|` `Nuova funzionalità|
|THREEDNET-617 |Generazione di forma L procedurale compatibile con ` `IFC|` `Nuova funzionalità|
|THREEDNET-618 |Generazione di forma a T procedurale compatibile con ` `IFC|` `Nuova funzionalità|
|THREEDNET-619 |Generazione di forma a U procedurale compatibile con ` `IFC|` `Nuova funzionalità|
|THREEDNET-620 |Generazione di forma rettangolare procedurale compatibile con ` `IFC|` `Nuova funzionalità|
|THREEDNET-625 |Generazione di forma del cerchio procedurale compatibile con ` `IFC|` `Nuova funzionalità|
|THREEDNET-626 |Generazione di forma ellittica procedurale compatibile con ` `IFC|` `Nuova funzionalità|
|THREEDNET-558 |` `Aggiungi il supporto per il rendering della trasparenza nel renderer web|` ` Potenziamento|
|THREEDNET-606 |` ` Visualizza casella di delimitazione se nodo selezionato nel browser delle risorse.|` ` Potenziamento|
|THREEDNET-613 |` `Aggiungere il supporto di rendering della forma|` ` Potenziamento|
|THREEDNET-630 |` ` Il processo si blocca quando si caricano i file RVM|` `Bug|
|THREEDNET-632 |` ` Eccezione sul caricamento del file FBX|` `Bug|
|THREEDNET-629 |` ` Eccezione sulla conversione da GLB a 3d|` `Bug|
|THREEDNET-623 |La GPU dello ` `Intels non è supportata dal renderer Aspose.3D|` `Bug|
|THREEDNET-628 |` ` Eccezione sul caricamento del file FBX|` `Bug|
## **Pubblico API e modifiche incompatibili arretrate**
### **Aggiunta nuova classe Aspose.ThreeD. Profili. Profilo**
Questa classe è la classe base di tutti i profili, che può essere utilizzata per creare mesh parametrizzate. Una classe Profilo rappresenta un profilo 2D nel piano x-y.

{{< highlight "java" >}}

     /// <summary>

    /// 2D Profile in xy plane

    /// </summary>

    public abstract class Profile : Entity

    {

        /// <summary>

        /// Gets the extent in x and y dimension.

        /// </summary>

        /// <returns></returns>

        public abstract Vector2 GetExtent();

    }

    /// <summary>

    /// The base class of all parameterized profiles.

    /// </summary>

    public abstract class ParameterizedProfile : Profile

    {

    }

{{< /highlight >}}

Tutta la sottoclasse di Profile può essere convertita in mesh 3D tramite LinearExtrusion come mostrato nel seguente codice di esempio:



{{< highlight "java" >}}

 var mesh = new LinearExtrusion(new LShape()

    {

     FilletRadius = 1,

     Width = 4,

     Depth = 7

      }, 1);

Scene s = new Scene(mesh);

s.Save(@"LShape.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
### **Aggiunta nuova classe Aspose.ThreeD. Profili. CircleShape**
Le proprietà di CircleShape possono essere illustrate nella figura seguente.

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_1.png)
### **Aggiunta nuova classe Aspose.ThreeD. Profili. CShape**
Le proprietà di CShape possono essere illustrate nella figura seguente:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_2.png)
### **Aggiunta nuova classe Aspose.ThreeD. Profili. EllipseShape**
Le proprietà di EllipseShape possono essere illustrate in questa figura:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_3.png)


### **Aggiunta nuova classe Aspose.ThreeD. Profili. HShape**
Le proprietà di HShape possono essere illustrate in questa figura:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_4.png)


### **Aggiunta nuova classe Aspose.ThreeD. Profili. LShape**
Le proprietà di LShape possono essere illustrate in questa figura:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_5.png)


### **Aggiunta nuova classe Aspose.ThreeD. Profili. RectangleShape**
Le proprietà di RectangleShape possono essere illustrate in questa figura:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_6.png)


### **Aggiunta nuova classe Aspose.ThreeD. Profili. TrapeziumShape**
Le proprietà di TrapeziumShape possono essere illustrate in questa figura:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_7.png)


### **Aggiunta nuova classe Aspose.ThreeD. Profili. TShape**
Le proprietà di TShape possono essere illustrate nella figura seguente:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_8.png)


### **Aggiunta nuova classe Aspose.ThreeD.Profiles.UShape**
Le proprietà di UShape possono essere illustrate nella figura seguente:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_9.png)


### **Aggiunta nuova classe Aspose.ThreeD. Profili. ZShape**
Le proprietà di ZShape possono essere illustrate nella figura seguente.

![Todo: immagine_Alt_Testo](aspose-3d-for-net-20-2-release-notes_10.png)


### **Aggiunta nuova classe Aspose.ThreeD. Profili. MirroredShape**
Questo profilo definisce un nuovo profilo rispecchiando il profilo di base attorno all'asse y.

{{< highlight "java" >}}

 var mesh = new LinearExtrusion(new MirroredProfile(new LShape()

            {

                FilletRadius = 1,

                Width = 4,

                Depth = 7

            }), 1);

Scene s = new Scene(mesh);

s.Save(@"MirroredLShape.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

