---
title: Trabajando con cilindro
type: docs
weight: 100
url: /es/java/working-with-cylinder/
description: Aspose.3D for Java permite personalizar Offset Top de un cilindro. Para utilizar esta funcionalidad, puede utilizar el método setOffsetTop() de clase Cilindro.
---
# **Personalizar parte superior offset**
Aspose.3D for Java permite personalizar Offset Top de un cilindro. Para utilizar esta funcionalidad, puede utilizar el método `setOffsetTop()` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Offset Top:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

![Todo: imagen_Alt_Texto](working-with-cylinder_1.png)

El izquierdo tiene OffsetTop configurado en (5, 3, 0), es fácil ver que la tapa superior se ha movido y todo el torso también se ve afectado.
# **Personalizar ShearBottom**
Aspose.3D for Java permite personalizar el fondo de cizallamiento de un cilindro. Para utilizar esta funcionalidad, puede utilizar la propiedad `setShearBottom()` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Shear Bottom:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

![Todo: imagen_Alt_Texto](working-with-cylinder_2.png)

El cilindro izquierdo tiene ShearBottom a (0, 0,83) mientras que el derecho es un cilindro ordinal.
# **Crear ventilador-cilindro**
Aspose.3D for Java permite crear un cilindro de ventilador. Para utilizar esta funcionalidad, puede `setGenerateFanCylinder()` propiedad de `Cylinder` clase a `true`. El siguiente fragmento de código muestra cómo usar esta funcionalidad:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

![Todo: imagen_Alt_Texto](working-with-cylinder_3.png)

El cilindro izquierdo tiene GenerateFanCylinder = falso y el derecho tiene GenerateFanCylinder = true.
