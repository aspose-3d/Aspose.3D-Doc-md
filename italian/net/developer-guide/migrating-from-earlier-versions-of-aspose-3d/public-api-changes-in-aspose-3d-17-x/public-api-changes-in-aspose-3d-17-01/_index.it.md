---
title: Pubblico API Modifiche nel Aspose.3D 17.01
type: docs
weight: 20
url: /it/net/public-api-changes-in-aspose-3d-17-01/
---
**Contenuto sommario**

- [Aggiunge la voce del formato PLY nella classe Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [Importazione di file PLY](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [Aggiunge Aspose.ThreeD. Classe GlobalTransform](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [Aggiunge una proprietà GlobalTransform a Aspose.ThreeD.Node Class](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [Aggiunge la proprietà Polygons a Aspose.ThreeD.Entities.Mesh Class](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [Caricare il file 3D e scrivere le maglie in formato binario personalizzato](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [Rimuove il membro CreateStream da Aspose.ThreeD.Formats.IOConfig Class](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.3D API dalla versione 16.12.0 alla 17.1.0, che potrebbero essere di interesse per gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte nello Aspose.3D.

{{% /alert %}} 
### **Aggiunge la voce del formato PLY nella classe Aspose.ThreeD.FileFormat**
Abbiamo aggiunto una voce in formato PLY a scopo di caricamento.
### **Importazione di file PLY**
Utilizzando la versione recente (17.01) o superiore, gli sviluppatori possono importare i file PLY. La voce del formato PLY viene aggiunta ai fini del caricamento.

**C#**

{{< highlight "java" >}}

 // an entry of PLY file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat PLY;

// initialize Scene class object

Scene scene = new Scene();

// initialize an object

PlyLoadOptions loadPLYOpts = new PlyLoadOptions();

// Flip the coordinate system.

loadPLYOpts.FlipCoordinateSystem = true;

// load 3D Ply model

scene.Open( "3DPlyModel.ply", loadPLYOpts);

{{< /highlight >}}
### **Aggiunge Aspose.ThreeD. Classe GlobalTransform**
La classe GlobalTransform fornisce esattamente la stessa interfaccia come Transform, ma tutte le sue proprietà sono di sola lettura. È utile per gli scopi della trasformazione globale.
### **Aggiunge una proprietà GlobalTransform a Aspose.ThreeD.Node Class**
Permette di accedere alla trasformazione globale del nodo. Questo è utile per trasformare la scena nel formato di file personalizzato dell'utente.
### **Aggiunge la proprietà Polygons a Aspose.ThreeD.Entities.Mesh Class**
Permette di ottenere tutti i poligoni all'interno della mesh, ogni poligono è un array di indice dei vertici poligonali. Prima di questa proprietà, dobbiamo usare la sintassi foreach per enumerare ogni poligono che è inefficiente.
### **Caricare il file 3D e scrivere le maglie in formato binario personalizzato**
**C#**

{{< highlight "java" >}}

 string = @"c:\temp\input.stl", output = @"c:\temp\output";

// load a 3D file

Scene scene = new Scene(input);

/*

\* 3D format demonstration is simple

\* 

\* struct File {

\*   MeshBlock blocks[];

\* };

\*

\* struct Vertex {

\*   float x;

\*   float y;

\*   float z;

\* };

\* 

\* struct Triangle {

\*   int a;

\*   int b;

\*   int c;

\* };

\* 

\* struct MeshBlock {

\*   int numControlPoints;

\*   int numTriangles;

\*   Vertex vertices[numControlPoints];

\*   Triangle faces[numTriangles];

\* };

*/

// open file for writing in binary mode

using (var writer = new BinaryWriter(new FileStream(output, FileMode.Create, FileAccess.Write)))

{

    // visit each descent nodes

    scene.RootNode.Accept(delegate (Node node)

    {

        foreach (Entity entity in node.Entities)

        {

            // only convert meshes, lights/camera and other stuff will be ignored

            if (!(entity is IMeshConvertible))

                continue;

            Mesh m = ((IMeshConvertible)entity).ToMesh();

            var controlPoints = m.ControlPoints;

            // triangulate the mesh, so triFaces will only store triangle indices

            int[][] triFaces = PolygonModifier.Triangulate(controlPoints, m.Polygons);

            // gets the global transform matrix

            Matrix4 transform = node.GlobalTransform.TransformMatrix;

            // write number of control points and triangle indices

            writer.Write(controlPoints.Count);

            writer.Write(triFaces.Length);

            // write control points

            for (int i = 0; i < controlPoints.Count; i++)

            {

                // calculate the control points in world space and save them to file

                var cp = transform * controlPoints[i];

                writer.Write((float)cp.x);

                writer.Write((float)cp.y);

                writer.Write((float)cp.z);

            }

            // write triangle indices

            for (int i = 0; i < triFaces.Length; i++)

            {

                writer.Write(triFaces[i][0]);

                writer.Write(triFaces[i][1]);

                writer.Write(triFaces[i][2]);

            }

        }

        return true;

    });

}

{{< /highlight >}}
### **Rimuove il membro CreateStream da Aspose.ThreeD.Formats.IOConfig Class**
Questo è stato contrassegnato come obsoleto nella versione 16.11.0, la nuova interfaccia FileSystem è stata introdotta nella versione 16.11.0 che fornisce maggiore estensibilità.

