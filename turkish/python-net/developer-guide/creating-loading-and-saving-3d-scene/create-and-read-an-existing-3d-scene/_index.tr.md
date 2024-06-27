---
title: Mevcut bir 3D sahne oluşturun ve okuyun
type: docs
weight: 10
url: /tr/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API yeni 3D sahnelerini sıfırdan oluşturmayı ve ardından desteklenen herhangi bir dosya biçiminde kaydetmeyi destekler. Geliştiriciler ayrıca değişiklik, ekleme veya işleme amaçları için mevcut bir 3D sahne yükleyebilir.
---
##  **Boş bir 3D sahne oluşturun ve desteklenen 3D dosya formatlarında kaydedin**
Aspose.3D API yeni 3D sahnelerini sıfırdan oluşturmayı ve ardından desteklenen herhangi bir dosya biçiminde kaydetmeyi destekler. Geliştiriciler ayrıca değişiklik, ekleme veya işleme amaçları için mevcut bir 3D sahne yükleyebilir.
###  **3D sahne belgesi oluşturma**
Aspose kullanarak 3D sahne belgesi oluşturmak için lütfen bu adımları izleyin. 3D apis:

1. 3D sahne belgesini temsil eden [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) sınıfının bir örneğini oluşturun.
1. Generate a 3D Scene document by calling the [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) method of the Scene class object.
####  **3D sahne belgesi oluşturma: programlama örnekleri**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
##  **3D sahnesini okumak**
Using Aspose.3D API, developers can load all the supported 3D documents. The available constructors of the **Sahne**Sınıf bunu yapmaya izin verir ve geçerli bir dosya yolu dizesini kabul ederler. To okunabilir dosya formatlarını aşağıdaki gibi destekledi:

1. FBX 7.7 (ascii, İkili)
1. FBX 7.6 (ascii, ikili)
1. FBX 7.5 (ascii, ikili)
1. FBX 7.4 (ascii, ikili)
1. FBX 7.3 (ascii, İkili)
1. FBX 7.2 (ascii, ikili)
1. STL (ascii, ikili)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ascii, ikili)
1. X (ASCI I, Binary)
1. XYZ
1. Draco
1. 3MF
1. RVM (metin, ikili)
1. ASE
1. USDZ
1. USD

Constructors of the `Scene` class detect 3D document format internally.
###  **3D sahne okuma: programlama örnekleri**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
