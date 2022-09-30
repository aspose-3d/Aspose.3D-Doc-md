---
title: Aspose.3D for .NET 19.6 Note di rilascio
type: docs
weight: 70
url: /it/net/aspose-3d-for-net-19-6-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 19.6](https://www.nuget.org/packages/Aspose.3D/19.6.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-511|Migliora la creazione del cilindro|Nuova funzione|
|THREEDNET-507|Perdi alcuni materiali durante l'apertura del file RVM|Bug|
|THREEDNET-508|Il sistema potrebbe non riuscire ad allocare il set di descrittori a volte nel renderer Vulkan|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
#### **Aggiunta nuova proprietà OffsetTop in classe Aspose.ThreeD.Entities.Cylinder**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the vertices transformation offset of the top side.

/// </summary>

public Vector3 OffsetTop

{

    get;

    set;

}

{{< /highlight >}}
#### **Aggiunta nuova proprietà OffsetBottom nella classe Aspose.ThreeD.Entities.Cylinder**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the vertices transformation offset of the bottom side.

/// </summary>

public Vector3 OffsetBottom

{

    get;

    set;

}

{{< /highlight >}}

Codice di esempio per generare un cilindro con OffsetTop personalizzato:

{{< highlight "java" >}}

 Scene scene = new Scene();

var fan = new Cylinder(2, 2, 10, 20, 1, false);

fan.OffsetTop = new Vector3(5, 3, 0);

scene.RootNode.CreateChildNode(fan).Transform.Translation = new Vector3(10, 0, 0);

var nonfan = new Cylinder(2, 2, 10, 20, 1, false);

scene.RootNode.CreateChildNode(nonfan);

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

Anteprima:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-19-6-release-notes_1.png)

Quello di sinistra ha**OffsetTop**Impostato su (5, 3, 0), è facile vedere che il tappo superiore si è spostato e anche l'intero busto ne viene influenzato.
#### **Aggiunta nuova proprietà GenerateFanCylinder nella classe Aspose.ThreeD. Entità. Cilindro**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets whether to generate the fan-style cylinder when the ThetaLength is less than 2*PI, otherwise the model will not be cut.

/// </summary>

public bool GenerateFanCylinder

{

    get;set;

}

{{< /highlight >}}

Codice di esempio per generare un cilindro stile ventola e un cilindro non a ventaglio:

{{< highlight "java" >}}

 Scene scene = new Scene();

var fan = new Cylinder(2, 2, 10, 20, 1, false);

fan.GenerateFanCylinder = true;

fan.ThetaLength = MathUtils.ToRadian(270);

scene.RootNode.CreateChildNode(fan).Transform.Translation = new Vector3(10, 0, 0);

var nonfan = new Cylinder(2, 2, 10, 20, 1, false);

nonfan.GenerateFanCylinder = false;

nonfan.ThetaLength = MathUtils.ToRadian(270);

scene.RootNode.CreateChildNode(nonfan);

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

Anteprima:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-19-6-release-notes_2.png)

Il cilindro sinistro ha GenerateFanCylinder = falso e quello destro ha GenerateFanCylinder = true.
#### **Aggiunta nuova proprietà ShearTop in classe Aspose.ThreeD. Entità. Cilindro**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets of the shear transform of the top side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

/// </summary>

public Vector2 ShearTop

{

    get;

    set;

}

{{< /highlight >}}
#### **Aggiunta nuova proprietà ShearBottom nella classe Aspose.ThreeD. Entità. Cilindro**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets of the shear transform of the bottom side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

/// </summary>

public Vector2 ShearBottom

{

    get;

    set;

}

{{< /highlight >}}

Codice di esempio per mostrare l'uso di ShearBottom(ShearTop):

{{< highlight "java" >}}

 Scene scene = new Scene();

var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

cylinder1.ShearBottom = new Vector2(0, 0.83);// shear 47.5deg in xy plane(z-axis)

scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);

var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

scene.RootNode.CreateChildNode(cylinder2);

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

Anteprima:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-19-6-release-notes_3.png)

Il cilindro sinistro ha ShearBottom a (0, 0,83) mentre quello destro è un cilindro ordinale.
