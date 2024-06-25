---
title: Personalizza la conversione dei materiali da PBR a PBR prima di salvare 3D scene in GLTF 2.0 Formato
type: docs
weight: 50
url: /it/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scene di Aspose.3D for Java API rappresenta una scena di 3D e gli sviluppatori possono creare una scena di 3D aggiungendo varie entità.
---
{{% alert color="primary" %}} 

La classe `Scene` di Aspose.3D for Java API rappresenta una scena 3D e gli sviluppatori possono creare una scena 3D aggiungendo varie entità. GLTF 2.0 supporta solo materiali PBR (Rendering basato sulla fisica), Aspose.3D API converte internamente materiali non PBR in materiali PBR prima di esportare in GLTF 2.0 (i materiali nella scena rimarranno invariati durante l'esportazione) e gli sviluppatori possono fornire la funzione di conversione personalizzata per sovrascrivere il comportamento predefinito.

{{% /alert %}} 
##  **Conversione del materiale da non PBR a PBR**
Questo esempio di codice mostra come convertire il materiale in materiale PBR e quindi salvare la scena 3D nel formato GLTF:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
