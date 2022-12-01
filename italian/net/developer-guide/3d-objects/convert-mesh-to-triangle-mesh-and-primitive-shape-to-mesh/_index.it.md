---
title: Convertire mesh in mesh triangolare e forma primitiva in mesh
type: docs
weight: 30
url: /it/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API consente agli sviluppatori di convertire qualsiasi oggetto mesh in mesh triangolare con layout di memoria personalizzato del vertice. Il layout di memoria personalizzato di Vertex viene definito utilizzando Struct o dinamicamente dalla classe VertexDeclaration negli esempi di codice.
---
## **Convertire una mesh in mesh triangolare con layout di memoria personalizzato del vertice**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API consente agli sviluppatori di convertire qualsiasi oggetto mesh in mesh triangolare con layout di memoria personalizzato del vertice. Il layout di memoria personalizzato di Vertex è definito utilizzando Struct o dinamicamente dalla classe [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) negli esempi di codice.

{{% alert color="primary" %}}

Questo argomento di aiuto crea mesh dalla casella e dalla sfera per mantenere il codice completo e breve. Gli sviluppatori possono costruire una mesh manualmente come narrato in questo argomento di aiuto:[Creare una maglia cubica 3D](/3d/it/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Questi esempi mostrano come:

- [Convertire una Sfera in Triangle Mesh con il layout di memoria personalizzato del vertice (definito nello Struct)](/3d/it/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convertire una casella in mesh triangolare con il layout di memoria personalizzato del vertice (definito dalla classe VertexDeclaration)](/3d/it/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
### **Convertire Mesh**
Gli sviluppatori possono convertire la mesh in una mesh triangolare perché qualsiasi struttura complessa (di superficie) può essere rappresentata come un gruppo di triangoli. Il triangolo è la geometria più atomica. Quindi è usato come base per quasi tutto.
### **Vertici di accesso di una mesh triangolare**
Gli sviluppatori possono accedere a indici, vertici effettivi, vertici prima della fusione e byte totali dei vertici in memoria.

Il seguente esempio converte una mesh Sfera in triangolo con il layout di memoria personalizzato.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.cs" >}}




Il seguente esempio converte una mesh box in triangolare con layout di memoria personalizzato.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.cs" >}}
## **Convertire il primitivo in una maglia**
Utilizzando Aspose.3D for .NET, gli sviluppatori possono convertire qualsiasi oggetto primitivo in una mesh. I primitivi includono molti degli oggetti più elementari e più utilizzati come scatola, sfera, piano, cilindro e toro.

{{% alert color="primary" %}}

Qualsiasi classe che implementa un'interfaccia `IMeshConvertible` può essere convertita in mesh durante l'esportazione in qualsiasi formato di file 3D.

{{% /alert %}}
### **Convertire una sfera in mesh**
Una sfera è un oggetto geometrico perfettamente rotondo nello spazio tridimensionale che appare ovunque, dalle palle sportive ai pianeti nello spazio. Usiamo la Sfera primitiva per creare una mesh.
L'esempio di codice seguente converte una sfera in mesh.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.cs" >}}
### **Convertire una scatola in mesh**
Una scatola descrive una varietà di contenitori e recipienti per uso permanente come deposito o per uso temporaneo, spesso per il trasporto di contenuti. Usiamo la scatola primitiva per creare una mesh. L'esempio di codice seguente converte un Box in mesh.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.cs" >}}
### **Convertire un aereo in rete**
Un piano si estende all'infinito senza spessore. Un esempio di un aereo è un piano di coordinate. Consente di utilizzare la primitiva `Plane` per creare una mesh. L'esempio di codice seguente converte da `Plane` a `Mesh`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.cs" >}}
### **Convertire un cilindro in rete**
Un cilindro è una delle forme geometriche curvilinee più elementari, la superficie formata dai punti a distanza fissa da una data linea retta, l'asse del cilindro. Può essere utilizzato in molti luoghi, ad esempio come pilastro davanti a una casa o come albero motore per auto. Consente di utilizzare il cilindro primitivo per creare una mesh. L'esempio di codice seguente converte un cilindro in mesh.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.cs" >}}
### **Convertire un Torus in Mesh**
Un toro è una superficie di rivoluzione generata ruotando un cerchio nello spazio tridimensionale attorno a un asse complanare con il cerchio. Se l'asse di rivoluzione non tocca il cerchio, la superficie ha una forma ad anello ed è chiamata toro di rivoluzione. Usiamo il Torus primitivo per creare una mesh. L'esempio di codice seguente converte un Torus in mesh.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.cs" >}}
