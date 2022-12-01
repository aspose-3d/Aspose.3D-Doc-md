---
title: Público API Cambios en Aspose.3D 1.2.0
type: docs
weight: 50
url: /es/net/public-api-changes-in-aspose-3d-1-2-0/
---
**Resumen de contenidos**

- [Configure el objetivo y la cámara en el archivo 3D](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
- [Flip Coordinate System en 3D Formats](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
- [Cómo triangular una malla](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)

{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.3D API de la versión 1.1.0 a 1.2.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.3D.

{{% /alert %}} 
### **Configure el objetivo y la cámara en el archivo 3D**
En algunos formatos de archivo, la luz/cámara es compatible con el objetivo, lo que permite que la luz/cámara siempre frente a un nodo específico, esto es útil en animación. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());

cameraNode.Transform.Translation = new Vector3(100, 20, 0);

cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");

scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);

{{< /highlight >}}

### **Flip Coordinate System en 3D Formats**
(THREEDNET-123) -Permitir al usuario voltear el sistema de coordenadas en OBJ/3DS/STL. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });

scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });

{{< /highlight >}}

### **Cómo triangular una malla**
La malla triangulada es útil para la industria de los juegos porque la triangular es la única primitiva admitida que admite el hardware de la GPU (los datos no triangulares se triangulan en el nivel del controlador, lo cual es ineficiente en la representación en tiempo real). Código de ejemplo:

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

