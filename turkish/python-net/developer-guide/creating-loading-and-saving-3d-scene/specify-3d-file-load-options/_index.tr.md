---
title: 3D dosya yükleme seçeneklerini belirtin
type: docs
weight: 30
url: /tr/python-net/specify-3d-file-load-options/
description: Tburada birkaç Scene vardır. Open yöntemi aşırı yükler veya bir Load. ptions nesnesini kabul eden aşırı yükler. Each yük formatı, bu yük formatı için yük seçeneklerini tutan ilgili bir sınıfa sahiptir.
---
##  **3D dosya yükleme seçenekleri**
There are several [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) method overloads or Scene class constructor overloads that accept a `LoadOptions` object. This should be an object of a class derived from the `LoadOptions` class. Each load format has a corresponding class that holds load options for that load format, for example there is `ColladaSaveOptions` for the `FileFormat.Collada` save format.
###  **Gizli 3DS yük seçeneklerinin kullanımı**
Aşağıdaki kod, gizli bir 3DS dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
###  **Bj bj ptions oad ptions ptions**
Aşağıdaki kod, 3D obj dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
###  **STL yük seçeneklerinin kullanımı**
Aşağıdaki kod, STL dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
###  **U3D yük seçeneklerinin kullanımı**
Aşağıdaki kod, U3D dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
###  **glTF yük seçeneklerinin kullanımı**
Aşağıdaki kod, glTF dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.
####  **Lip lip V/T Texture ordinoordinate**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
###  **Pse of Ply Load ptions ptions**
Aşağıdaki kod, PLY modelini yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
###  **DirectiX LLoad ptions ptions se**
To kodu aşağıda bir Directfile dosya yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
###  **Use RVM load options**
**C#**

```py


import aspose.threed as a3d
# set load options of RVM

scene = a3d.Scene()

opt = a3d.formats.RvmLoadOptions()
opt.cylinder_radial_segments = 32
opt.dish_latitude_segments = 16
opt.dish_longitude_segments = 24
opt.torus_tubular_segments = 40

# import RVM

scene.open("LAD-TOP.rvm", opt);

# save in the OBJ format

scene.save("LAD-TOP.obj", a3d.FileFormat.WAVEFRONT_OBJ);

```

###  **Using FBX Load Options**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
