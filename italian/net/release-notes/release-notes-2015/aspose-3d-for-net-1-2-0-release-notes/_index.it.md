---
title: Aspose.3D for .NET 1.2.0 Note di rilascio
type: docs
weight: 10
url: /it/net/aspose-3d-for-net-1-2-0-release-notes/
---
Di seguito è riportato un elenco di miglioramenti e modifiche in questa versione dello Aspose.3D
# **1)Aspose.3D**
## **Nuove funzionalità**
(THREEDNET-115) - 3DS (Formato file di Autodesk 3D Studio DOS) importatore ed esportatore
## **Miglioramenti**
(THREEDNET-122) -più scene di supporto

(THREEDNET-123) -Consentire all'utente di capovolgere il sistema di coordinate in OBJ/3DS/STL
# **Pubblico API e modifiche incompatibili arretrate**
Di seguito è riportato un elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul forum di supporto Aspose.3D.

Aggiunta proprietà Target/Direction on Light/Camera

Collada/3ds e alcuni altri file utilizzano Target/Direction per impostare l'orientamento della luce/della fotocamera.

Aggiunti più metodi membro e overload dell'operatore per Vector2/Quaternion.

Viene utilizzato per il calcolo interno e anche utile per i clienti.

Aggiunto un nuovo PolygonModifier di classe.

Alcuni formati di file supportano solo le mesh triangolari mentre Aspose.3D supportano le mesh poligonali, quindi abbiamo aggiunto questa classe per consentire la conversione di mesh basate su poligoni in mesh a triangolo.
Aggiungeremo altre modifiche alla mesh in futuro.

Aggiunte diverse sottoclassi IOConfig come FBXConfig/OBJConfig/STLConfig/Discreet3DSConfig

Consenti all'utente di impostare le opzioni durante l'importazione/esportazione come ha fatto 3ds max/Maya/frullatore.
