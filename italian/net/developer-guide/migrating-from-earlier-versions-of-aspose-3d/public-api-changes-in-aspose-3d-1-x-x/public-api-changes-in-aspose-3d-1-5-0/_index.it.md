---
title: Pubblico API Modifiche nello Aspose.3D 1.5.0
type: docs
weight: 20
url: /it/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Contenuto sommario**

- [Convertire il primitivo in una mesh e creare una scena da modelli primitivi 3D](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Convertire una mesh in mesh triangolare con layout di memoria personalizzato del vertice](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Rete spaccata](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Rimozione del formato Distreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Aggiunge il formato Discreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Aggiunge la proprietà FlipCoordinateSystem nella classe Aspose.ThreeD. Formati. Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.3D API dalla versione da 1.4.0 a 1.5.0, che potrebbero essere di interesse per gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte nello Aspose.3D.

{{% /alert %}} 
### **Convertire il primitivo in una mesh e creare una scena da modelli primitivi 3D**
**Vengono aggiunte varie classi, metodi e proprietà**

- **Aggiunge l'interfaccia Aspose.ThreeD. Entità. IMeshConvertible.** 
-Qualsiasi classe che implementa questa interfaccia può essere convertita in mesh durante l'esportazione in qualsiasi formato di file 3D.
- **Aggiunge la classe Aspose.ThreeD. Entità. Primitive.** 
-Deriva dalla classe Entity e anche dalla classe base per tutte le classi primitive.
- **Aggiunge la classe Aspose.ThreeD. Entità. Scatola/Cilindro/Aereo/Sfera/Torus.** 
-Questi possono essere usati per definire la scena con semplici primitive. Gli sviluppatori possono anche convertirli automaticamente in mesh.

I primitivi includono molti degli oggetti più elementari e più utilizzati come scatola, sfera, piano, cilindro e toro. Gli sviluppatori possono anche convertirli in mesh ai fini della modifica. Questi argomenti di aiuto illustrano come farlo:[Convertire il primitivo in una maglia](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models)E[Convertire il primitivo in una maglia](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
### **Convertire una mesh in mesh triangolare con layout di memoria personalizzato del vertice**
**Vengono aggiunte varie classi, metodi e proprietà**

- **Aggiunge la classe Aspose.ThreeD. Entità. TriMesh/TriMesh<T>** 
-TriMesh/TriMesh<T>Contiene la definizione di mesh basate su triangolo con layout di memoria personalizzato, che è utile quando lo sviluppatore richiede di convertire la scena nei propri formati di file proprietari o nel rendering.
- **Aggiunge la struttura Aspose.ThreeD.Utilities.FVector2/FVector3/FVector4** 
-Queste classi presentano componenti vettoriali nel galleggiante. Solo poche GPU moderne supporta il vettore a doppia precisione, i tipi di flottante a precisione singola sono più graditi nel mondo del rendering in tempo reale. Queste sostituzioni coesisteranno con l'originale Vector2/Vector3/Vector4 poiché svolgono ruoli diversi nello Aspose.3D. La doppia precisione viene utilizzata principalmente per memorizzare i dati del modello perché ha meno errori accumulati. La precisione singola viene utilizzata principalmente nel rendering o nella conversione dei formati di file proprietari dell'utente perché ha una migliore accettazione e prestazioni. Abbiamo introdotto questo set di vettori nello Aspose.3D 1.5 perché abbiamo aggiunto il supporto per il layout personalizzato dei vertici, in cui verranno utilizzati frequentemente i vettori float.
- **Aggiunge la classe di attributi Aspose.ThreeD.Utilities.SemanticAttribute** 
-Lo sviluppatore può definire la struttura personalizzata per il vertice e utilizzare questo attributo per contrassegnare la semantica dei campi.
- **Aggiunge la classe Aspose.ThreeD.Utilities.VertexDeclaration** 
-Descrive il layout della memoria del vertice.
- **Aggiunge enum Aspose.ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic** 
-Questi tipi enum annotano rispettivamente il tipo di dati e la semantica del campo del vertice.
- **Aggiunge la classe Aspose.ThreeD.Utilities.VertexField** 
-Descrive ogni campo nel layout di memoria personalizzato di Vertex.
- **Aggiunge la classe Aspose.ThreeD.Utilities.Vertex** 
-Può essere utilizzato per accedere al vertice grezzo in TriMesh/TriMesh<T>

Gli sviluppatori possono convertire qualsiasi oggetto mesh nella mesh triangolare con il layout di memoria personalizzato del vertice. I pacchetti software grafici e i dispositivi hardware funzionano in modo più efficiente su triangoli. Questo argomento di aiuto illustra come farlo:[Convertire una mesh in mesh triangolare con layout di memoria personalizzato del vertice](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
### **Rete spaccata**
**Vengono aggiunte varie classi, metodi e proprietà**

- **Aggiunge enum Aspose.ThreeD.Entities.SplitMeshPolicy** 
-Specifica la politica dei dati utilizzata nell'algoritmo di frazionamento mesh, supportiamo due politiche, condividiamo i dati tra sottogmesh o ogni sottogmesh ha i propri dati (solo dati utilizzati).
- **Aggiunge 3 metodi SplitMesh alla classe Aspose.ThreeD.Entities.PolygonModifier** 
1. Dividere le maglie su un nodo specificato in sottogruppi per definizione di materiale.
1. Dividere tutte le mesh nella scena data in sotto-mesh per definizione di materiale.
1. Dividere la mesh data in sottogruppi per definizione materiale.
- **Aggiunge la proprietà FlipCoordinateSystem nella classe Aspose.ThreeD. Formati. Universal3DConfig** 
-Permette agli utenti di capovolgere il sistema di coordinate di U3D durante l'importazione o l'esportazione.

Gli sviluppatori possono richiedere di dividere automaticamente una mesh per materiale, in modo che ogni mesh utilizzi solo un materiale o una maglia divisa specificando il materiale. Questi argomenti di aiuto illustrano come farlo:[Dividi una maglia specificando il materiale](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial)E[Dividi tutte le maglie di una scena per materiale](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
### **Rimozione del formato Distreet3DS.**
Il formato Distreet3DS è contrassegnato come obsoleto a causa dell'incantesimo errato.
### **Aggiunge il formato Discreet3DS.**
Il formato Discreet3DS è stato introdotto.
### **Aggiunge la proprietà FlipCoordinateSystem nella classe Aspose.ThreeD. Formati. Universal3DConfig**
Consente agli utenti di capovolgere il sistema di coordinate dello U3D durante l'importazione o l'esportazione.
