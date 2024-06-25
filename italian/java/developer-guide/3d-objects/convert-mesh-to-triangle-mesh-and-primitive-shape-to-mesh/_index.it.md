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



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.java" >}}
##  **Convertire la forma primitiva in mesh**
Aspose.3D for Java API supporta la conversione di qualsiasi forma primitiva in mesh. Le forme primitive includono oggetti più semplici e usati come scatola, sfera, piano, cilindro e toro.

{{% alert color="primary" %}}

Qualsiasi classe che implementa un'interfaccia IMeshConvertible può essere convertita in mesh durante l'esportazione in qualsiasi formato di file 3D.

{{% /alert %}}
###  **Convertire la sfera primitiva in mesh**
Una sfera è un oggetto geometrico perfettamente rotondo nello spazio tridimensionale che appare ovunque, dalle palle sportive ai pianeti nello spazio. Usiamo la Sfera primitiva per creare una mesh.
L'esempio di codice seguente converte una sfera in mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertSpherePrimitivetoMesh.java" >}}
###  **Convertire la casella in mesh**
Una scatola descrive una varietà di contenitori e recipienti per uso permanente come deposito o per uso temporaneo, spesso per il trasporto di contenuti. Usiamo la scatola primitiva per creare una mesh. L'esempio di codice seguente converte un Box in mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxPrimitivetoMesh.java" >}}
###  **Convertire un aereo in rete**
Un piano si estende all'infinito senza spessore. Un esempio di un aereo è un piano di coordinate. Consente di utilizzare il piano primitivo per creare una mesh. L'esempio di codice seguente converte un piano in mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertPlanePrimitivetoMesh.java" >}}
###  **Convertire un cilindro in rete**
Un cilindro è una delle forme geometriche curvilinee più elementari, la superficie formata dai punti a distanza fissa da una data linea retta, l'asse del cilindro. Può essere utilizzato in molti luoghi, ad esempio come pilastro davanti a una casa o come albero motore per auto. Consente di utilizzare il cilindro primitivo per creare una mesh. L'esempio di codice seguente converte un cilindro in mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertCylinderPrimitivetoMesh.java" >}}
###  **Convertire un Torus in Mesh**
Un toro è una superficie di rivoluzione generata ruotando un cerchio nello spazio tridimensionale attorno a un asse complanare con il cerchio. Se l'asse di rivoluzione non tocca il cerchio, la superficie ha una forma ad anello ed è chiamata toro di rivoluzione. Usiamo il Torus primitivo per creare una mesh. L'esempio di codice seguente converte un Torus in mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertTorusPrimitivetoMesh.java" >}}
