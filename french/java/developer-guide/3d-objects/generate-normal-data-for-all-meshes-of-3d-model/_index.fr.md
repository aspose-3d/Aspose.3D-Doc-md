---
title: Générer des données normales pour tous les maillages du modèle 3D
type: docs
weight: 40
url: /fr/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API a le support de générer des données normales pour tous les maillages du modèle 3D (sans les données normales).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API a le support de générer des données normales pour tous les maillages du modèle 3D (sans les données normales).

{{% /alert %}} 
##  **Générer des données normales pour tous les maillages du modèle 3DS**
La méthode generateNormal exposée par la classe `PolygonModifier` peut être utilisée pour générer des données normales pour tous les maillages d'un fichier 3DS. Si l'élément VertexElementSmoothingGroup a été défini dans le maillage, les données normales générées seront lissées par le VertexElementSmoothingGroup.
###  **Échantillon de programmation**
Cet exemple de code charge un fichier 3DS, visite tous les nœuds et crée des données normales pour tous les maillages.

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
