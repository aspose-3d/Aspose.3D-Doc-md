---
title: Boş bir 3D belgesi oluşturun
type: docs
weight: 20
url: /tr/nodejs-java/create-an-empty-3d-document/
description: Aspose.3D for Node.js via Java API, sıfırdan 3D sahne oluşturma desteğine sahiptir ve daha sonra desteklenen 3D formatında kaydedin.
---
##  **Boş bir 3D sahne oluşturun ve desteklenen 3D formatında kaydedin**
Aspose.3D for Node.js via Java API, sıfırdan 3D sahne oluşturma desteğine sahiptir ve daha sonra desteklenen 3D formatında kaydedin.
###  **Boş bir 3D sahne oluşturma**
Aspose.3D for Node.js via Java API ile 3D sahne oluşturmak için lütfen bu adımları izleyin:

1. Create bir örnek**Sahne** class that represents 3D scene.
1. Çağırarak 3D belgesi oluşturun**Kaydet**Yöntemi**Sahne**Sınıf örneği.
####  **Boş bir 3D sahne oluşturma: programlama örnekleri**
{{< highlight "java" >}}

var file="document.fbx";

// Create an object of the Scene class
var scene = new aspose.threed.Scene();

// Save 3D scene document
scene.save(file);

{{< /highlight >}}




