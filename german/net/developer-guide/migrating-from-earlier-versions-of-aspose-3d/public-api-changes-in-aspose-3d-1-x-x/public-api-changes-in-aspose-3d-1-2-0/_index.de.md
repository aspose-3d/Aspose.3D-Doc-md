---
title: Öffentliche API Änderungen in Aspose.3D 1.2.0
type: docs
weight: 50
url: /de/net/public-api-changes-in-aspose-3d-1-2-0/
---
**Inhalts übersicht**

- [Richten Sie das Ziel und die Kamera in der Datei 3D ein](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
- [Flip-Koordinaten system in den Formaten 3D](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
- [Wie man ein Netz trianguliert](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)

{{% alert color="primary" %}} 

In diesem Dokument werden Änderungen an Aspose.3D API von Version 1.1.0 zu 1.2.0 beschrieben, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung etwaiger Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
### **Richten Sie das Ziel und die Kamera in der Datei 3D ein**
In einigen Dateiformaten unterstützt Licht/Kamera das Ziel, wodurch das Licht/die Kamera immer einem bestimmten Knoten zugewandt ist. Dies ist in der Animation nützlich. Beispiel code:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());

cameraNode.Transform.Translation = new Vector3(100, 20, 0);

cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");

scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);

{{< /highlight >}}

### **Flip-Koordinaten system in den Formaten 3D**
(THREEDNET-123) -Erlauben Sie dem Benutzer, das Koordinaten system in OBJ/3DS/STL umzudrehen. Beispiel code:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });

scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });

{{< /highlight >}}

### **Wie man ein Netz trianguliert**
Triangulate Mesh ist für die Spiele industrie nützlich, da das Dreiecksnetz das einzige unterstützte Primitiv ist, das die GPU-Hardware unterstützt (nicht dreieckige Daten werden auf Treiber ebene trianguliert, was beim Echtzeit-Rendering ineffizient ist). Beispiel code:

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

