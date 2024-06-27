---
title: Malla dividida
type: docs
weight: 10
url: /es/java/split-mesh/
description: Aspose.3D for Java API tiene soporte para dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena si se le ha asignado un único material. Se puede lograr usando Aspose.3D for Java API.
---
##  **Dividir todas las mallas de escena por material**
Aspose.3D for Java API tiene soporte para dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena si se le ha asignado un único material. Se puede lograr usando Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum especifica la política de datos utilizada en el algoritmo de división de malla, admite dos políticas, comparte datos entre submallas o cada submalla tiene sus propios datos (solo datos utilizados).

{{% /alert %}} 

El siguiente ejemplo de código divide todas las mallas de una escena por material. Cada sub-malla comparte los mismos datos directos y solo difiere en índices.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitAllMeshesofScenebyMaterial.java" >}}
##  **Dividir una malla especificando el material**
Aspose.3D for Java API tiene soporte para dividir una malla especificando manualmente el material. La opción de dividir malla crea objetos separados y cada submalla utilizará un solo material.
###  **Malla dividida de la caja**
Este tema de ayuda crea una malla de la caja para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda: [Crear una malla de cubo 3D](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Además, una caja está compuesta por 6 planos y cada plano se convertirá en una sub-malla. El ejemplo de código a continuación divide una malla primitiva especificando manualmente el material.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitMeshbyMaterial.java" >}}
