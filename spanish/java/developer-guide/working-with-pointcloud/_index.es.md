---
title: Trabajar con PointCloud
type: docs
weight: 110
url: /es/java/working-with-pointcloud/
description: Aspose.3D for Java permite decodificar una malla de un archivo Draco directamente sin construir una escena usando el método de decodificación de la clase DracoFormat.
---
#  **Decodificar malla**
Aspose.3D for Java permite decodificar una malla de un archivo Draco directamente sin construir una escena usando el método [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) de la clase [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-DecodeMesh-1.java" >}}
#  **Codificar malla**
Aspose.3D for Java permite codificar una malla de esfera en un archivo Draco directamente sin construir una escena usando el método [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) de la clase [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMesh-1.java" >}}
#  **Codificar Esfera como PointCloud**
Aspose.3D for Java permite codificar una malla de esfera en un archivo Draco como una nube de puntos utilizando el método [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) de la clase [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeSphereAsPointCloud-1.java" >}}
#  **Encode Mesh a PLY**
Aspose.3D for Java permite codificar una malla en un archivo PLY directamente sin construir una escena usando el método [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) de la clase [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Decodificar malla desde PLY**
Aspose.3D for Java permite decodificar una malla/nube de puntos a partir de un archivo PLY usando el método [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-) de la clase [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Exportar a PLY como PointCloud**
Aspose.3D for Java permite exportar una escena a PLY como PointCloud utilizando el método [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-) de la clase [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-ExportToPlyAsPointCloud-1.java" >}}
#  **Exportar escena 3D como nube de puntos**
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 

Aspose.3D for Java permite exportar una escena 3D como PointCloud utilizando el método [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) de la clase [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-Export3DSceneAsPointCloud-1.java" >}}
