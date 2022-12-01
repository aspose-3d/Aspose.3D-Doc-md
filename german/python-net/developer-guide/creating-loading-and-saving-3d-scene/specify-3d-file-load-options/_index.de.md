---
title: Geben Sie 3D Datei lade optionen an
type: docs
weight: 30
url: /de/python-net/specify-3d-file-load-options/
description: Es gibt mehrere Scene.Open-Methode überlastet oder Scene-Class-Konstruktor-Überladungen, die ein Load Options-Objekt akzeptieren. Jedes Last format verfügt über eine entsprechende Klasse, die Last optionen für dieses Last format enthält.
---
## **3D Datei lade optionen**
Es gibt mehrere Überladungen von [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) Methoden oder Überlastungen von Scene-Klassen konstruktoren, die ein `LoadOptions`-Objekt akzeptieren. Dies sollte ein Objekt einer Klasse sein, die aus der Klasse `LoadOptions` abgeleitet ist. Jedes Lade format verfügt über eine entsprechende Klasse, die Last optionen für dieses Last format enthält. Beispiels weise gibt es `ColladaSaveOptions` für das Speicher format `FileFormat.Collada`.
### **Verwendung der diskreten Lade optionen 3DS**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine Discreet 3DS-Datei laden.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
### **Verwendung der Obj-Lade optionen**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine Obj-Datei 3D laden.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
### **Nutzung der Lade optionen STL**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine STL-Datei laden.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
### **Nutzung der Lade optionen U3D**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine U3D-Datei laden.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
### **Nutzung der Lade optionen glTF**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine glTF-Datei laden.
#### **Drehen Sie die V/T-Textur koordination um**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
### **Verwendung der Ply-Load-Optionen**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie ein PLY-Modell laden.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
### **Nutzung der Lade optionen DirectX X**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine DirectX X-Datei laden.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
### **Lade optionen RVM nutzen**
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

### **Verwendung von FBX Lade optionen**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
