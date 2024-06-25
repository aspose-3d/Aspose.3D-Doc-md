---
title: Installation
type: docs
weight: 40
url: /ar/python-net/installation/
---
##  **متطلبات النظام**

أولاً ، يجب عليك التحقق والتأكد من أن مواصفات الجهاز تفي بسعر [متطلبات النظام](/3d/ar/python-net/system-requirements/).

##  **تثبيت Aspose.3D for Python via .NET**
`pip` هو أسهل طريقة لتنزيل وتثبيت [Aspose.3D for Python via .NET](https://pypi.org/project/aspose-3d/).

لتثبيت Aspose.3D تشغيل هذا الأمر: تثبيت نقطة

##  **Using Aspose.3D for Python via .NET**

بمجرد الانتهاء من تثبيت الوحدة ، يمكنك استخدام Aspose.3D من رمز بايثون بهذه الطريقة:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

