---
title: Offentlig API Ändrar i Aspose.3D 17.01.
type: docs
weight: 20
url: /sv/net/public-api-changes-in-aspose-3d-17-01/
---
**Innehåll**

- [Adds PLY Format Entry in the Aspose.ThreeD.FileFormat Class](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [Importing PLY Files](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [Adds Aspose.ThreeD.GlobalTransform Class](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [Adds a GlobalTransform property to Aspose.ThreeD.Node Class](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [Adds Polygons property to Aspose.ThreeD.Entities.Mesh Class](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [Load 3D File and Write Meshes in Custom Binary Format](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [Removes CreateStream member from Aspose.ThreeD.Formats.IOConfig Class](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar i Aspose. 3D API från version 16.12. 0-17,1. 0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose. 3D.

{{% /alert %}} 
###  **Lägger till PLY Format Post i Aspose.ThreeD.FileFormat klass**
Vi har lagt till en post i PLY för lastning.
###  **Importerar PLY filer**
Genom att använda den senaste versionen (17.01) eller högre, kan utvecklare importera PLY-filer. Posten PLY-formatet läggs till för lastning.

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
###  **Lägger till Aspose.ThreeD.GlobalTransform Class.**
Klassen GlobalTransform ger exakt samma gränssnitt som Transform men alla dess egenskaper är skrivskyddade. Den är användbar för den globala omvandlingen.
###  **Lägger till en egenskap GlobalTransform till Aspose.ThreeD.Node Class.**
Det tillåter att komma åt nodens globala transformation. Detta är användbart för att omvandla scenen till användarens egna filformat.
###  **Lägger till egenskapen Polygons till Aspose.ThreeD.Entites.Mesh Class.**
Det tillåter att få alla polygoner inuti mesh, varje polygon är en array av polygon vertex index. Innan denna egenskap, måste vi använda foreach syntax för att räkna upp varje polygon som är ineffektiv.
###  **Ladda 3D Arkiv och skriva meshes i eget binärformat**
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
###  **Ta bort CreateStream-medlem från Aspose.ThreeD.Formats.IOConfig Class.**
Detta markerades som föråldrat i version 16.11.0, det nya gränssnittet FileSystem introducerades i version 16.11.0 som ger mer extensibilitet.

