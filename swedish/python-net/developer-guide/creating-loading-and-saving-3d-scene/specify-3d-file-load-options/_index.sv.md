---
title: Ange 3D Filladdningsalternativ
type: docs
weight: 30
url: /sv/python-net/specify-3d-file-load-options/
description: Det finns flera Scene.Öppen metod överbelastning eller Scene klass konstruktor överbelastning som accepterar ett LoadOptions objekt. Varje lastformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet.
---
## **3D Filladdningsalternativ**
Det finns flera metodöverbelastningar [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) eller Scene klass konstruktor överbelastningar som accepterar ett `LoadOptions` objekt. Detta bör vara föremål för en klass som härrör från klassen `LoadOptions`. Varje belastningsformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet. till exempel finns det `ColladaSaveOptions` för `FileFormat.Collada` sparformat.
### **Användning av diskret 3DS lastalternativ**
Koden nedan visar hur man ställer in lastalternativ innan man laddar en diskret 3DS-fil.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
### **Användning av Obj-lastalternativ**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en 3D Obj-fil.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
### **Användning av belastningsalternativ STL**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en STL-fil.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
### **Användning av belastningsalternativ U3D**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en U3D-fil.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
### **Användning av belastningsalternativ glTF**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en glTF-fil.
#### **Vänd V/T texturkoordinat**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
### **Användning av Ply-lastalternativ**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en PLY modell.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
### **Användning av DirectX X-lastalternativ**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en DirectX X-fil.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
### **Använd RVM belastningsalternativ**
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

### **Använda FBX lastalternativ**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
