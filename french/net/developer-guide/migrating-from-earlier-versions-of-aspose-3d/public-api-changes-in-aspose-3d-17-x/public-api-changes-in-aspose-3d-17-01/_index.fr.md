---
title: Public API Changements dans Aspose.3D 17.01
type: docs
weight: 20
url: /fr/net/public-api-changes-in-aspose-3d-17-01/
---
**Résumé du contenu**

- [Ajoute une entrée de format PLY dans la classe Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [Importation de fichiers PLY](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [Ajoute la classe Aspose.ThreeD.GlobalTransform](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [Ajoute une propriété GlobalTransform à Aspose.ThreeD.Node Class](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [Ajoute la propriété Polygons à Aspose.ThreeD.Entities.Mesh Class](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [Charger 3D Fichier et écrire des maillages au format binaire personnalisé](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [Supprime le membre CreateStream de la classe Aspose.ThreeD.Formats.IOConfig](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées à Aspose.3D API de la version 16.12.0 à la version 17.1.0, qui peuvent intéresser les développeurs de modules/applications. Il inclut non seulement des méthodes publiques nouvelles et mises à jour, mais aussi une description de tout changement de comportement dans les coulisses de Aspose.3D.

{{% /alert %}} 
###  **Ajoute une entrée de format PLY dans la classe Aspose.ThreeD.FileFormat**
Nous avons ajouté une entrée de format PLY à des fins de chargement.
###  **Importation de fichiers PLY**
En utilisant la version récente (17.01) ou supérieure, les développeurs peuvent importer des fichiers PLY. L'entrée de format PLY est ajoutée à des fins de chargement.

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
###  **Ajoute la classe Aspose.ThreeD.GlobalTransform**
La classe GlobalTransform fournit exactement la même interface comme Transform, mais toutes ses propriétés sont en lecture seule. Il est utile à des fins de transformation globale.
###  **Ajoute une propriété GlobalTransform à Aspose.ThreeD.Node Class**
Il permet d'accéder à la transformée globale du nœud. Ceci est utile pour transformer la scène dans le format de fichier personnalisé de l'utilisateur.
###  **Ajoute la propriété Polygons à Aspose.ThreeD.Entities.Mesh Class**
Il permet d'obtenir tous les polygones à l'intérieur du maillage, chaque polygone est un tableau d'indice de sommets polygonaux. Avant cette propriété, nous devons utiliser la syntaxe foreach pour énumérer chaque polygone qui est inefficace.
###  **Charger 3D Fichier et écrire des maillages au format binaire personnalisé**
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
###  **Supprime le membre CreateStream de la classe Aspose.ThreeD.Formats.IOConfig**
Cela a été marqué comme obsolète dans la version 16.11.0, la nouvelle interface FileSystem a été introduite dans la version 16.11.0 qui offre plus d'extensibilité.

