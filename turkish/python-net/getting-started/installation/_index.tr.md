---
title: Stalnstallation
type: docs
weight: 40
url: /tr/python-net/installation/
---
## **sistem gereksinimleri**

First, makinenin özelliklerinin karşılandığını kontrol etmeli ve onaylamalısınız.[Sistem gereksinimleri](/3d/tr/python-net/system-requirements/).

## **Python via .NET için 07nstalling Aspose.3D**
`pip` indirmek ve yüklemek için en kolay yoldur[Python via .NET için Aspose.3D](https://pypi.org/project/aspose-3d/).

To Aspose.3D yükleyin, bu komutu çalıştırın: pip yükle aspose-3d

## **Python via .NET için 07sing Aspose.3D**

Modülü yüklemeyi bitirdiğinizde, python kodunuzdan Aspose.3D kullanabilirsiniz:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

