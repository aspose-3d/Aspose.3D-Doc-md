---
title: 3D dosya kaydetme seçeneklerini belirtin
type: docs
weight: 40
url: /tr/python-net/specify-3d-file-save-options/
description: Tburada birkaç Scene.Save yöntemi, bir aveaveaveptions nesnesini kabul eden aşırı yükler. Each kaydetme formatı, bu kaydetme formatı için kaydetme seçeneklerini tutan ilgili bir sınıfa sahiptir.
---
##  **3D dosya kaydetme seçenekleri**
There are several [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) method overloads that accept a `SaveOptions` object. This should be an object of a class derived from the `SaveOptions` class. Each save format has a corresponding class that holds save options for that save format, for example, there is `ColladaSaveOptions` for the `FileFormat.Collada` save format.
###  **Collada kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, 3D dosyasını Collada formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
###  **Discreet3DS kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, 3D dosyasını gizli bir 3DS formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
###  **FBX kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, 3D dosyasını FBX formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` ayrıca FBX dosyasında büyük ikili verileri sıkıştırmak için kullanılabilecek `enable_compression` özelliğini de ortaya çıkarır. Bu özelliğin varsayılan değeri doğrudur. Aşağıdaki kod parçacığı, bir sahneyi kaydederken bu mülkle nasıl çalışabileceğinizi açıklar.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
###  **Bj se of the bj bj ptions ave ptions ptions**
Aşağıdaki kod, bir obj formatına 3D dosyasını kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
###  **STL kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, 3D dosyasını STL formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
###  **U3D kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, bir belgeyi U3D formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
###  **glTF kaydet seçeneklerinin kullanımı**
{{% alert color="primary" %}} 

This özelliği 19.8 veya daha büyük sürümle desteklenir.

{{% /alert %}} 



Aşağıdaki kod, bir belgeyi glTF formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
###  **Preprint print glTF kaydet seçenekleri**
You ayrıca insan-anlaşılabilir Jhuman print print baskı için PLproperty aveave. ptions sınıfının Pre. rinrint özelliğini de kullanabilir. The kodu aşağıda bu işlevselliğin nasıl kullanılacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
###  **Gerçek dosya sisteminde 3D sahnenin bağımlılıklarını kaydedin**
Developers may require to save all 3D scene dependencies in the real file system. They can define the path of a local directory, save in the MemoryFileSystem object or simply discard dependencies. The FileSystem property is added in the all save option classes.
####  **Erial iscard erial aving erial aterial Files**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
####  **Local Directory içinde Dave pendenependencies**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
####  **MemoryFileSystem MemoryFileSystem bject'de pendenave pendenependencies**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
###  **Google Draco (.drc) kullanım seçenekleri kaydedin**
Aşağıdaki kod, 3D modelini DRC formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
###  **RVM kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, 3D modelini RVM formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
