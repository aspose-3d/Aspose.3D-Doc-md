---
title: 3D dosya kaydetme seçeneklerini belirtin
type: docs
weight: 10
url: /tr/java/specify-3d-file-save-options/
description: Tburada birkaç Scene vardır. save aveaveptions örneğini kabul eden aşırı yükleme yöntemi kaydedin.
---
##  **3D dosya kaydetme seçenekleri**
Tburada birkaç Scene vardır. save aveaveptions örneğini kabul eden aşırı yükleme yöntemi kaydedin. This, Saveaveptions sınıfından türetilen bir sınıfın örneği olmalıdır. Each kaydetme formatı, bu kaydetme formatı için kaydetme seçeneklerini tutan karşılık gelen bir sınıfa sahiptir, örneğin Fileiormat için Collada. ave. ptions. save format format format format format save save format.
###  **Collada kaydet seçeneklerinin kullanımı**
The code below shows how to set save options before saving a 3D file in Collada format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
###  **Discreet3DS kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, 3D dosyasını gizli bir 3DS formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
###  **FBX kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, 3D dosyasını FBX formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
###  **OBJ kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, bir obj formatına 3D dosyasını kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
###  **STL kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, 3D dosyasını STL formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
###  **U3D kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, bir belgeyi U3D formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
###  **glTF kaydet seçeneklerinin kullanımı**
{{% alert color="primary" %}} 

This özelliği 19.8 veya daha büyük sürümle desteklenir.

{{% /alert %}} 



Aşağıdaki kod, bir belgeyi glTF formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
###  **Preprint print glTF kaydet seçenekleri**
You ayrıca insan anlaşılabilir understandable human human print print aveave. ptions sınıfı setPre. rinrint yöntemini de kullanabilir. The kodu aşağıda bu işlevselliğin nasıl kullanılacağını gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
###  **Gerçek dosya sisteminde 3D sahnenin bağımlılıklarını kaydedin**
Geliştiriciler, gerçek dosya sisteminde 3D sahnesinin tüm bağımlılıklarını kaydetmeyi gerektirebilir. Yerel bir dizinin yolunu tanımlayabilir, `MemoryFileSystem` nesnesinden tasarruf edebilir veya sadece bağımlılıkları atabilirler. Dosya sistemi özelliği tüm kaydetme seçeneği sınıflarına eklenir.
####  **Erial iscard erial aving erial aterial Files**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
####  **Local Directory içinde Dave pendenependencies**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
####  **MemoryFileSystem stance stance nstance içinde Dave pendenependencies**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
###  **Google Draco (.DRC) kullanım seçenekleri kaydedin**
Aşağıdaki kod, 3D modelini DRC formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
###  **RVM kaydet seçeneklerinin kullanımı**
Aşağıdaki kod, 3D modelini RVM formatına kaydetmeden önce kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
