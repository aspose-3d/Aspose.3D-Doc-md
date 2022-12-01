---
title: Öffentlich API Änderungen in Aspose.3D 17.01
type: docs
weight: 20
url: /de/net/public-api-changes-in-aspose-3d-17-01/
---
**Inhalts übersicht**

- [Fügt PLY Format-Eintrag in der Aspose.ThreeD.FileFormat-Klasse hinzu](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [Importieren von PLY-Dateien](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [Fügt Aspose.ThreeD.Global Transform-Klasse hinzu](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [Fügt Aspose.ThreeD.Node Class eine GlobalTransform-Eigenschaft hinzu](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [Fügt Polygons-Eigenschaft zu Aspose.ThreeD. Entitäten. Mesh-Klasse hinzu](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [Laden Sie 3D Datei und schreiben Sie Maschen im benutzer definierten binären Format](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [Entfernt Create Stream member von Aspose.ThreeD. Formate. IOConfig Class](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

In diesem Dokument werden Änderungen an Aspose.3D API von Version 16.12.0 bis 17.1.0 beschrieben, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung etwaiger Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
### **Fügt PLY Format-Eintrag in der Aspose.ThreeD.FileFormat-Klasse hinzu**
Zu Lade zwecken haben wir einen Eintrag im Format PLY hinzugefügt.
### **Importieren von PLY-Dateien**
Mit der aktuellen Version (17.01) oder höher können Entwickler PLY-Dateien importieren. Der Eintrag im Format PLY wird zum Laden hinzugefügt.

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
### **Fügt Aspose.ThreeD.Global Transform-Klasse hinzu**
Die GlobalTransform-Klasse bietet genau dieselbe Schnitts telle wie Transform, aber alle Eigenschaften sind schreib bar. Es ist nützlich für die Zwecke der globalen Transformation.
### **Fügt Aspose.ThreeD.Node Class eine GlobalTransform-Eigenschaft hinzu**
Es ermöglicht den Zugriff auf die globale Transformation des Knotens. Dies ist nützlich, um die Szene in das benutzer definierte Dateiformat des Benutzers umzuwandeln.
### **Fügt Polygons-Eigenschaft zu Aspose.ThreeD. Entitäten. Mesh-Klasse hinzu**
Es ermöglicht, alle Polygone innerhalb des Netzes zu erhalten. Jedes Polygon ist ein Array eines Polygon-Scheitel punkt index. Vor dieser Eigenschaft müssen wir die Foreach-Syntax verwenden, um jedes Polygon aufzuzählen, das ineffizient ist.
### **Laden Sie 3D Datei und schreiben Sie Maschen im benutzer definierten binären Format**
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
### **Entfernt Create Stream member von Aspose.ThreeD. Formate. IOConfig Class**
Dies wurde in Version 16.11.0 als veraltet markiert. Die neue Schnitts telle FileS ystem wurde in Version 16.11.0 eingeführt, die mehr Erweiterbar keit bietet.

