---
title: Lavorare con il cilindro
type: docs
weight: 130
url: /it/net/working-with-cylinder/
description: Aspose.3D for .NET consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, è possibile utilizzare la proprietà Offset della classe Cilindro.
---
#  **Personalizza la parte superiore offset**
Aspose.3D for .NET consente di personalizzare la parte superiore offset di un cilindro. Per utilizzare questa funzionalità, puoi utilizzare la proprietà `Offset` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare Offset Top:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedOffsetTopCylinder-1.cs" >}}

! [Todo: image_alt_text](working-with-cylinder_1.png)

Quello sinistro ha OffsetTop impostato su (5, 3, 0), è facile vedere che il tappo superiore si è spostato e anche l'intero busto ne viene influenzato.
#  **Personalizza ShearBottom**
Aspose.3D for .NET consente di personalizzare il fondo di taglio di un cilindro. Per utilizzare questa funzionalità, puoi utilizzare la proprietà `ShearBottom` della classe `Cylinder`. Il seguente frammento di codice mostra come personalizzare il fondo di taglio:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

! [Todo: image_alt_text](working-with-cylinder_2.png)

Il cilindro sinistro ha `ShearBottom` a (0, 0,83) mentre quello destro è un cilindro ordinale.
#  **Crea Ventilatore-Cilindro**
Aspose.3D for .NET consente di creare un cilindro della ventola. Per poter utilizzare questa funzionalità, puoi impostare la proprietà `GenerateFanCylinder` della classe `Cylinder` su `true`. Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

! [Todo: image_alt_text](working-with-cylinder_3.png)

Il cilindro sinistro ha `GenerateFanCylinder = false` e quello destro ha `GenerateFanCylinder = true`.
