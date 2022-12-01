---
title: Aspose.3D for .NET 1.5.0 Note di rilascio
type: docs
weight: 80
url: /it/net/aspose-3d-for-net-1-5-0-release-notes/
---
## **Altri miglioramenti e modifiche**

|**Chiave** |**Riassunto** |**Categoria** |
|:- |:- |:- |
|THREEDNET-146 |Convertire geometrie in struttura per vertice.|Nuova funzione|
|THREEDNET-148 |Consenti all'utente di dividere la mesh per materiali.|Nuova funzione|
|THREEDNET-150 |Creare mesh per l'aereo.|Nuova funzione|
|THREEDNET-151 |Crea mesh per Box.|Nuova funzione|
|THREEDNET-152 |Crea mesh per Sfera.|Nuova funzione|
|THREEDNET-153 |Crea la maglia per il cilindro.|Nuova funzione|
|THREEDNET-155 |Crea mesh per torus.|Nuova funzione|
|THREEDNET-145 |Consentire il sistema di coordinate flip nella classe di configurazione load/save di U3D.|Miglioramento|
|THREEDNET-154 |Problema ortografico: Distreet3DS dovrebbe essere Discreet3DS.|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Rimozione del formato Distreet3DS.**
Il formato Distreet3DS è contrassegnato come obsoleto a causa dell'incantesimo errato.
#### **Aggiunge il formato Discreet3DS.**
Il formato Discreet3DS è stato introdotto.
#### **Aggiunge l'interfaccia Aspose.ThreeD. Entità. IMeshConvertible.**
Qualsiasi classe che implementa questa interfaccia può essere convertita in mesh durante l'esportazione in qualsiasi formato di file 3D.
#### **Aggiunge la classe Aspose.ThreeD. Entità. Primitive.**
È derivato dalla classe Entity e anche dalla classe base per tutte le classi primitive.
#### **Aggiunge la classe Aspose.ThreeD. Entità. Scatola/Cilindro/Aereo/Sfera/Torus**
Questi possono essere usati per definire la scena con semplici primitive. Gli sviluppatori possono anche convertirli automaticamente in mesh.
#### **Aggiunge la classe Aspose.ThreeD. Entità. TriMesh/TriMesh<T>**
TriMesh/TriMesh<T>Contiene la definizione di mesh basate su triangolo con layout di memoria personalizzato, che è utile quando lo sviluppatore richiede di convertire la scena nei propri formati di file proprietari o nel rendering.
#### **Aggiunge la struttura Aspose.ThreeD.Utilities.FVector2/FVector3/FVector4**
Queste classi presentano componenti vettoriali nel galleggiante. Solo poche GPU moderne supporta il vettore a doppia precisione, i tipi di flottante a precisione singola sono più graditi nel mondo del rendering in tempo reale. Queste sostituzioni coesisteranno con l'originale Vector2/Vector3/Vector4 poiché svolgono ruoli diversi nello Aspose.3D. La doppia precisione viene utilizzata principalmente per memorizzare i dati del modello perché ha meno errori accumulati. La precisione singola viene utilizzata principalmente nel rendering o nella conversione dei formati di file proprietari dell'utente perché ha una migliore accettazione e prestazioni. Abbiamo introdotto questo set di vettori nello Aspose.3D 1.5 perché abbiamo aggiunto il supporto per il layout personalizzato dei vertici, in cui verranno utilizzati frequentemente i vettori float.
#### **Aggiunge la classe di attributi Aspose.ThreeD.Utilities.SemanticAttribute**
Lo sviluppatore può definire la struttura personalizzata per vertex e utilizzare questo attributo per contrassegnare la semantica dei campi.
#### **Aggiunge la classe Aspose.ThreeD.Utilities.VertexDeclaration**
Descrive il layout della memoria del vertice.
#### **Aggiunge enum Aspose.ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic**
Questi tipi enum annotano rispettivamente il tipo di dati e la semantica del campo del vertice.
#### **Aggiunge la classe Aspose.ThreeD.Utilities.VertexField**
Descrive ogni campo nel layout di memoria personalizzato di Vertex.
#### **Aggiunge la classe Aspose.ThreeD.Utilities.Vertex**
Può essere utilizzato per accedere al vertice grezzo in TriMesh/TriMesh<T>
#### **Aggiunge enum Aspose.ThreeD.Entities.SplitMeshPolicy**
Specifica la politica dei dati utilizzata nell'algoritmo di frazionamento mesh, supportiamo due criteri, condividiamo i dati tra sottogmesh o ogni sottogmesh ha i propri dati (solo dati utilizzati).
#### **Aggiunge 3 metodi SplitMesh alla classe Aspose.ThreeD.Entities.PolygonModifier**
1. Dividere le maglie su un nodo specificato in sottmesh per definizione di materiale.
1. Dividi tutte le maglie nella scena data in sotto-mesh per definizione materiale.
1. Dividere la mesh data in sottogmesh per definizione materiale.
#### **Aggiunge la proprietà FlipCoordinateSystem nella classe Aspose.ThreeD. Formati. Universal3DConfig**
Consente agli utenti di capovolgere il sistema di coordinate dello U3D durante l'importazione o l'esportazione.

