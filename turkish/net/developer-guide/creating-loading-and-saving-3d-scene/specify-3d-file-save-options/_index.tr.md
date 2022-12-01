---
title: C# yılında Specify 3D File ave ave ptions ptions
linktitle: Specify 3D File ave ave ptions ptions
type: docs
weight: 40
url: /tr/net/specify-3d-file-save-options/
description: Tburada birkaç Scene.Save yöntemi, bir aveaveaveptions nesnesini kabul eden aşırı yükler. Each kaydetme formatı, bu kaydetme formatı için kaydetme seçeneklerini tutan ilgili bir sınıfa sahiptir.
---
## **Overview**

Tonun makalesi 3D dosyalarını farklı formatlara nasıl kaydedebileceğinizi açıklıyor[Onları cene cene nesnesine yükledikten sonra](https://docs.aspose.com/3d/net/specify-3d-file-load-options/)C# kullanarak. By yükleme ve kaydetme, örneğin farklı dönüşüm sayısını gerçekleştirebilirsiniz

- Convert FBX to X in C#
- Convert GLTF OBJ C#
- Convert OBJ to X in C#
- Convert STL OBJ C#
- Convert RVM 3DS C#

## **3D File ave ave ptions ptions**
Tburada bir aveaveaveptions nesnesini kabul eden birkaç [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) yöntemi aşırı yüklenir. This `SaveOptions` sınıfından türetilen bir sınıfın nesnesi olmalıdır. Each kaydetme formatı, bu kaydetme formatı için kaydetme seçeneklerini tutan ilgili bir sınıfa sahiptir, örneğin `FileFormat.Collada` kaydetme formatı için `ColladaSaveOptions` vardır.
### **Use of Collada ptions ave ptions ptions**
The C# kodu aşağıda 3D dosyasından Collada formatına kadar tasarruf seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
### **Use of Discreet3DS ptions ave ptions ptions**
The C# kodu aşağıda, 3D dosyasını bir Discreet 3DS formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
### **Use of FBX ptions ave ptions ptions**
The C# kodu aşağıda 3D dosyasını FBX formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` ayrıca FBX dosyasında büyük ikili verileri sıkıştırmak için kullanılabilecek `EnableCompression` özelliğini de ortaya çıkarır. Bu mülkün fault efault değeri doğrudur. Below kod snippet, bir sahneyi kaydederken bu mülkle nasıl çalışabileceğinizi açıklıyor.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
### **Bj se of the bj bj ptions ave ptions ptions**
The kodu aşağıda, 3D dosyasını bir Obj formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
### **Use of STL ptions ave ptions ptions**
The C# kodu aşağıda 3D dosyasından STL formatına kadar tasarruf seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
### **Use of U3D ptions ave ptions ptions**
The C# kodu aşağıda, bir belgeyi U3D formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
### **Use of glTF ptions ave ptions ptions**
{{% alert color="primary" %}} 

This özelliği 19.8 veya daha büyük sürümle desteklenir.

{{% /alert %}} 



The C# kodu aşağıda, bir belgeyi glTF formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
### **Prere07rint glTF ave ave ptions ptions**
You ayrıca insan-anlaşılabilir Jhuman print print baskı için PLproperty aveave. ptions sınıfının Pre. rinrint özelliğini de kullanabilir. The kodu aşağıda bu işlevselliğin nasıl kullanılacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
### **Real File stem ystem içinde 3D cene cene bir pendenave pendenependen**
Developers, gerçek dosya sisteminde 3D sahne bağımlılıklarını kaydetmeyi gerektirebilir. They yerel bir dizinin yolunu tanımlayabilir, `MemoryFileSystem` nesnesinden tasarruf edebilir veya sadece bağımlılıkları reddedebilir. The `FileSystem` özelliği tüm kaydetme seçeneği sınıflarına eklenir.
#### **Erial iscard erial aving erial aterial Files**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
#### **Local Directory içinde Dave pendenependencies**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
#### **MemoryFileSystem MemoryFileSystem bject'de pendenave pendenependencies**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
### **Use of Google Draco (.drc) ave ave ptions ptions**
The C# kodu aşağıda 3D modelinden DRC formatına kadar tasarruf seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
### **Use of RVM ptions ave ptions ptions**
The C# kodu aşağıda 3D modelinden RVM formatına kadar tasarruf seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
