---
title: Specify 3D File Load Options
type: docs
weight: 30
url: /python-net/specify-3d-file-load-options/
description: There are several Scene.Open method overloads or Scene class constructor overloads that accept a LoadOptions object. Each load format has a corresponding class that holds load options for that load format.
---

## **3D File Load Options**
There are several [Scene.Open](https://apireference.aspose.com/3d/python-net/aspose.threed/scene) method overloads or Scene class constructor overloads that accept a LoadOptions object. This should be an object of a class derived from the LoadOptions class. Each load format has a corresponding class that holds load options for that load format, for example there is ColladaSaveOptions for the FileFormat.Collada save format.
### **Use of the Discreet 3DS Load Options**
The code below shows how to set load options before loading a Discreet 3DS file.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
### **Use of the Obj Load Options**
The code below shows how to set load options before loading an 3D Obj file.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
### **Use of the STL Load Options**
The code below shows how to set load options before loading an STL file.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
### **Use of the U3D Load Options**
The code below shows how to set load options before loading a U3D file.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
### **Use of the glTF Load Options**
The code below shows how to set load options before loading a glTF file.
#### **Flip the V/T Texture Coordinate**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
### **Use of the Ply Load Options**
The code below shows how to set load options before loading a PLY model.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
### **Use of the DirectX X Load Options**
The code below shows how to set load options before loading a DirectX X file.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
### **Use RVM load options**
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

### **Using FBX Load Options**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
