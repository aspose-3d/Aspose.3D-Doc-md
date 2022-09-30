---
title: Pubblico API Modifiche nel Aspose.3D 1.2.0
type: docs
weight: 50
url: /it/net/public-api-changes-in-aspose-3d-1-2-0/
---
**Contenuto sommario**

- [Configurazione della destinazione e della fotocamera nel file 3D](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
- [Flip Coordinate System in formato 3D](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
- [Come Triangolare una Mesh](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.3D API dalla versione da 1.1.0 a 1.2.0, che potrebbero essere di interesse per gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte nello Aspose.3D.

{{% /alert %}} 
### **Configurazione della destinazione e della fotocamera nel file 3D**
In alcuni formati di file, la luce/la fotocamera supporta il target, che consente alla luce/fotocamera di affrontare sempre un nodo specificato, questo è utile nell'animazione. Esempio di codice:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());

cameraNode.Transform.Translation = new Vector3(100, 20, 0);

cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");

scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);

{{< /highlight >}}

### **Flip Coordinate System in formato 3D**
(THREEDNET-123) -Consentire all'utente di capovolgere il sistema di coordinate in OBJ/3DS/STL. Esempio di codice:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });

scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });

{{< /highlight >}}

### **Come Triangolare una Mesh**
La mesh triangolata è utile per l'industria dei giochi perché il triangolare è l'unica primitiva supportata che l'hardware GPU supporta (i dati non triangolari sono triangolati a livello di driver, che è inefficiente nel rendering in tempo reale). Esempio di codice:

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

