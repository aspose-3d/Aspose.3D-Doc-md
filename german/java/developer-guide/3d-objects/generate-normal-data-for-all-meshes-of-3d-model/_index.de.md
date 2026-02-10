---
title: Generieren Sie normale Daten für alle Maschen des 3D-Modells
type: docs
weight: 40
url: /de/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API unterstützt die Generierung normaler Daten für alle Netze des 3D Modells (ohne die normalen Daten).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API unterstützt die Generierung normaler Daten für alle Netze des 3D Modells (ohne die normalen Daten).

{{% /alert %}} 
##  **Generieren Sie normale Daten für alle Maschen des 3DS-Modells**
Die generate Normal-Methode, die von der `PolygonModifier`-Klasse verfügbar gemacht wird, kann verwendet werden, um normale Daten für alle Netze in einer 3DS-Datei zu generieren. Wenn das VertexElementSmoothingGroup-Element im Netz definiert wurde, werden die generierten normalen Daten von der VertexElementSmoothingGroup geglättet.
###  **Programmier probe**
Dieses Code beispiel lädt eine 3DS-Datei, besucht alle Knoten und erstellt normale Daten für alle Netze.

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
