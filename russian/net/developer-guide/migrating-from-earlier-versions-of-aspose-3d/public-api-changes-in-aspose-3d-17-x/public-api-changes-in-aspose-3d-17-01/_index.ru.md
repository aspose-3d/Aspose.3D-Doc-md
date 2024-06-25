---
title: Публичные изменения API в Aspose.3D 17,01
type: docs
weight: 20
url: /ru/net/public-api-changes-in-aspose-3d-17-01/
---
**Содержание Резюме**

- [Добавляет запись формата PLY в класс Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [Импорт файлов PLY](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [Добавляет класс Aspose.ThreeD.GlobalTransform](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [Добавляет свойство GlobalTransform в класс Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [Добавляет свойство полигонов в Aspose.ThreeD. Сущности. Класс сетки](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [Загрузите файл 3D и запишите сетки в настраиваемый двоичный формат](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [Удаляет участника CreateStream из Aspose.ThreeD. Форматы. Класс IOConfig](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 16.12.0 до 17.1.0, которые могут представлять интерес для разработчиков модулей/приложений. Она включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
###  **Добавляет запись формата PLY в класс Aspose.ThreeD.FileFormat**
Мы добавили запись в формате PLY для целей загрузки.
###  **Импорт файлов PLY**
Используя последнюю версию (17,01) или выше, разработчики могут импортировать файлы PLY. Запись в формате PLY добавляется для целей загрузки.

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
###  **Добавляет класс Aspose.ThreeD.GlobalTransform**
Класс GlobalTransform предоставляет точно такой же интерфейс, как Transform, но все его свойства доступны только для чтения. Это полезно для целей глобального преобразования.
###  **Добавляет свойство GlobalTransform в класс Aspose.ThreeD.Node**
Это позволяет получить доступ к глобальному преобразованию узла. Это полезно для преобразования сцены в пользовательский формат файла пользователя.
###  **Добавляет свойство полигонов в Aspose.ThreeD. Сущности. Класс сетки**
Это позволяет получить все многоугольники внутри сетки, каждый многоугольник представляет собой массив индекса вершин многоугольника. Перед этим свойством мы должны использовать для каждого синтаксиса, чтобы перечислить каждый многоугольник, который неэффективен.
###  **Загрузите файл 3D и запишите сетки в настраиваемый двоичный формат**
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
###  **Удаляет участника CreateStream из Aspose.ThreeD. Форматы. Класс IOConfig**
Он был отмечен как устаревший в версии 16.11.0, новый интерфейс FileSystem был представлен в версии 16.11.0, что обеспечивает большую расширяемость.

