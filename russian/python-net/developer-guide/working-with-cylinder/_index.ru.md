---
title: Работа с цилиндром
type: docs
weight: 130
url: /ru/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET позволяет настроить Offset Top цилиндра. Для того, чтобы использовать эту функциональность, вы можете использовать свойство Offset класса Cylinder.
---
#  **Настроить офсетный топ**
Aspose.3D for Python via .NET позволяет настроить Offset Top цилиндра. Чтобы использовать эту функциональность, вы можете использовать свойство `offset` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Offset Top:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

! [Для: имаге_альт_текст](working-with-cylinder_1.png)

На левой стороне `offset_top` установлено значение (5, 3, 0), легко увидеть, что верхняя крышка сдвинулась, и все туловище также пострадало.
#  **Настроить ShearBottom**
Aspose.3D for Python via .NET позволяет настраивать срезное дно цилиндра. Чтобы использовать эту функциональность, вы можете использовать свойство `shear_bottom` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить дно сдвига:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

! [Для: имаге_альт_текст](working-with-cylinder_2.png)

Левый цилиндр имеет от `shear_bottom` до (0, 0,83), а правый-порядковый цилиндр.
#  **Создать вентилятор-цилиндр**
Aspose.3D for Python via .NET позволяет создать цилиндр вентилятора. Чтобы использовать эту функцию, вы можете установить свойство `generate_fan_cylinder` класса `Cylinder` на `True`. Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

! [Для: имаге_альт_текст](working-with-cylinder_3.png)

Левый цилиндр имеет `generate_fan_cylinder = False`, а правый-`generate_fan_cylinder = True`.
