---
title: Specify 3D File ave ave ptions ptions
type: docs
weight: 40
url: /tr/python-net/specify-3d-file-save-options/
description: Tburada birkaç Scene.Save yöntemi, bir aveaveaveptions nesnesini kabul eden aşırı yükler. Each kaydetme formatı, bu kaydetme formatı için kaydetme seçeneklerini tutan ilgili bir sınıfa sahiptir.
---
## **3D File ave ave ptions ptions**
T`SaveOptions` nesnesini kabul eden birkaç [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) yöntemi aşırı yüklenir. This `SaveOptions` sınıfından türetilen bir sınıfın nesnesi olmalıdır. Each kaydetme formatı, bu kaydetme formatı için kaydetme seçeneklerini tutan ilgili bir sınıfa sahiptir, örneğin 076. 481 kaydetme formatı için `ColladaSaveOptions` vardır.
### **Use of Collada ptions ave ptions ptions**
Aşağıdaki kod, 3D dosyasını Collada formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
### **Use of Discreet3DS ptions ave ptions ptions**
Aşağıdaki kod, 3D dosyasını bir 07iscreet 3DS formatına kaydetmeden önce kaydetme seçeneklerini nasıl ayarlayacağınızı gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
### **Use of FBX ptions ave ptions ptions**
The kodu, 3D dosyasını FBX formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` ayrıca FBX dosyasında büyük ikili verileri sıkıştırmak için kullanılabilecek `enable_compression` özelliğini de ortaya çıkarır. Bu mülkün fault efault değeri doğrudur. Below kod snippet, bir sahneyi kaydederken bu mülkle nasıl çalışabileceğinizi açıklıyor.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
### **Bj se of the bj bj ptions ave ptions ptions**
The kodu aşağıda, 3D dosyasını bir Obj formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
### **Use of STL ptions ave ptions ptions**
Aşağıdaki kod, 3D dosyasını STL formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
### **Use of U3D ptions ave ptions ptions**
The kodu aşağıda, bir belgeyi U3D formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
### **Use of glTF ptions ave ptions ptions**
{{% alert color="primary" %}} 

This özelliği 19.8 veya daha büyük sürümle desteklenir.

{{% /alert %}} 



The kodu aşağıda, bir belgeyi glTF formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
### **Prere07rint glTF ave ave ptions ptions**
You ayrıca insan-anlaşılabilir Jhuman print print baskı için PLproperty aveave. ptions sınıfının Pre. rinrint özelliğini de kullanabilir. The kodu aşağıda bu işlevselliğin nasıl kullanılacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
### **Real File stem ystem içinde 3D cene cene bir pendenave pendenependen**
Developers, gerçek dosya sisteminde 3D sahne bağımlılıklarını kaydetmeyi gerektirebilir. They, yerel bir dizinin yolunu tanımlayabilir, MemoryFileSystem nesnesine kaydedebilir veya sadece bağımlılıkları atabilir. The Filestem ystem özelliği tüm kaydetme seçeneği sınıflarına eklenir.
#### **Erial iscard erial aving erial aterial Files**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
#### **Local Directory içinde Dave pendenependencies**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
#### **MemoryFileSystem MemoryFileSystem bject'de pendenave pendenependencies**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
### **Use of Google Draco (.drc) ave ave ptions ptions**
The kodu aşağıda 3D modelini DRC formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
### **Use of RVM ptions ave ptions ptions**
The kodu aşağıda 3D modelini RVM formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
