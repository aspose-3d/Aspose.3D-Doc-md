---
title: Public API hangمعلقة في Aspose.3D 1.2.0
type: docs
weight: 50
url: /ar/net/public-api-changes-in-aspose-3d-1-2-0/
---
**Contents Sأوماري**

- [Tup etop ararget و amamera في 3D ile ile](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
- [Fالشفاه ordinordinفي 3D orormat](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
- [How إلى ririesh](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 1.1.0 إلى 1.2.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
### **Tup etop ararget و amamera في 3D ile ile**
In بعض صيغ الملفات ، الضوء/الكاميرا يدعم الهدف ، والذي يسمح للضوء/الكاميرا تواجه دائما عقدة محددة ، وهذا مفيد في الرسوم المتحركة. Eرمز xample:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());

cameraNode.Transform.Translation = new Vector3(100, 20, 0);

cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");

scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);

{{< /highlight >}}

### **Fالشفاه ordinordinفي 3D orormat**
(THREEDNET-123) - Allow المستخدم إلى الوجه تنسيق النظام في OBJ/3DS/STL. Eرمز xample:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });

scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });

{{< /highlight >}}

### **How إلى ririesh**
شبكة ريانغتوليت غير مفيدة لصناعة اللعبة لأن الثلاثي هو البدائية الوحيدة المدعومة التي تدعم الأجهزة GPU (يتم تقسيم البيانات غير الثلاثية في مستوى السائق ، وهو غير فعال في تقديم في الوقت الحقيقي). Eرمز xample:

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

