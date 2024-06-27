---
title: Trabajando con cilindro
type: docs
weight: 100
url: /es/java/working-with-cylinder/
description: Aspose.3D for Java permite personalizar Offset Top of a cylinder. Para utilizar esta funcionalidad, puede utilizar el método setOffsetTop() de la clase Cylinder.
---
#  **Personalizar parte superior offset**
Aspose.3D for Java permite personalizar Offset Top of a cylinder. Para usar esta funcionalidad, puede usar el método `setOffsetTop()` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Offset Top:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

¡! [Todo: image_alt_text](working-with-cylinder_1.png)

El izquierdo tiene OffsetTop configurado en (5, 3, 0), es fácil ver que la tapa superior se ha movido y todo el torso también se ve afectado.
#  **Personalizar ShearBottom**
Aspose.3D for Java permite personalizar el fondo de corte de un cilindro. Para usar esta funcionalidad, puede usar la propiedad `setShearBottom()` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Shear Bottom:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

¡! [Todo: image_alt_text](working-with-cylinder_2.png)

El cilindro izquierdo tiene ShearBottom a (0, 0,83) mientras que el derecho es un cilindro ordinal.
#  **Crear ventilador-cilindro**
Aspose.3D for Java permite crear un cilindro de ventilador. Para utilizar esta funcionalidad, puede `setGenerateFanCylinder()` propiedad de `Cylinder` clase a `true`. El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

¡! [Todo: image_alt_text](working-with-cylinder_3.png)

El cilindro izquierdo tiene GenerateFanCylinder = falso y el derecho tiene GenerateFanCylinder = true.
