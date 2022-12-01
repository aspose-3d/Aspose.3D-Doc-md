---
title: Specify 3D ptions ile ile oad ptions
type: docs
weight: 30
url: /ar/python-net/specify-3d-file-load-options/
description: Tهنا العديد من method cene. cenطريقة القلم الزائد أو overcene الفئة منشئ الأحمال الزائدة التي تقبل كائن ptions oadO. تنسيق تحميل ach ach لديه فئة المقابلة التي تحمل خيارات الحمل لتنسيق الحمل هذا.
---
## **3D ptions ile ptions oad ptions**
في ما يلي العديد من [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) طريقة الأحمال الزائدة أو overcene الفئة منشئ الأحمال الزائدة التي تقبل كائن `LoadOptions`. Tيجب أن يكون كائن من فئة مشتقة من فئة `LoadOptions`. تنسيق تحميل ach ach لديه فئة المقابلة التي تحمل خيارات الحمل لتنسيق الحمل هذا ، على سبيل المثال هناك `ColladaSaveOptions` لتنسيق حفظ `FileFormat.Collada`.
### **Use من ptions iscreet 3DS ptions oad ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
### **Use من ptions bj ptions oad ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف 3D Obj.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
### **Use من STL ptions oad ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
### **Use من U3D ptions oad ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
### **Use من glTF ptions oad ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف glTF.
#### **Lip الشفاه V/T exexture ordinالمرؤوس**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
### **Use من ptions ly ptions oad ptions**
Tانه رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل نموذج PLY.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
### **Use من DirectX ptions ptions oad ptions**
Tيظهر الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف DirectX X.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
### **Use RVM خيارات التحميل**
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

### **Using FBX ptions oad ptions**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
