---
title: Aspose.3D for .NET 17.6 Note di rilascio
type: docs
weight: 70
url: /it/net/aspose-3d-for-net-17-6-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 17.6](https://www.nuget.org/packages/Aspose.3D/17.6.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-257|Esporta la scena 3D in file GLTF 2.0 ASCII|Nuova funzionalità|
|THREEDNET-258|Esporta la scena 3D in GLTF 2.0 File binari|Nuova funzionalità|
|THREEDNET-264|I modelli hanno tangente ma non hanno un doppio normale non verranno resi correttamente|Bug|
|THREEDNET-267|I materiali nei file Collada potrebbero non essere caricati correttamente.|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge il membro MaterialConverter allo Aspose.ThreeD.Formats.GLTFSaveOptions Class**
GLTF 2.0 supporta solo materiali PBR, Aspose.3D convertirà internamente materiali non PBR in materiali PBR prima di esportare in GLTF 2.0 (i materiali nella scena rimarranno invariati durante l'esportazione) e l'utente può fornire la funzione di conversione personalizzata per sovrascrivere il comportamento predefinito.

Questo esempio di codice mostra come convertire il materiale in materiale PBR e quindi salvare la scena 3D nel formato GLTF 2.0:

**.NET, C#**

{{< highlight "java" >}}

 var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = delegate(Material material)

{

    PhongMaterial m = (PhongMaterial) material;

    return new PbrMaterial() {Albedo = new Vector3(m.DiffuseColor.x, m.DiffuseColor.y, m.DiffuseColor.z)};

};

s.Save("test.gltf", opt);

{{< /highlight >}}
### **Esempi di utilizzo**
Controlla l'elenco degli argomenti di aiuto aggiunti o aggiornati nei documenti Wiki Aspose.3D:

1. [Personalizzare la conversione dei materiali da PBR a PBR prima di salvare le scene da 3D al formato 2.0 GLTF](/3d/it/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/)
