---
title: Aspose.3D for .NET 20.8 Note di rilascio
type: docs
weight: 9
url: /it/net/aspose-3d-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 20.8.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-698|Aggiunto il supporto per l'importazione di file 3D con zip|
|THREEDNET-697|I materiali PBR fissi con speculare non erano supportati nel GLTF|
|THREEDNET-705|Aggiunto il supporto per l'importazione di FBX 6.0|
|THREEDNET-706|Aggiunto FBX 6.1 supporto all'importazione|
|THREEDNET-707|Aggiunto FBX 7.0/7.1 supporto all'importazione|
|THREEDNET-708|Gli attributi non supportati in FBX non sono supportati.|
|THREEDNET-703|Aggiunto FBX 7.7 supporto all'importazione|
|THREEDNET-704|Il file OBJ con indice di elementi negativi non è supportato.|
|THREEDNET-700|Il fisso Aspose.3D si blocca all'analisi del file PDF incompleto|
|THREEDNET-699|Fisso lo scarico di tutta la memoria Aspose.3D quando si parava un file PDF|
|THREEDNET-714|Aspose.3D richiede molta memoria e CPU per caricare un file GLB|
|THREEDNET-715|Risolto il rendering della mesh semplice (con solo dati normali) con il materiale PBR non era corretto|
|THREEDNET-711|Aspose.3D si blocca all'importazione di un file FBX.|
|THREEDNET-710|Il rendering non funziona con alcuni hardwares AMD.|

## API modifiche ##
Questa versione è principalmente una versione di bug fix, quindi nessun esempio di codice.

### Classi aggiunte ###
  * Classe Aspose.ThreeD.Shading.PbrSpecularMaterial-Questo viene utilizzato per rappresentare il materiale pbr speculare, al momento supportato solo in GLTF 2.0.
  * Classe aggiunta Aspose.ThreeD. Entità. VertexElementHole-per il foro di supporto nella maglia dello FBX
### Membri aggiunti ###
  * Membro aggiunto al tipo enum Aspose.ThreeD.Entities.VertexElementType
```
public static Aspose.ThreeD.Entities.VertexElementType Hole;
```
  * Membri aggiunti alla classe Aspose.ThreeD.FileFormat
```
public static readonly Aspose.ThreeD.FileFormat Zip;
```
Con questo nuovo supporto per il formato di file, Aspose.3D può importare un file zip che contiene un file 3D. Di solito non è necessario utilizzare manualmente questo.

