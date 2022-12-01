---
title: Работа с цилиндром
type: docs
weight: 100
url: /ru/java/working-with-cylinder/
description: Aspose.3D for Java позволяет настраивать смещение верхней части цилиндра. Чтобы использовать эту функциональность, вы можете использовать метод setOffsetTop() класса Cylinder.
---
# **Настроить офсетный топ**
Aspose.3D for Java позволяет настраивать смещение верхней части цилиндра. Чтобы использовать эту функциональность, вы можете использовать метод `setOffsetTop()` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Offset Top:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

![Todo: изображение_Альт_Текст](working-with-cylinder_1.png)

У левого есть OffsetTop (5, 3, 0), легко увидеть, что верхняя крышка сдвинулась, и весь туловище также пострадает.
# **Настроить ShearBottom**
Aspose.3D for Java позволяет настраивать срезное дно цилиндра. Для того, чтобы использовать этот функционал, вы можете использовать свойство `setShearBottom()` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Shear Bottom:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

![Todo: изображение_Альт_Текст](working-with-cylinder_2.png)

Левый цилиндр имеет ShearBottom до (0, 0,83), а правый-порядковый цилиндр.
# **Создать вентилятор-цилиндр**
Aspose.3D for Java позволяет создавать цилиндр вентилятора. Чтобы использовать эту функциональность, вы можете `setGenerateFanCylinder()` свойство класса `Cylinder` до `true`. Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

![Todo: изображение_Альт_Текст](working-with-cylinder_3.png)

Левый цилиндр имеет GenerateFanCylinder = false, а правый-GenerateFanCylinder = true.
