---
title: Aspose.3D for .NET 1.7.0 Note di rilascio
type: docs
weight: 60
url: /it/net/aspose-3d-for-net-1-7-0-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 1.7.0](https://www.nuget.org/packages/Aspose.3D/1.7.0)

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-141|Aggiungere il supporto per convertire STL in un formato immagine.|Nuova funzione|
|THREEDNET-169|Rendi la scena a una consistenza.|Nuova funzione|
|THREEDNET-170|Aggiungi il supporto dell'ombra.|Nuova funzione|
|THREEDNET-174|Generare dati normali dal gruppo di livellamento.|Nuova funzione|
|THREEDNET-179|Si è verificato un errore dell'indice fuori intervallo durante il caricamento di un file U3D.|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge Aspose.ThreeD. Entità. Classe Frustum**
Viene aggiunta una nuova classe Frustum. Camera e Luce erano le sottoclassi della classe Entity. Nella versione 1.7.0, queste classi vengono ereditate da Frustum e Frustum viene ereditato da Entity, poiché le proprietà Position, Up, LookAt, Direction, Target, NearPlane e FarPlane vengono estratte in Frustum.
#### **Aggiunge Aspose.ThreeD. Classe ImageRenderOptions**
Consente agli sviluppatori di impostare varie opzioni di rendering come il colore dello sfondo, la directory delle risorse e abilitare/disabilitare l'ombra degli oggetti prima di convertire un file 3D in immagine.
#### **Aggiunge più metodi di rendering nella classe Aspose.ThreeD.Scene**
Rende una scena 3D nella prospettiva della fotocamera data nel formato e nelle dimensioni del file immagine specificati.
#### **Aggiunge il metodo MoveForward nella classe Aspose.ThreeD.Entities.Camera**
Si sposta in avanti la telecamera verso il suo orientamento. L'orientamento di una fotocamera è specificato da uno qualsiasi dei Target/Direction/LookAt

- **Obiettivo:**Un nodo target nello spazio, la fotocamera guarderà sempre questo obiettivo qualunque sia l'obiettivo/la telecamera che ha cambiato la sua posizione nello spazio.
- **LookAt:**Una posizione fissa nello spazio, la fotocamera guarderà sempre questa posizione.
- **Direzione:**Un vettore di direzione, l'orientamento di una telecamera è specificato direttamente da questo vettore qualunque sia la sua posizione.
#### **Aggiunge membri CastShadows e ReceiveShadows in Aspose.ThreeD.Entities.Geometry class**
Alcuni formati di file possono memorizzare le impostazioni relative alle ombre in geometria come FBX e vengono utilizzate anche nel rendering.
#### **Aggiunge il metodo GenerateNormal in Aspose.ThreeD. Entità. Classe PolygonModifier**
Consente agli sviluppatori di generare dati normali dall'istanza Mesh, se l'elemento VertexElementSmoothingGroup è stato definito sulla mesh, i dati normali generati verranno smussati da VertexElementSmoothingGroup.
#### **Aggiunge il metodo Concate nella classe Aspose.ThreeD.Utilities.Quaternion**
Consente agli sviluppatori di concatenare due trasformazioni di rotazione in una rappresentata in Quaternion.
