---
title: Aspose.3D 1.2.0中的公共 API 更改
type: docs
weight: 50
url: /zh/net/public-api-changes-in-aspose-3d-1-2-0/
---
**内容摘要**

- [在 3D 文件中设置目标和相机](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
- [以 3D 格式翻转坐标系](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
- [如何三角剖分网格](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)

{{% alert color="primary" %}} 

本文档介绍了对 Aspose.3D API 从版本1.1.0到1.2.0的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
###  **在 3D 文件中设置目标和相机**
在某些文件格式中，light/camera支持目标，这允许light/camera始终面对指定的节点，这在动画中很有用。示例代码:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());

cameraNode.Transform.Translation = new Vector3(100, 20, 0);

cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");

scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);

{{< /highlight >}}

###  **以 3D 格式翻转坐标系**
(THREEDNET-123) -允许用户在 OBJ/3DS/STL 中翻转坐标系。示例代码:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });

scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });

{{< /highlight >}}

###  **如何三角剖分网格**
三角网格对于游戏行业很有用，因为三角形是GPU硬件支持的唯一受支持的基元 (非三角数据在驱动程序级别进行三角划分，这在实时渲染中效率低下)。示例代码:

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

