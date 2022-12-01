---
title: Aspose.3D for .NET 17.12-Dicembre 2017
type: docs
weight: 10
url: /it/net/aspose-3d-for-net-17-12-december-2017/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 17.12](https://www.nuget.org/packages/Aspose.3D/17.12.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-304|Aggiungere il supporto di esportazione RVM (AVEVA PDMS)|Nuova funzionalità|
|THREEDNET-312|Aggiungi un modo stenografico per scalare le geometrie|Miglioramento|
|THREEDNET-314|Aggiungere il supporto per l'esportazione di proprietà/ID personalizzati ai nodi nel formato GLTF|Miglioramento|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge la proprietà SaveExtras alla classe Aspose.ThreeD.Formats.GLTFSaveOptions**
Il valore predefinito della proprietà SaveExtras è falso, se si desidera che Aspose.3D for .NET API per esportare le proprietà personalizzate dell'oggetto, è possibile assegnarlo a true.

**C#**

{{< highlight "java" >}}

 public bool SaveExtras{ get;set;}

{{< /highlight >}}

{{% alert color="primary" %}} 

Le proprietà personalizzate verranno salvate in un campo "extra" a causa delle specifiche dello glTF. Un esempio di codice è narrato di seguito.

{{% /alert %}}
#### **Aggiunge tre membri alla classe Aspose.ThreeD.A3DObject**
RemoveProperty, GetProperty, SetProperty sono un insieme di metodi short-handed per manipolare le proprietà personalizzate dell'oggetto. I vecchi metodi come FindProperty e CreateDynamicProperty sono troppo prolissi e pianificati per essere rimossi in futuro. Le proprietà personalizzate sono supportate da FBX/glTF (tutte le versioni).

**C#**

{{< highlight "java" >}}

 public bool RemoveProperty(string property)

public object GetProperty(string property)

public void SetProperty(string property, object value)

{{< /highlight >}}

**Codice del campione:**

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

var box = scene.RootNode.CreateChildNode("box", new Box());

box.SetProperty("obj-id", "box-id");

scene.Save("test.fbx", FileFormat.FBX7400ASCII);

scene.Save("test.gltf", new GLTFSaveOptions(FileFormat.GLTF){SaveExtras = true});

scene.Save("test-2.gltf", new GLTFSaveOptions(FileFormat.GLTF2){SaveExtras = true});

{{< /highlight >}}

Questo codice di esempio salverà la scena con le proprietà personalizzate in FBX, glTF e glTF 2.0.
#### **Aggiunge due membri alla classe Aspose.ThreeD.Entities.PolygonModifier**
Questi membri sono utili, se gli sviluppatori non vogliono cambiare la trasformazione del nodo ma vogliono scalare le geometrie e si applicano solo alle geometrie.

**C#**

{{< highlight "java" >}}

 public static void Scale(Aspose.ThreeD.Scene scene, Aspose.ThreeD.Utilities.Vector3 scale)

public static void Scale(Aspose.ThreeD.Node node, Aspose.ThreeD.Utilities.Vector3 scale)

{{< /highlight >}}

**Codice del campione:**

**C#**

{{< highlight "java" >}}

 // scale the model in huge-scene.obj by 0.01 and save it to another file:

Scene scene = new Scene("huge-scene.obj");

PolygonModifier.Scale(scene, new Vector3(0.01));

scene.Save("scaled-scene.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **Aggiunge il metodo FindNode alla classe Aspose.ThreeD.Node**
Questo è un metodo pratico per trovare un nodo figlio in base al nome, restituirà null se non è possibile trovare un nodo.

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("child", new Box());

Node child = scene.RootNode.FindNode("child");

{{< /highlight >}}
#### **Esempi di utilizzo**
Controlla l'elenco degli argomenti di aiuto aggiunti o aggiornati nei documenti Wiki Aspose.3D:

1. [Manipolare le proprietà personalizzate di una scena 3D](/3d/it/net/manipulate-custom-properties-of-a-3d-scene/)
1. [Geometrie in scala di una scena 3D](/3d/it/net/scale-geometries-of-a-3d-scene/)
