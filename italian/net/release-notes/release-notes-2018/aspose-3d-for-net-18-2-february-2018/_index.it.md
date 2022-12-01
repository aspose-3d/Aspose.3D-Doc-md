---
title: Aspose.3D for .NET 18.2-Febbraio 2018
type: docs
weight: 110
url: /it/net/aspose-3d-for-net-18-2-february-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 18.2](https://www.nuget.org/packages/Aspose.3d/18.2.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-335|Implementare l'aggiunta di obiettivi a MorphChannel|Nuova funzionalità|
|THREEDNET-348|Aggiungere il supporto dell'esportazione di animazione scheletro/morphing|Nuova funzionalità|
|THREEDNET-332|Aggiungere il supporto per la curva NURBS|Nuova funzionalità|
|THREEDNET-333|Aggiungere il supporto per la superficie NURBS|Nuova funzionalità|
|THREEDNET-338|Aggiungere il supporto di pre/post rotazione|Nuova funzionalità|
|THREEDNET-351|Impossibile rendere la trasparenza sull'immagine PNG della scena|Miglioramento|
|THREEDNET-334|Uscita FBX-si è verificato l'errore del puntatore nullo|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge membri alla classe Aspose.ThreeD.Deformers.Bone**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets the weight for control point specified by index

/// </summary>

/// <param name="index">Control point's index</param>

/// <returns>the weight at specified index, or 0 if the index is invalid</returns>

public double GetWeight(int index)

/// <summary>

/// Sets the weight for control point specified by index

/// </summary>

/// <param name="index">Control point's index</param>

/// <param name="weight">New weight</param>

public void SetWeight(int index, double weight)

/// <summary>

/// Gets the count of weight, this is automatically extended by <see cref="SetWeight"/>

/// </summary>

int WeightCount{ get;}

/// <summary>

/// Gets or sets the transform matrix of the bone.

/// </summary>

Aspose.ThreeD.Utilities.Matrix4 BoneTransform{ get;set;}

{{< /highlight >}}
#### **Aggiunge i membri alla classe Aspose.ThreeD.Deformers.MorphTargetChannel**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets the weight for the specified target, if the target is not belongs to this channel, default value 0 is returned. 

/// </summary>

/// <param name="target"></param>

/// <returns></returns>

public double GetWeight(Aspose.ThreeD.Entities.Geometry target)

/// <summary>

/// Sets the weight for the specified target, default value is 1, range should between 0~1

/// </summary>

/// <param name="target"></param>

/// <param name="weight"></param>

public void SetWeight(Aspose.ThreeD.Entities.Geometry target, double weight)

{{< /highlight >}}
#### **Aggiunge membri nella classe Aspose.ThreeD.Entities.NurbsCurve**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Evaluate the nurbs curve

/// </summary>

/// <param name="steps">The evaluation frequency between two neighbor knots, default value is 20</param>

/// <returns>Points in the curve</returns>

public Aspose.ThreeD.Utilities.Vector4[]Evaluate(double delta)

/// <summary>

/// Evaluate the curve's point at specified position

/// </summary>

/// <param name="u">The position in the curve, between 0 and 1</param>

/// <returns></returns>

public Aspose.ThreeD.Utilities.Vector4 EvaluateAt(double u)

{{< /highlight >}}

**Codice del campione:**

**C#**

{{< highlight "java" >}}

 public static void Main(string[]args)

{

    NurbsCurve curve = new NurbsCurve();

    curve.ControlPoints.AddRange(new Vector4[]{

        new Vector4(-28.0118217468262, 53.0359077453613, 0, 1),

        new Vector4(8.95330429077148, 64.7735290527344, 0, 1),

        new Vector4(35.7778739929199, 42.424259185791, 0, 1),

        new Vector4(24.8725852966309, -4.86993026733398, 0, 1),

        new Vector4(-35.7778739929199, -34.192684173584, 0, 1),

        new Vector4(-18.6066780090332, -57.1458396911621, 0, 1),

        new Vector4(17.733715057373, -64.7735290527344, 0, 1)

    });

    curve.KnotVectors.AddRange(new double[]{0, 0, 0, 0, 0.25, 0.5, 0.75, 1, 1, 1, 1});

    foreach (var pt in curve.Evaluate())

    {

        Console.WriteLine(pt);

    }

}

{{< /highlight >}}
#### **Aggiunge i membri alla classe Aspose.ThreeD.Entities.NurbsCurve**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Convert the nurbs surface to the mesh

/// </summary>

/// <returns></returns>

public Aspose.ThreeD.Entities.Mesh ToMesh()

{{< /highlight >}}

{{% alert color="primary" %}} 

Con la recente versione 18.2 dello Aspose.3D for .NET, la superficie NURBS è ora in grado di rendere.

{{% /alert %}} {{% alert color="primary" %}} 

La superficie NURBS che ha una direzione periodica U/V non è ancora supportata, sarà supportata nelle versioni future.

{{% /alert %}}
#### **Aggiunge membri alla classe Aspose.ThreeD.Transform**
Alcuni file FBX contengono un valore di rotazione pre/post diverso da zero per i nodi, queste due proprietà li espone all'utente e consentono di manipolarli.

**C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the pre-rotation represented in degree

/// </summary>

Aspose.ThreeD.Utilities.Vector3 PreRotation{ get;set;}

/// <summary>

/// Gets or sets the post-rotation represented in degree

/// </summary>

Aspose.ThreeD.Utilities.Vector3 PostRotation{ get;set;}

{{< /highlight >}}
#### **Aggiunge i membri alla classe Aspose.ThreeD.Utilities.MathUtils**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Convert a number from radian to degree

/// </summary>

/// <param name="x">The x component in radian value.</param>

/// <param name="y">The y component in radian value.</param>

/// <param name="z">The z component in radian value.</param>

/// <returns>The degree value.</returns>

public static Aspose.ThreeD.Utilities.Vector3 ToDegree(double x, double y, double z)

/// <summary>

/// Convert a vector from degree to radian

/// </summary>

/// <param name="x">The x component in degree value.</param>

/// <param name="y">The y component in degree value.</param>

/// <param name="z">The z component in degree value.</param>

/// <returns>The radian value.</returns>

public static Aspose.ThreeD.Utilities.Vector3 ToRadian(double x, double y, double z)

{{< /highlight >}}

Il vecchio esempio di codice:

**C#**

{{< highlight "java" >}}

 MathUtils.ToDegree(new Vector3(x, y, z));

MathUtils.ToRadian(new Vector3(x, y, z));

{{< /highlight >}}

Ora può essere semplificato come:

**C#**

{{< highlight "java" >}}

 MathUtils.ToDegree(x, y, z);

MathUtils.ToRadian(x, y, z);

{{< /highlight >}}

{{% alert color="primary" %}} 

Le seguenti modifiche non dovrebbero apportare modifiche al codice sul lato utente, ma sono necessarie affinché la versione java mantenga coerente.

{{% /alert %}} 
#### **Membro aggiornato in Aspose.ThreeD. Formati. GLTFSaveOptions**
**Vecchia definizione**

{{< highlight "java" >}}

 System.Func<Aspose.ThreeD.Shading.Material, Aspose.ThreeD.Shading.Material> MaterialConverter{ get;set;}

{{< /highlight >}}

**Nuova definizione**

{{< highlight "java" >}}

 //New definition

Aspose.ThreeD.Formats.MaterialConverter MaterialConverter{ get;set;}

{{< /highlight >}}

La definizione di MaterialConverter ha la stessa firma per il vecchio Func<Material, Material>:

**C#**

{{< highlight "java" >}}

 /// <summary>

/// Custom converter to convert the geometry's original material to GLTF's PBR material.

/// </summary>

/// <param name="mat">Old material instance</param>

/// <returns>New material instance</returns>

public delegate Material MaterialConverter(Material mat);

{{< /highlight >}}
#### **Aggiunge una nuova classe Aspose.ThreeD.Entities.VertexElementVector4**
Questa classe è la nuova classe base di VertexElementNormal, VertexElementVertexColor, VertexElementBinormal, VertexElementTangent, VertexElementUV e VertexElementSpecular. Non influisce sul codice laterale dell'utente.
#### **Il membro viene modificato in Aspose.ThreeD. Entità. Classe NurbsCurve**
**Vecchia definizione**

{{< highlight "java" >}}

 System.Collections.Generic.List<double> KnotVectors{ get;}

{{< /highlight >}}

**Nuova definizione**

{{< highlight "java" >}}

 IArrayList<double> KnotVectors{ get;}

{{< /highlight >}}
#### **Il membro viene modificato in Aspose.ThreeD. Entità. Classe NurbsDirection**
**Vecchia definizione**

{{< highlight "java" >}}

 System.Collections.Generic.List<double> KnotVectors{ get;}

{{< /highlight >}}

**Nuova definizione**

{{< highlight "java" >}}

 IArrayList<double> KnotVectors{ get;}

{{< /highlight >}}
