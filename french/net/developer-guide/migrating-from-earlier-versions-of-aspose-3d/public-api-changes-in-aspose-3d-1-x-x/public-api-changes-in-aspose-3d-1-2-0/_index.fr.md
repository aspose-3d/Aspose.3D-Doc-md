---
title: Public API Changements dans Aspose.3D 1.2.0
type: docs
weight: 50
url: /fr/net/public-api-changes-in-aspose-3d-1-2-0/
---
**Résumé du contenu**

- [Configurer la cible et la caméra dans le fichier 3D](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
- [Retourner le système de coordonnées dans les formats 3D](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
- [Comment trianguler un maillage](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées à Aspose.3D API de la version 1.1.0 à 1.2.0, qui peuvent intéresser les développeurs de modules/applications. Il inclut non seulement des méthodes publiques nouvelles et mises à jour, mais aussi une description de tout changement de comportement dans les coulisses de Aspose.3D.

{{% /alert %}} 
###  **Configurer la cible et la caméra dans le fichier 3D**
Dans certains formats de fichiers, la lumière/caméra prend en charge la cible, ce qui permet à la lumière/caméra toujours face à un nœud spécifié, cela est utile dans l'animation. Exemple de code:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());

cameraNode.Transform.Translation = new Vector3(100, 20, 0);

cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");

scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);

{{< /highlight >}}

###  **Retourner le système de coordonnées dans les formats 3D**
(THREEDNET-123) -Permet à l'utilisateur de retourner le système de coordonnées dans OBJ/3DS/STL. Exemple de code:

**C#**

{{< highlight "csharp" >}}

 Scene scene = new Scene();

scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });

scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });

{{< /highlight >}}

###  **Comment trianguler un maillage**
Le maillage triangulé est utile pour l'industrie du jeu car le triangulaire est la seule primitive prise en charge par le matériel GPU (les données non triangulaires sont triangulées au niveau du pilote, ce qui est inefficace en temps réel). Exemple de code:

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

