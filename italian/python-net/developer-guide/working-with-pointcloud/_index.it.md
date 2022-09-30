---
title: Lavorare con PointCloud
type: docs
weight: 150
url: /it/python-net/working-with-pointcloud/
description: Aspose.3D per Python via .NET consente di decodificare una mesh da un file Draco direttamente senza costruire una scena utilizzando il metodo Decode della classe DracoFormat.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.7 o maggiore.

{{% /alert %}} 
# **Decodificare la maglia**
Aspose.3D per Python via .NET consente di decodificare una mesh da un file Draco direttamente senza costruire una scena utilizzando il metodo [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) della classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-DecodeMesh-1.py" >}}
# **Code Mesh**
Aspose.3D per Python via .NET consente di codificare una mesh a sfera su un file Draco direttamente senza costruire una scena utilizzando il metodo [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) della classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMesh-1.py" >}}
# **Codificare sfera come PointCloud**
Aspose.3D per Python via .NET consente di codificare una maglia a sfera in file Draco come nuvola di punti utilizzando il metodo [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) della classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeSphereAsPointCloud-1.py" >}}
# **Codificare la maglia allo PLY**
Aspose.3D per Python via .NET permette la codifica di un file mesh a PLY direttamente senza costruire una scena utilizzando il[Codifica](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1)Metodo di[Formato ply](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)Classe. Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
# **Decodificare la maglia dallo PLY**
Aspose.3D per Python via .NET consente di decodificare una nuvola mesh/point da un file PLY utilizzando il metodo [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) della classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
# **Esportare in PLY come PointCloud**
Aspose.3D per Python via .NET consente di esportare una scena in PLY come PointCloud utilizzando il metodo [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) della classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-ExportToPlyAsPointCloud-1.py" >}}
# **Esporta la scena 3D come Point Cloud**
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.8 o maggiore.

{{% /alert %}} 

Aspose.3D per Python via .NET consente di esportare una scena 3D come PointCloud utilizzando la proprietà [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) della classe [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Il seguente frammento di codice mostra come utilizzare questa funzionalità:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-Export3DSceneAsPointCloud-1.py" >}}
