---
title: Offentlig API Ändrar i Aspose.3D 1.2.0
type: docs
weight: 50
url: /sv/net/public-api-changes-in-aspose-3d-1-2-0/
---
**Innehåll**

- [Setup the Target and Camera in 3D File](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
- [Flip Coordinate System in 3D Formats](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
- [How to Triangulate a Mesh](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)

{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar i Aspose. 3D API från version 1.1. 0 till 1.2.0, som kan vara av intresse för modul/applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose. 3D.

{{% /alert %}} 
###  **Ställ in mål och kamera i 3D fil**
I vissa filformat, stöder ljus/kamera mål, vilket tillåter ljuset/kameran alltid vända mot en specificerad nod, detta är användbart i animation. Exempelkod:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());

cameraNode.Transform.Translation = new Vector3(100, 20, 0);

cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");

scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);

{{< /highlight >}}

###  **Vänd koordinatsystem i 3D Format**
(THREEDNET-123) - Tillåt användaren att vända koordinatsystemet i OBJ/3DS/STL. Exempelkod:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });

scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });

{{< /highlight >}}

###  **Hur man kan tränga ett tåg**
Triangulera mesh är användbart för spelindustrin eftersom den trekantiga är den enda primitiva som stöds som GPU hårdvara stöder (icke-triangulära data är triangulerad i förarnivå, som är ineffektiv i realtids rendering. Exempelkod:

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

