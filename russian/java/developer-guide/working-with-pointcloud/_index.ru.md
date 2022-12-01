---
title: Работа с PointCloud
type: docs
weight: 110
url: /ru/java/working-with-pointcloud/
description: Aspose.3D for Java позволяет напрямую декодировать сетку из файла Draco без построения сцены с использованием метода декодирования класса DracoFormat.
---
# **Декодирование сетки**
Aspose.3D for Java позволяет напрямую декодировать сетку из файла Draco без построения сцены с использованием метода [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) класса [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-DecodeMesh-1.java" >}}
# **Кодировать сетку**
Aspose.3D for Java позволяет напрямую кодировать сферную сетку в файл Draco без создания сцены с использованием метода [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) класса [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMesh-1.java" >}}
# **Кодировать сферу как PointCloud**
Aspose.3D for Java позволяет кодировать сферную сетку в файл Draco как облако точек с использованием метода [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) класса [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeSphereAsPointCloud-1.java" >}}
# **Кодировать сетку к PLY**
Aspose.3D for Java позволяет напрямую кодировать сетку в файл PLY без создания сцены с использованием метода [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) класса [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
# **Декодировать Mesh от PLY**
Aspose.3D for Java позволяет декодировать облако сетки/точек из файла PLY с использованием метода [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-) класса [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
# **Экспорт в PLY как PointCloud**
Aspose.3D for Java позволяет экспортировать сцену в PLY как PointCloud с использованием метода [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-) класса [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-ExportToPlyAsPointCloud-1.java" >}}
# **Экспорт 3D Сцена в виде облака точек**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 

Aspose.3D for Java позволяет экспортировать сцену 3D как PointCloud с использованием метода [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) класса [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions). Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-Export3DSceneAsPointCloud-1.java" >}}
