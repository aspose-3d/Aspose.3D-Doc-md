---
title: Malla dividida
type: docs
weight: 100
url: /es/net/split-mesh/
description: Los desarrolladores pueden requerir dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena si se le ha asignado un único material. Los desarrolladores ahora pueden lograr esto usando Aspose.3D for .NET API.
---
##  **Dividir todas las mallas de una escena por material**
Los desarrolladores pueden requerir dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena si se le ha asignado un único material. Los desarrolladores ahora pueden lograr esto usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum especifica la política de datos utilizada en el algoritmo de división de malla, admite dos políticas, comparte datos entre submallas o cada submalla tiene sus propios datos (solo datos utilizados).

{{% /alert %}}

El siguiente ejemplo de código divide todas las mallas de una escena por material. Cada sub-malla comparte los mismos datos directos y solo difiere en índices.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.cs" >}}
##  **Dividir una malla especificando el material**
Aspose.3D for .NET API permite a los desarrolladores dividir una malla especificando manualmente el material. La opción de dividir malla crea objetos separados y cada submalla utilizará un solo material.
###  **Dividir la malla de la caja**
Este tema de ayuda crea una malla de la caja para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda: [Crear una malla de cubo 3D](/3d/es/net/create-3d-mesh-and-scene/). Además, una caja está compuesta por 6 planos y cada plano se convertirá en una sub-malla. El ejemplo de código siguiente divide una malla primitiva especificando manualmente el material.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.cs" >}}
