---
title: Работа с цилиндром
type: docs
weight: 130
url: /ru/python-net/working-with-cylinder/
description: Aspose.3D для Python via .NET позволяет настраивать смещение верхней части цилиндра. Чтобы использовать эту функциональность, вы можете использовать свойство Offset класса Cylinder.
---
# **Настроить офсетный топ**
Aspose.3D для Python via .NET позволяет настраивать смещение верхней части цилиндра. Для того, чтобы использовать этот функционал, вы можете использовать свойство `offset` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Offset Top:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

![Todo: изображение_Альт_Текст](working-with-cylinder_1.png)

Левый имеет настроенный на `offset_top` (5, 3, 0), легко увидеть, что верхняя крышка сдвинулась, и весь туловище также пострадает.
# **Настроить ShearBottom**
Aspose.3D для Python via .NET позволяет настраивать срезное дно цилиндра. Для того, чтобы использовать этот функционал, вы можете использовать свойство `shear_bottom` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Shear Bottom:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![Todo: изображение_Альт_Текст](working-with-cylinder_2.png)

Левый цилиндр имеет `shear_bottom` до (0, 0,83), а правый-порядковый цилиндр.
# **Создать вентилятор-цилиндр**
Aspose.3D для Python via .NET позволяет создавать цилиндр вентилятора. Чтобы использовать эту функциональность, вы можете установить свойство `generate_fan_cylinder` класса `Cylinder` на `True`. Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![Todo: изображение_Альт_Текст](working-with-cylinder_3.png)

Левый цилиндр имеет `generate_fan_cylinder = False`, а правый-`generate_fan_cylinder = True`.
