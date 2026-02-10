---
title: Convertire mesh in mesh triangolare e forma primitiva in mesh
type: docs
weight: 20
url: /it/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API supporta la conversione da mesh a mesh triangolari con layout di memoria personalizzato del vertice. Il layout di memoria personalizzato di Vertex è definito dinamicamente dalla classe VertexDeclaration negli esempi di codice.
---
##  **Convertire Mesh in Triangle Mesh con un layout di memoria personalizzato di Vertex**
Aspose.3D for Java API supporta la conversione da mesh a mesh triangolari con layout di memoria personalizzato del vertice. Il layout di memoria personalizzato di Vertex è definito dinamicamente dalla classe `VertexDeclaration` negli esempi di codice.

{{% alert color="primary" %}}

Questo argomento di aiuto crea mesh dalla casella e dalla sfera per mantenere il codice completo e breve. Gli sviluppatori possono costruire una mesh manualmente come narrato in questo argomento di aiuto: [Crea 3D Cube Mesh](/3d/it/java/create-3d-mesh-and-scene/).

{{% /alert %}}

Gli sviluppatori possono convertire la mesh in una mesh triangolare perché qualsiasi struttura complessa (di superficie) può essere rappresentata come un gruppo di triangoli. Il triangolo è la geometria più atomica. Quindi è usato come base per quasi tutto. Questo esempio di codice converte una mesh box in triangolare con layout di memoria personalizzato.



{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("box");
// Get mesh of the Box
Mesh box = (new Box()).toMesh();
// Create a customized vertex layout
VertexDeclaration vd = new VertexDeclaration();
VertexField position = vd.addField(VertexFieldDataType.F_VECTOR4, VertexFieldSemantic.POSITION);
vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);
// Get a triangle mesh
TriMesh triMesh = TriMesh.fromMesh(box);
// ExEnd:ConvertBoxMeshtoTriangleMeshCustomMemoryLayout
// Point node to the Mesh geometry
cubeNode.setEntity(box);
// Add Node to a scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir() + RunExamples.getOutputFilePath("BoxToTriangleMeshCustomMemoryLayoutScene.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}
##  **Convertire la forma primitiva in mesh**
Aspose.3D for Java API supporta la conversione di qualsiasi forma primitiva in mesh. Le forme primitive includono oggetti più semplici e usati come scatola, sfera, piano, cilindro e toro.

{{% alert color="primary" %}}

Qualsiasi classe che implementa un'interfaccia IMeshConvertible può essere convertita in mesh durante l'esportazione in qualsiasi formato di file 3D.

{{% /alert %}}
###  **Convertire la sfera primitiva in mesh**
Una sfera è un oggetto geometrico perfettamente rotondo nello spazio tridimensionale che appare ovunque, dalle palle sportive ai pianeti nello spazio. Usiamo la Sfera primitiva per creare una mesh.
L'esempio di codice seguente converte una sfera in mesh.

{{< highlight "java" >}}
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
// Convert a Sphere to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertire la casella in mesh**
Una scatola descrive una varietà di contenitori e recipienti per uso permanente come deposito o per uso temporaneo, spesso per il trasporto di contenuti. Usiamo la scatola primitiva per creare una mesh. L'esempio di codice seguente converte un Box in mesh.

{{< highlight "java" >}}
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertire un aereo in rete**
Un piano si estende all'infinito senza spessore. Un esempio di un aereo è un piano di coordinate. Consente di utilizzare il piano primitivo per creare una mesh. L'esempio di codice seguente converte un piano in mesh.

{{< highlight "java" >}}
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
// Convert a Plane to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertire un cilindro in rete**
Un cilindro è una delle forme geometriche curvilinee più elementari, la superficie formata dai punti a distanza fissa da una data linea retta, l'asse del cilindro. Può essere utilizzato in molti luoghi, ad esempio come pilastro davanti a una casa o come albero motore per auto. Consente di utilizzare il cilindro primitivo per creare una mesh. L'esempio di codice seguente converte un cilindro in mesh.

{{< highlight "java" >}}
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
// Convert a Cylinder to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertire un Torus in Mesh**
Un toro è una superficie di rivoluzione generata ruotando un cerchio nello spazio tridimensionale attorno a un asse complanare con il cerchio. Se l'asse di rivoluzione non tocca il cerchio, la superficie ha una forma ad anello ed è chiamata toro di rivoluzione. Usiamo il Torus primitivo per creare una mesh. L'esempio di codice seguente converte un Torus in mesh.

{{< highlight "java" >}}
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
// Convert a Torus to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
