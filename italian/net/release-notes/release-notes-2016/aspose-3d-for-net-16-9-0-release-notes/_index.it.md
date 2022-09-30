---
title: Aspose.3D for .NET 16.9.0 Note di rilascio
type: docs
weight: 30
url: /it/net/aspose-3d-for-net-16-9-0-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 16.9.0](https://www.nuget.org/packages/Aspose.3D/16.9.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-209|Generare tangente dai dati mesh.|Nuova funzionalità|
|THREEDNET-208|Mappatura normale nel rendering.|Nuova funzionalità|
|THREEDNET-182|Esporta la scena 3D allo PDF 1.6.|Nuova funzionalità|
|THREEDNET-205|Importa le scene 3D da un file PDF.|Nuova funzionalità|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
### **Salva una scena 3D nel formato PDF**
Utilizzando la versione recente (16.9.0) o superiore, gli sviluppatori possono salvare tutti i file 3D supportati nel formato PDF.
#### **Aggiunge Aspose.ThreeD.Formats.PdfSaveOptions Class**
Abbiamo aggiunto la classe PdfSaveOptions. Aiuta ad applicare l'impostazione prima di salvare nel formato di output PDF.
#### **Aggiunge Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums**
Gli sviluppatori possono impostare una modalità di rendering e uno schema di illuminazione prima di salvare una scena 3D nel formato PDF.
### **Importazione 3D Scena dalla fonte PDF**
Utilizzando la versione recente (16.9.0) o superiore, gli sviluppatori possono recuperare 3D scene da un file di input PDF.
#### **Aggiunge Aspose.ThreeD. Formati. Classe PdfLoadOptions**
Abbiamo aggiunto la classe PdfLoadOptions. Aiuta a caricare il contenuto dal file di input PDF. Gli sviluppatori possono applicare la password per i PDF protetti.
#### **Aggiunge il formato PDF nella classe Aspose.ThreeD.FileFormat**
Abbiamo aggiunto una voce del formato PDF per scopi di caricamento e salvataggio.
#### **Aggiunge Aspose.ThreeD. Formati. Classe PdfFormat**
Abbiamo aggiunto la classe PdfFormat. Aiuta a manipolare i PDF.
### **Aggiunge il metodo triangolato nella classe Aspose.ThreeD.Entities.PolygonModifier**
Abbiamo aggiunto un altro sovraccarico del metodo Triangulate nella classe PolygonModifier che prende un oggetto classe Scene come parametro.
#### **Aggiunge due metodi BuildTangentBinormal nella classe Aspose.ThreeD.Entities.PolygonModifier**
Abbiamo aggiunto due metodi BuildTangentBinormal nella classe PolygonModifier. Un metodo prende l'oggetto classe Scene come parametro e un altro prende l'oggetto classe Mesh come parametro.