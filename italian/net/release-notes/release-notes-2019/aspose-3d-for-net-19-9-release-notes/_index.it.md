---
title: Aspose.3D for .NET 19.9 Note di rilascio
type: docs
weight: 40
url: /it/net/aspose-3d-for-net-19-9-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 19.9](/3d/it/net/aspose-3d-for-net-19-9-release-notes/)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-532|Esporta la scena 3D allo HTML|Nuova funzione|
|THREEDNET-561|Esporre le proprietà geometriche di trasformazione|Miglioramento|
|THREEDNET-556|La rotazione geometrica sembra errata|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **Aggiunti nuovi formati di file HTML5/Aspose3DWeb**
{{< highlight "java" >}}

 /// <summary>

/// Aspose.3D Web format.

/// </summary>

public static readonly FileFormat Aspose3DWeb;

/// <summary>

/// HTML5 File

/// </summary>

public static readonly FileFormat HTML5;

{{< /highlight >}}

Quando si esporta la scena nel file HTML5, ci saranno in realtà 3 file, un file HTML, un file DWeb Aspose3 (*.a3dw) e un file JavaScript renderizzato, è possibile esportare il file a3dw solo specificando DWeb Aspose3 come tipo di esportazione e riutilizzare il file javascript all'interno della propria pagina HTML.

Codice del campione:

{{< highlight "java" >}}

 var scene = new Scene();

var node = scene.RootNode.CreateChildNode(new Cylinder());

node.Material = new LambertMaterial() { DiffuseColor = new Vector3(Color.Chartreuse) };

scene.RootNode.CreateChildNode(new Light() { LightType = LightType.Point }).Transform.Translation = new Vector3(10, 0, 10);

scene.Save(@"test.html", FileFormat.HTML5);

{{< /highlight >}}

{{% alert color="primary" %}} 

A causa dei limiti di sicurezza del browser, il file HTML esportato non può essere aperto direttamente, è necessario aprirlo tramite un server Web, se è installato python3, è possibile avviare il server Web nella riga di comando nella directory esportata

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Allora aprilo<http://localhost:8000/test.html>. Il renderer web utilizza WebGL2, è possibile utilizzare<https://get.webgl.org/webgl2/>Per verificare se il tuo browser lo supporta o meno.
### **Aggiunta nuova classe Aspose.ThreeD. Formati. HTML5SaveOptions**
Questo permette di personalizzare la pagina 3D esportate HTML

Codice del campione:

{{< highlight "java" >}}

 var scene = new Scene();

var node = scene.RootNode.CreateChildNode(new Cylinder());

node.Material = new LambertMaterial() { DiffuseColor = new Vector3(Color.Chartreuse) };

scene.RootNode.CreateChildNode(new Light() { LightType = LightType.Point }).Transform.Translation = new Vector3(10, 0, 10);

var opt = new HTML5SaveOptions();

opt.ShowGrid = false;  //Turn off the grid

opt.ShowUI = false; //Turn off the user interface.

scene.Save(@"test.html", opt);

{{< /highlight >}}
### **Aggiunta nuova proprietà FileFormat nella classe Aspose.ThreeD. Formati. IOConfig**
{{< highlight "java" >}}

 /// <summary>

/// Gets the file format that specified in current Save/Load option.

/// </summary>

public FileFormat FileFormat { get; }

{{< /highlight >}}
### **Aggiunto nuovo metodo EvaluateGlobalTransform in classe Aspose.ThreeD.Node**
{{< highlight "java" >}}

 /// <summary>

/// Evaluate the global transform, include the geometric transform or not.

/// </summary>

/// <param name="withGeometricTransform">Whether the geometric transform is needed.</param>

/// <returns></returns>

public Matrix4 EvaluateGlobalTransform(bool withGeometricTransform);

{{< /highlight >}}

La differenza tra Node.GlobalTransform.TransformMatrix è che consente di ottenere una matrice di trasformazione con una trasformata geometrica, che influisce solo sull'entità collegata e mantiene inalterati i nodi figlio.
### **Aggiunte nuove proprietà GeometricTranslation/GeometricScaling/GeometricRotation nella classe Aspose.ThreeD.Transform**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the geometric translation. 

/// Geometric transformation only affects the entities attached and leave the child nodes unaffected.

/// It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

/// </summary>

public Vector3 GeometricTranslation {get; set;}

/// <summary>

/// Gets or sets the geometric scaling. 

/// Geometric transformation only affects the entities attached and leave the child nodes unaffected.

/// It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

/// </summary>

public Vector3 GeometricScaling {get; set;}

/// <summary>

/// Gets or sets the geometric euler rotation(measured in degree). 

/// Geometric transformation only affects the entities attached and leave the child nodes unaffected.

/// It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

/// </summary>

public Vector3 GeometricRotation {get; set; }

{{< /highlight >}}

Codice del campione:

{{< highlight "java" >}}

 var n = new Node();

n.Transform.GeometricTranslation = new Vector3(10, 0, 0);

Console.WriteLine(n.EvaluateGlobalTransform(true));

Console.WriteLine(n.EvaluateGlobalTransform(false));

{{< /highlight >}}

La prima Console.WriteLine emetterà la matrice di trasformazione che include la trasformazione geometrica mentre la seconda no.
