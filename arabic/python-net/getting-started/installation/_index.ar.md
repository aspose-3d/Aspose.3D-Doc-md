---
title: Installation
type: docs
weight: 40
url: /ar/python-net/installation/
---
## **متطلبات النظام**

First ، عليك التحقق والتأكد من أن مواصفات الجهاز تلبي[متطلبات النظام](/3d/ar/python-net/system-requirements/).

## **Instيعادل Aspose.3D ل Python via .NET**
`pip` هي أسهل طريقة لتحميل وتركيب[Aspose.3D ل Python via .NET](https://pypi.org/project/aspose-3d/).

To تثبيت Aspose.3D ، قم بتشغيل هذا الأمر: تثبيت pip aspose-3d

## **Using Aspose.3D ل Python via .NET**

Once يمكنك الانتهاء من تثبيت الوحدة النمطية ، يمكنك استخدام Aspose.3D من رمز بايثون الخاص بك بهذه الطريقة:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

