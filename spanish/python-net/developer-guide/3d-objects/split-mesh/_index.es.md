---
title: Malla dividida
type: docs
weight: 100
url: /es/python-net/split-mesh/
description: Los desarrolladores pueden requerir dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena Si se le ha asignado un único material. Los desarrolladores ahora pueden lograr esto usando Aspose.3D para Python via .NET API.
---
## **Dividir todas las mallas de una escena por material**
Los desarrolladores pueden requerir dividir todas las mallas de una escena en varias submallas por material. El método `split_mesh` no dividirá una malla de la escena Si se le ha asignado un solo material. Los desarrolladores ahora pueden lograr esto usando[Aspose.3D para Python via .NET](https://products.aspose.com/3d/python-net/)API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum especifica la política de datos utilizada en el algoritmo de división de malla, admite dos políticas, comparte datos entre sub-mallas o cada sub-malla tiene sus propios datos (solo se usan datos).

{{% /alert %}}

El siguiente ejemplo de código divide todas las mallas de una escena por material. Cada sub-malla comparte los mismos datos directos y solo difiere en índices.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
## **Dividir una malla especificando el material**
Aspose.3D para Python via .NET API permite a los desarrolladores dividir una malla especificando manualmente el material. La opción de malla dividida crea objetos separados y cada malla secundaria utilizará solo un material.
### **Dividir la malla de la caja**
Este tema de ayuda crea una malla de la caja para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda:[Crear una malla de cubo 3D](/3d/es/python-net/create-3d-mesh-and-scene/)... Además, una caja está compuesta por 6 planos y cada plano se convertirá en una malla secundaria. La siguiente muestra de código divide una malla primitiva especificando manualmente el material.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
