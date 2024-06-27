---
title: Trabajando con cilindro
type: docs
weight: 130
url: /es/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET permite personalizar Offset Top of a cylinder. Para utilizar esta funcionalidad, puede utilizar la propiedad Offset de la clase Cylinder.
---
#  **Personalizar parte superior offset**
Aspose.3D for Python via .NET permite personalizar Offset Top of a cylinder. Para usar esta funcionalidad, puede usar la propiedad `offset` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Offset Top:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

¡! [Todo: image_alt_text](working-with-cylinder_1.png)

El izquierdo tiene `offset_top` establecido en (5, 3, 0), es fácil ver que la tapa superior se ha movido y todo el torso también se ve afectado.
#  **Personalizar ShearBottom**
Aspose.3D for Python via .NET permite personalizar el fondo de corte de un cilindro. Para usar esta funcionalidad, puede usar la propiedad `shear_bottom` de la clase `Cylinder`. El siguiente fragmento de código muestra cómo personalizar Shear Bottom:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

¡! [Todo: image_alt_text](working-with-cylinder_2.png)

El cilindro izquierdo tiene `shear_bottom` a (0, 0,83) mientras que el derecho es un cilindro ordinal.
#  **Crear ventilador-cilindro**
Aspose.3D for Python via .NET permite crear un cilindro de ventilador. Para utilizar esta funcionalidad, puede establecer la propiedad `generate_fan_cylinder` de la clase `Cylinder` en `True`. El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

¡! [Todo: image_alt_text](working-with-cylinder_3.png)

El cilindro izquierdo tiene `generate_fan_cylinder = False` y el derecho tiene `generate_fan_cylinder = True`.
