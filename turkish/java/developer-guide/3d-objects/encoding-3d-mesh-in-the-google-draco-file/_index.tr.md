---
title: 3D mesh kodlaması Google Draco dosyasında
type: docs
weight: 30
url: /tr/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API 3D modelini ithal etme desteğine sahiptir, mesh alır ve daha sonra Google Draco dosyasında örgü kodlar.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 3D modelini ithal etme desteğine sahiptir, mesh alır ve daha sonra Google Draco dosyasında örgü kodlar. Geliştiriciler ayrıca bir örgü kodlamadan önce pozisyonu, doku koordinatlarını, rengi ve normal bitlerini ve sıkıştırma seviyesini de belirtebilirler.

{{% /alert %}} 
##  **3D mesh alın ve Google Draco dosyasında kodlayın**
The encode method exposed by the `DracoFormat` class can be used to encode a 3D mesh in the Google Draco file. It takes a `Mesh` and `DracoSaveOptions` objects as parameters. With the Draco save options, developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.
###  **Programming ample ample**
Bu kod örneği, kürenin ağını alır ve daha sonra bir sıkıştırma seviyesi belirttikten sonra Google Draco dosyasında kodlanır.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-Encode3DMeshinGoogleDraco.java" >}}
