﻿---
title: Aspose.3D for .NET 20.4 Note di rilascio
type: docs
weight: 40
url: /it/net/aspose-3d-for-net-20-4-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 20.4.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-663 |` `Aggiungere il supporto per il rendering Linux|` `Nuova funzionalità|
|THREEDNET-661 |` `Ottieni dati con VertexDeclaration personalizzata|` ` Potenziamento|
|THREEDNET-652 |` `Aggiungi controllo del movimento orbitale|` ` Potenziamento|
|THREEDNET-653 |` `Aggiungi supporto di linea nel formato A3DW.|` ` Potenziamento|
|THREEDNET-655 |` `Aggiungere il supporto di rendering di TriMesh|` ` Potenziamento|
|THREEDNET-656 |` ` Il rendering leggero non era corretto nel renderer web.|` `Bug|
## **Pubblico API e modifiche incompatibili arretrate**
### **Utenti aggiunti alla classe Aspose.ThreeD.Utilities.Vertex**
{{< highlight "java" >}}

 /// <summary>

/// Read the vector4 field

/// </summary>

/// <param name="field">The field with a Vector4/FVector4 data type</param>

/// <returns></returns>

public Aspose.ThreeD.Utilities.Vector4 ReadVector4(Aspose.ThreeD.Utilities.VertexField field)


/// <summary>

/// Read the vector4 field

/// </summary>

/// <param name="field">The field with a Vector4/FVector4 data type</param>

/// <returns></returns>

public Aspose.ThreeD.Utilities.FVector4 ReadFVector4(Aspose.ThreeD.Utilities.VertexField field)


/// <summary>

/// Read the vector3 field

/// </summary>

/// <param name="field">The field with a Vector3/FVector3 data type</param>

/// <returns></returns>

public Aspose.ThreeD.Utilities.Vector3 ReadVector3(Aspose.ThreeD.Utilities.VertexField field)


/// <summary>

/// Read the vector3 field

/// </summary>

/// <param name="field">The field with a Vector3/FVector3 data type</param>

/// <returns></returns>

public Aspose.ThreeD.Utilities.FVector3 ReadFVector3(Aspose.ThreeD.Utilities.VertexField field)


/// <summary>

/// Read the vector2 field

/// </summary>

/// <param name="field">The field with a Vector2/FVector2 data type</param>

/// <returns></returns>

public Aspose.ThreeD.Utilities.Vector2 ReadVector2(Aspose.ThreeD.Utilities.VertexField field)


/// <summary>

/// Read the vector2 field

/// </summary>

/// <param name="field">The field with a Vector2/FVector2 data type</param>

/// <returns></returns>

public Aspose.ThreeD.Utilities.FVector2 ReadFVector2(Aspose.ThreeD.Utilities.VertexField field)


/// <summary>

/// Read the double field

/// </summary>

/// <param name="field">The field with a float/double compatible data type</param>

/// <returns></returns>

public double ReadDouble(Aspose.ThreeD.Utilities.VertexField field)


/// <summary>

/// Read the double field

/// </summary>

/// <param name="field">The field with a float/double compatible data type</param>

/// <returns></returns>

public float ReadFloat(Aspose.ThreeD.Utilities.VertexField field)

{{< /highlight >}}
#### **Esempio di utilizzo**
{{< highlight "java" >}}

 Scene s = new Scene(@"test.stl");

var mesh = (Mesh)s.RootNode.ChildNodes[0].Entity;

//create a VertexDeclaration so we can get the TriMesh with memory layout exactly we want.

var vd = new VertexDeclaration();

var pos = vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Position);

var normal = vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Normal);

var uv = vd.AddField(VertexFieldDataType.FVector2, VertexFieldSemantic.UV);

//construct the TriMesh using specified vertex layout

var m = TriMesh.FromMesh(vd, mesh);

//print each vertex's position, normal and uv

foreach(var vtx in m)

{

    var v_pos = vtx.ReadVector3(pos);

    var v_normal = vtx.ReadVector3(normal);

    var v_uv = vtx.ReadVector2(uv);

        Console.WriteLine($"({v_pos}), ({v_uv}), ({v_normal})");

}

{{< /highlight >}}
### **Membro aggiunto alla classe Aspose.ThreeD.Entities.TriMesh**
Se le istanze TriMesh presentano un layout di memoria incerto, potete utilizzare questo metodo per costruire una nuova istanza con il layout di memoria esattamente necessario.

{{< highlight "java" >}}

 /// <summary>

/// Copy the <see cref="TriMesh"/> from input with new vertex layout

/// </summary>

/// <param name="input">The input TriMesh for copying</param>

/// <param name="vd">The new vertex delcaration of the output TriMesh</param>

/// <returns>A new TriMesh instance with new vertex declaration.</returns>

public static Aspose.ThreeD.Entities.TriMesh CopyFrom(Aspose.ThreeD.Entities.TriMesh input, Aspose.ThreeD.Utilities.VertexDeclaration vd)

{{< /highlight >}}
#### **Esempio di utilizzo**
{{< highlight "java" >}}

 Scene s = new Scene(@"test.STL");

var mesh = (Mesh)s.RootNode.ChildNodes[0].Entity;

var originalTriMesh = TriMesh.FromMesh(mesh);

//If the original TriMesh's memory layout is not what you wanted, you can use CopyFrom to get a new instance

//with specified memory layout

var vd = new VertexDeclaration();

var pos = vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Position);

var normal = vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Normal);

var uv = vd.AddField(VertexFieldDataType.FVector2, VertexFieldSemantic.UV);

var m = TriMesh.CopyFrom(originalTriMesh, vd);

foreach(var vtx in m)

{

    //Field's offset in vertex can be retrieved by VertexField.Offset 

    var v_pos = vtx.ReadVector3(pos);

    var v_normal = vtx.ReadVector3(normal);

    var v_uv = vtx.ReadVector2(uv);

        Console.WriteLine($"({v_pos}), ({v_uv}), ({v_normal})");

}

{{< /highlight >}}
### **Membro aggiunto alla classe Aspose.ThreeD.Entities.TriMesh**
Con questo metodo, è possibile ricostruire facilmente l'istanza TriMesh da un array di byte, come la deserializzazione.

{{< highlight "java" >}}

 /// <summary>

/// Create TriMesh from raw data

/// </summary>

/// <param name="vd">Vertex declaration, must contains at least one field.</param>

/// <param name="vertices">The input vertex data, the minimum length of the vertices must be greater or equal to vertex declaration's size</param>

/// <param name="indices">The triangle indices</param>

/// <param name="generateVertexMapping">Generate <see cref="Vertex"/> for each vertex, which is not necessary for just serialization/deserialization.</param>

/// <returns>The <see cref="TriMesh"/> instance that encapsulated the input byte array.</returns>

/// <remarks>The returned TriMesh will not copy the input byte array for performance, external changes on the array will be reflected to this instance.</remarks>

public static Aspose.ThreeD.Entities.TriMesh FromRawData(Aspose.ThreeD.Utilities.VertexDeclaration vd, byte[]vertices, int[]indices, bool generateVertexMapping)

{{< /highlight >}}
#### **Esempio di utilizzo**
{{< highlight "java" >}}

 Scene s = new Scene(@"test.STL");

var mesh = (Mesh)s.RootNode.ChildNodes[0].Entity;

var vd = new VertexDeclaration();

var pos = vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Position);

var normal = vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Normal);

var uv = vd.AddField(VertexFieldDataType.FVector2, VertexFieldSemantic.UV);

var originalTriMesh = TriMesh.FromMesh(vd, mesh);

//If the original TriMesh's memory layout is not what you wanted, you can use CopyFrom to get a new instance

//with specified memory layout

byte[]verticesInBytes = originalTriMesh.VerticesToArray();

int[]indices;

originalTriMesh.IndicesToArray(out indices);

var m = TriMesh.FromRawData(vd, verticesInBytes, indices, true);

foreach(var vtx in m)

{

    //Field's offset in vertex can be retrieved by VertexField.Offset 

    var v_pos = vtx.ReadVector3(pos);

    var v_normal = vtx.ReadVector3(normal);

    var v_uv = vtx.ReadVector2(uv);

    Console.WriteLine($"({v_pos}), ({v_uv}), ({v_normal})");

}

{{< /highlight >}}
### **Aggiunta la classe Aspose.ThreeD.Render. Maniglia per finestre**
Viene utilizzato per incapsulare la maniglia finestra nativa per la creazione di una finestra di rendering.
### **Membro aggiunto alla classe Aspose.ThreeD.Render.RenderFactory**


{{< highlight "java" >}}

 /// <summary>

/// Create a render target that renders to the native window.

/// </summary>

/// <param name="parameters">Render parameters to create the render window</param>

/// <param name="handle">The handle of the window to render</param>

/// <returns></returns>

public Aspose.ThreeD.Render.IRenderWindow CreateRenderWindow(Aspose.ThreeD.Render.RenderParameters parameters, Aspose.ThreeD.Render.WindowHandle handle)

{{< /highlight >}}
### **Membro obsoleto**
Il vecchio CreateRenderWindow è contrassegnato come Obsoleted, per portare il vecchio codice su questo metodo, correggi il tuo vecchio codice come il seguente frammento di codice:

{{< highlight "java" >}}

  //Renderer renderer = ... your renderer instance

//RenderParameters renderParameters = ... your render parameters

//Control control = ... your control for rendering.

//renderer.RenderFactory.CreateRenderWindow(renderParameters, control.Handle);

//The above code should be fixed like the following line, pass a Win32 handle.

renderer.RenderFactory.CreateRenderWindow(renderParameters, WindowHandle.FromWin32(control.Handle));

{{< /highlight >}}
### **Aggiunti membri alla classe Aspose.ThreeD.Utilities.IOUtils**
Questi sono metodi di estensione per scrivere Vector2/Vector3 in BinaryWriter.



{{< highlight "java" >}}

 /// <summary>

/// Write the vector to the binary writer

/// </summary>

/// <param name="writer">Target binary writer</param>

/// <param name="v">Vector to write</param>

public static void Write(this System.IO.BinaryWriter writer, Aspose.ThreeD.Utilities.Vector2 v)

/// <summary>

/// Write the vector to the binary writer

/// </summary>

/// <param name="writer">Target binary writer</param>

/// <param name="v">Vector to write</param>

public static void Write(this System.IO.BinaryWriter writer, Aspose.ThreeD.Utilities.Vector3 v)

{{< /highlight >}}
### **Aggiunti membri alla classe Aspose.ThreeD.Utilities.Vector3**


{{< highlight "java" >}}

 /// <summary>

/// Calculate the inner angle between two direction

/// Two direction can be non-normalized vectors

/// </summary>

/// <param name="dir">The direction vector to compare with</param>

/// <param name="up">The up vector of the two direction's shared plane</param>

/// <returns>inner angle in radian</returns>

public double AngleBetween(Aspose.ThreeD.Utilities.Vector3 dir, Aspose.ThreeD.Utilities.Vector3 up)

/// <summary>

/// Calculate the inner angle between two direction

/// Two direction can be non-normalized vectors

/// </summary>

/// <param name="dir">The direction vector to compare with</param>

/// <returns>inner angle in radian</returns>

public double AngleBetween(Aspose.ThreeD.Utilities.Vector3 dir)

{{< /highlight >}}