---
title: Skapa normala data för alla maskor i 3D Modell
type: docs
weight: 40
url: /sv/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose. 3D for Java API har stöd för att generera normala data för alla maskor i 3D-modellen (utan normala data).
---
{{% alert color="primary" %}} 

Aspose. 3D for Java API har stöd för att generera normala data för alla maskor i 3D-modellen (utan normala data).

{{% /alert %}} 
##  **Skapa normala data för alla maskor i 3DS Modell**
Den genereradeNormal metoden som exponeras av klassen `PolygonModifier` kan användas för att skapa normala data för alla maskor i en 3DS-fil. Om VertexElementSmoothingGroup element definierades i masken, den genererade normala data kommer att jämnas ut av VertexElementSmoothingGroup.
###  **Programmeringsprova**
Det här kodexemplet laddar en 3DS-fil, besöker alla noder och skapar normala data för alla maskor.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load a 3ds file, 3ds file doesn't have normal data, but it has smoothing group
Scene s = new Scene(MyDir + "camera.3ds");
// Visit all nodes and create normal data for all meshes
s.getRootNode().accept(new NodeVisitor() {
    @Override
    public boolean call(Node node) {
        Mesh mesh = (Mesh)node.getEntity();
        if (mesh != null)
        {
            VertexElementNormal normals = PolygonModifier.generateNormal(mesh);
            mesh.addElement(normals);
        }
        return true;
    }
});
{{< /highlight >}}
