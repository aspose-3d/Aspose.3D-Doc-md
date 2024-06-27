---
title: Работа с цилиндром
type: docs
weight: 130
url: /ru/net/working-with-cylinder/
description: Aspose.3D for .NET позволяет настроить верх цилиндра со смещением. Для того, чтобы использовать эту функциональность, вы можете использовать свойство Offset класса Cylinder.
---
#  **Настроить офсетный топ**
Aspose.3D for .NET позволяет настроить верх цилиндра со смещением. Чтобы использовать эту функциональность, вы можете использовать свойство `Offset` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить Offset Top:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedOffsetTopCylinder-1.cs" >}}

! [Для: имаге_альт_текст](working-with-cylinder_1.png)

У левого есть OffsetTop (5, 3, 0), легко увидеть, что верхняя крышка сдвинулась, и весь туловище также пострадает.
#  **Настроить ShearBottom**
Aspose.3D for .NET позволяет настраивать срезное дно цилиндра. Чтобы использовать эту функциональность, вы можете использовать свойство `ShearBottom` класса `Cylinder`. Следующий фрагмент кода показывает, как настроить дно сдвига:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

! [Для: имаге_альт_текст](working-with-cylinder_2.png)

Левый цилиндр имеет от `ShearBottom` до (0, 0,83), а правый-порядковый цилиндр.
#  **Создать вентилятор-цилиндр**
Aspose.3D for .NET позволяет создать цилиндр вентилятора. Чтобы использовать эту функцию, вы можете установить свойство `GenerateFanCylinder` класса `Cylinder` на `true`. Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

! [Для: имаге_альт_текст](working-with-cylinder_3.png)

Левый цилиндр имеет `GenerateFanCylinder = false`, а правый-`GenerateFanCylinder = true`.
