---
title: Público API Cambios en Aspose.3D 17,01
type: docs
weight: 20
url: /es/net/public-api-changes-in-aspose-3d-17-01/
---
**Resumen de contenidos**

- [Agrega una entrada de formato PLY en la clase Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [Importación de archivos PLY](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [Agrega Aspose.ThreeD.GlobalTransform Class](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [Agrega una propiedad GlobalTransform a la clase Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [Agrega la propiedad Polygons a Aspose.ThreeD.Entities.Mesh Class](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [Cargar mallas de archivo y escritura 3D en formato binario personalizado](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [Elimina el miembro CreateStream de la clase Aspose.ThreeD.Formats.IOConfig](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 16.12.0 to 17.1.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Agrega una entrada de formato PLY en la clase Aspose.ThreeD.FileFormat**
Hemos añadido una entrada de formato PLY para fines de carga.
###  **Importación de archivos PLY**
Con la versión reciente (17,01) o superior, los desarrolladores pueden importar archivos PLY. La entrada de formato PLY se agrega para fines de carga.

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
###  **Agrega Aspose.ThreeD.GlobalTransform Class**
La clase GlobalTransform proporciona exactamente la misma interfaz como Transform, pero todas sus propiedades son de solo lectura. Es útil para los propósitos de transformación global.
###  **Agrega una propiedad GlobalTransform a la clase Aspose.ThreeD.Node**
Permite acceder a la transformación global del nodo. Esto es útil para transformar la escena en el formato de archivo personalizado del usuario.
###  **Agrega la propiedad Polygons a Aspose.ThreeD.Entities.Mesh Class**
Permite que todos los polígonos entren en la malla, cada polígono es una matriz de índice de vértice de polígono. Antes de esta propiedad, tenemos que usar la sintaxis de foreach para enumerar cada polígono que es ineficiente.
###  **Cargar mallas de archivo y escritura 3D en formato binario personalizado**
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
###  **Elimina el miembro CreateStream de la clase Aspose.ThreeD.Formats.IOConfig**
Esto se marcó como obsoleto en la versión 16.11.0, la nueva interfaz FileSystem se introdujo en la versión 16.11.0 que proporciona más extensibilidad.

