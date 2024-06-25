---
title: Публичные изменения API в Aspose.3D 1.2.0
type: docs
weight: 50
url: /ru/net/public-api-changes-in-aspose-3d-1-2-0/
---
**Содержание Резюме**

- [Настройте цель и камеру в файле 3D](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
- [Перевернуть систему координат в форматах 3D](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
- [Как триангулировать сетку](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 1.1.0 до 1.2.0, которые могут представлять интерес для разработчиков модулей/приложений. Она включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
###  **Настройте цель и камеру в файле 3D**
В некоторых форматах файлов свет/камера поддерживает цель, что позволяет свету/камере всегда обращаться к указанному узлу, это полезно в анимации. Пример кода:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());

cameraNode.Transform.Translation = new Vector3(100, 20, 0);

cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");

scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);

{{< /highlight >}}

###  **Перевернуть систему координат в форматах 3D**
(THREEDNET-123) -Разрешить пользователю переворачивать систему координат в OBJ/3DS/STL. Пример кода:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });

scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });

{{< /highlight >}}

###  **Как триангулировать сетку**
Треугольная сетка полезна для игровой индустрии, потому что треугольная-единственный поддерживаемый примитив, который поддерживает оборудование GPU (нетреугольные данные триангулированы на уровне драйвера, что неэффективно при рендеринге в реальном времени). Пример кода:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

 scene.Open(@"d:\\cube.fbx");

 scene.RootNode.Accept(delegate (Node node)

 {

   Mesh mesh = node.GetEntity<Mesh>();

        if (mesh != null)

        {

            //triangulate the mesh

            Mesh newMesh = PolygonModifier.Triangulate(mesh);

            //replace the old mesh

            node.Entity = mesh;

        }

   return true;

  });

 scene.Save(@"d:\cube-tri.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}

