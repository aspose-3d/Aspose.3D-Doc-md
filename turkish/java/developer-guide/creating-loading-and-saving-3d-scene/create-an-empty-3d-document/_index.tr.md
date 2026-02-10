---
title: Boş bir 3D belgesi oluşturun
type: docs
weight: 20
url: /tr/java/create-an-empty-3d-document/
description: Aspose.3D for Java API sıfırdan 3D sahne oluşturma desteği var ve daha sonra desteklenen 3D formatında kaydedin.
---
##  **Boş bir 3D sahne oluşturun ve desteklenen 3D formatında kaydedin**
Aspose.3D for Java API sıfırdan 3D sahne oluşturma desteği var ve daha sonra desteklenen 3D formatında kaydedin.
###  **Boş bir 3D sahne oluşturma**
Aspose ile 3D sahne oluşturmak için lütfen bu adımları izleyin. 3D for Java API:

1. Create bir örnek**Sahne** class that represents 3D scene.
1. Çağırarak 3D belgesi oluşturun**Kaydet**Yöntemi**Sahne**Sınıf örneği.
####  **Boş bir 3D sahne oluşturma: programlama örnekleri**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}




