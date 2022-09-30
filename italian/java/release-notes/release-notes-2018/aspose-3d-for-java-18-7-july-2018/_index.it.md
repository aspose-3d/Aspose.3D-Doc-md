---
title: Aspose.3D for Java 18.7-luglio 2018
type: docs
weight: 60
url: /it/java/aspose-3d-for-java-18-7-july-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for Java 18.7](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.7/).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Riassunto**|**Categoria**|
|:- |:- |
|Aggiungi il supporto per l'importazione di Draco 2.2|Nuova funzione|
|Aggiungi supporto per l'esportazione Draco 2.2|Nuova funzione|
|Importare i file glTF con compressione draco|Nuova funzione|

## **Pubblico API e modifiche incompatibili arretrate**
Si prega di visualizzare l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché eventuali modifiche non retrocompatibili apportate allo Aspose.3D for Java API. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).

## **API modifiche:**

**3 membri rimossi dalla classe com.aspose.threed. Proprietà:**

{{< highlight "java" >}}

     public void com.aspose.threed.Property.setExtraData(java.lang.String);

    public java.lang.String com.aspose.threed.Property.getExtraData();

    public int com.aspose.threed.Property.getFlags();

{{< /highlight >}}

Questi vengono rimossi per sincronizzare le modifiche dalla versione .NET. (Sono programmati per essere rimossi dallo Aspose.3D for .NET 18.2)

**1 proprietà aggiunta alla classe com.aspose.threed.ObjLoadOptions:**

{{< highlight "java" >}}

     public boolean com.aspose.threed.ObjLoadOptions.getNormalizeNormal();

    public void com.aspose.threed.ObjLoadOptions.setNormalizeNormal(boolean);

{{< /highlight >}}

Ottiene o imposta se normalizzare il vettore normale durante il caricamento, il valore predefinito è vero.

**Codice del campione:**

{{< highlight "java" >}}

         Scene scene = new Scene();

        ObjLoadOptions opt = new ObjLoadOptions();

        opt.setNormalizeNormal(false);

        scene.open("test.obj", opt);

{{< /highlight >}}

Questo caricherà il file obj e lascerà i vettori normali non normalizzati, la vecchia versione normalizzerà i vettori normali quando il file obj viene caricato.
