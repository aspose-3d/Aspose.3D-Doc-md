---
title: Lavorare con il cilindro
type: docs
weight: 100
url: /it/java/working-with-cylinder/
description: Aspose.3D for Java consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, è possibile utilizzare setMetodo OffsetTop() della classe Cilindro.
---
#  **Personalizza la parte superiore offset**
Aspose.3D for Java consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, è possibile utilizzare il metodo `setOffsetTop()` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare Offset Top:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

! [Todo: image_alt_text](working-with-cylinder_1.png)

Quello sinistro ha OffsetTop impostato su (5, 3, 0), è facile vedere che il tappo superiore si è spostato e anche l'intero busto ne viene influenzato.
#  **Personalizza ShearBottom**
Aspose.3D for Java consente di personalizzare il fondo di taglio di un cilindro. Per utilizzare questa funzionalità, puoi utilizzare la proprietà `setShearBottom()` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare il fondo di taglio:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

! [Todo: image_alt_text](working-with-cylinder_2.png)

Il cilindro sinistro ha ShearBottom a (0, 0,83) mentre quello destro è un cilindro ordinale.
#  **Crea Ventilatore-Cilindro**
Aspose.3D for Java consente di creare un cilindro della ventola. Per poter utilizzare questa funzionalità, puoi `setGenerateFanCylinder()` di proprietà della classe `Cylinder` a `true`. Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

! [Todo: image_alt_text](working-with-cylinder_3.png)

Il cilindro sinistro ha GenerateFanCylinder = falso e quello destro ha GenerateFanCylinder = true.
