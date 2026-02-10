---
title: İlkel 3D şekilleri ile sahne oluşturun
type: docs
weight: 20
url: /tr/java/create-scene-with-primitive-3d-shapes/
description: Aspose.3D for Java API primitive 3D şekillerinin desteğine sahiptir. Tüm parametreli ilkeller, desteklenen herhangi bir çıkış dosyası formatında tasarruf ederken otomatik olarak ağa dönüştürülecektir.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API primitive 3D şekillerinin desteğine sahiptir. Tüm parametreli ilkeller, desteklenen herhangi bir çıkış dosyası formatında tasarruf ederken otomatik olarak ağa dönüştürülecektir.

{{% /alert %}} 
##  **İlkel 3D şekillerinden sahne oluşturun**
Modelleme, saf yaratma ve Aspose sürecidir. 3D API, primitive 3D şekilleriyle bir sahne oluşturmayı destekler.
###  **Programming ample ample**
Bu kod örneği, İlkel 3D şekilleri ile bir sahne oluşturur ve FBX dosyasında tasarruf sağlar.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.getRootNode().createChildNode("box", new Box());
// Create a Cylinder model
scene.getRootNode().createChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
MyDir = MyDir + RunExamples.getOutputFilePath("test.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
