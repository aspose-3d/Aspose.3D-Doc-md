---
title: Specify 3D File ptions oad ptions ptions
type: docs
weight: 30
url: /tr/python-net/specify-3d-file-load-options/
description: Tburada birkaç Scene vardır. Open yöntemi aşırı yükler veya bir Load. ptions nesnesini kabul eden aşırı yükler. Each yük formatı, bu yük formatı için yük seçeneklerini tutan ilgili bir sınıfa sahiptir.
---
## **3D File Load ptions ptions**
Tburada [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) yöntemi aşırı yükler veya `LoadOptions` nesnesini kabul eden Scene sınıfı oluşturucu aşırı yükler vardır. This `LoadOptions` sınıfından türetilen bir sınıfın nesnesi olmalıdır. Each yük formatı, bu yük formatı için yük seçeneklerini tutan ilgili bir sınıfa sahiptir, örneğin 076. 481 kaydetme formatı için `ColladaSaveOptions` vardır.
### **Discreet 3DS Load ptions ptions ptions**
To kodu aşağıda, bir Discreet 3DS dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
### **Bj bj ptions oad ptions ptions**
Aşağıdaki kod, 3D Obj dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
### **Use of STL ptions oad ptions ptions**
The kodu, STL dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
### **Use of U3D ptions oad ptions ptions**
The kodu, U3D dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
### **Use of glTF ptions oad ptions ptions**
The kodu, glTF dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.
#### **Lip lip V/T Texture ordinoordinate**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
### **Pse of Ply Load ptions ptions**
The kodu, PLY modelini yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
### **Use of DirectX X Load ptions ptions**
The kodu, DirectX X dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
### **Use RVM yük seçenekleri**
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

### **Using FBX Load ptions ptions**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
