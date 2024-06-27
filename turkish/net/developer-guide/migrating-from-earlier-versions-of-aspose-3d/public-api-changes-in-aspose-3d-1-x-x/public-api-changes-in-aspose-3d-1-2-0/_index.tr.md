---
title: Kamu API Aspose içinde değişir. 3D 1.2.0
type: docs
weight: 50
url: /tr/net/public-api-changes-in-aspose-3d-1-2-0/
---
**Contents Summary**

- [Hedef ve kamerayı 3D dosyasında kur](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
- [Koordinat sistemini 3D formatlarında çevir](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
- [Ow ow to a riangulate a Mesh](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.1.0 to 1.2.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Hedef ve kamerayı 3D dosyasında kur**
In bazı dosya biçimleri, ışık/kamera, ışık/kameranın her zaman belirtilen bir düğüme bakmasını sağlayan hedefi destekler, bu animasyonda yararlıdır. Example kodu:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());

cameraNode.Transform.Translation = new Vector3(100, 20, 0);

cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");

scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);

{{< /highlight >}}

###  **Koordinat sistemini 3D formatlarında çevir**
(THREEDNET-123) - Allow user to flip coordinate system in OBJ/3DS/STL. Example code:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });

scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });

{{< /highlight >}}

###  **Ow ow to a riangulate a Mesh**
Triangulate mesh, oyun endüstrisi için yararlıdır, çünkü üçgen, Ghardware hardware donanım desteğinin desteklediği tek desteklenen ilkeldir (üçgen olmayan veriler, gerçek zamanlı olarak verimsiz olan sürücü seviyesinde üçgendir). Example kodu:

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

