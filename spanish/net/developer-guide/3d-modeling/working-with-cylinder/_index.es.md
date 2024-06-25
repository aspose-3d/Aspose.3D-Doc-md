---
title: Trabajando con cilindro
type: docs
weight: 130
url: /es/net/working-with-cylinder/
description: Aspose.3D for .NET permite personalizar Offset Top of a cylinder. Para utilizar esta funcionalidad, puede utilizar la propiedad Offset de la clase Cylinder.
---
#  **Personalizar parte superior offset**
Aspose.3D for .NET permite personalizar Offset Top of a cylinder. Para usar esta funcionalidad, puede usar la propiedad `Offset` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Offset Top:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedOffsetTopCylinder-1.cs" >}}

¡! [Todo: image_alt_text](working-with-cylinder_1.png)

El izquierdo tiene OffsetTop configurado en (5, 3, 0), es fácil ver que la tapa superior se ha movido y todo el torso también se ve afectado.
#  **Personalizar ShearBottom**
Aspose.3D for .NET permite personalizar el fondo de corte de un cilindro. Para usar esta funcionalidad, puede usar la propiedad `ShearBottom` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Shear Bottom:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

¡! [Todo: image_alt_text](working-with-cylinder_2.png)

El cilindro izquierdo tiene `ShearBottom` a (0, 0,83) mientras que el derecho es un cilindro ordinal.
#  **Crear ventilador-cilindro**
Aspose.3D for .NET permite crear un cilindro de ventilador. Para utilizar esta funcionalidad, puede establecer la propiedad `GenerateFanCylinder` de la clase `Cylinder` en `true`. El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

¡! [Todo: image_alt_text](working-with-cylinder_3.png)

El cilindro izquierdo tiene `GenerateFanCylinder = false` y el derecho tiene `GenerateFanCylinder = true`.
