---
title: Lavorare con il cilindro
type: docs
weight: 130
url: /it/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, è possibile utilizzare la proprietà Offset della classe Cilindro.
---
#  **Personalizza la parte superiore offset**
Aspose.3D for Python via .NET consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, puoi utilizzare la proprietà `offset` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare Offset Top:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

! [Todo: image_alt_text](working-with-cylinder_1.png)

Quello sinistro ha `offset_top` impostato su (5, 3, 0), è facile vedere che il tappo superiore si è spostato e anche l'intero busto ne viene influenzato.
#  **Personalizza ShearBottom**
Aspose.3D for Python via .NET consente di personalizzare il fondo di taglio di un cilindro. Per utilizzare questa funzionalità, puoi utilizzare la proprietà `shear_bottom` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare il fondo di taglio:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

! [Todo: image_alt_text](working-with-cylinder_2.png)

Il cilindro sinistro ha `shear_bottom` a (0, 0,83) mentre quello destro è un cilindro ordinale.
#  **Crea Ventilatore-Cilindro**
Aspose.3D for Python via .NET consente di creare un cilindro della ventola. Per poter utilizzare questa funzionalità, puoi impostare la proprietà `generate_fan_cylinder` della classe `Cylinder` su `True`. Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

! [Todo: image_alt_text](working-with-cylinder_3.png)

Il cilindro sinistro ha `generate_fan_cylinder = False` e quello destro ha `generate_fan_cylinder = True`.
