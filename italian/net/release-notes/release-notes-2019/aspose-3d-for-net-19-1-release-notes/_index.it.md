---
title: Aspose.3D for .NET 19.1 Note di rilascio
type: docs
weight: 120
url: /it/net/aspose-3d-for-net-19-1-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 19.1](https://www.nuget.org/packages/Aspose.3D/19.1.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-346|Algoritmo di atlante UV|Nuova funzione|
|THREEDNET-467|AMF Esportatore|Nuova funzione|
|THREEDNET-469|Rilevamento del formato file basato su archivio|Nuova funzione|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
#### **Classe aggiunta Aspose.ThreeD. Formati. AMFSaveOptions**


{{< highlight "java" >}}

     /// <summary>

    /// Save options for AMF

    /// </summary>

    public class AMFSaveOptions : SaveOptions

    {

        /// <summary>

        /// Whether to use compression to reduce the final file size, default value is true

        /// </summary>

        public bool EnableCompression { get; set; }

    }

{{< /highlight >}}
#### **Nuovo membro aggiunto alla classe Aspose.ThreeD.Entities.PolygonModifier:**
{{< highlight "java" >}}

         /// <summary>

        /// Generate UV data from the given input mesh and specified normal data.

        /// </summary>

        /// <param name="mesh">The input mesh</param>

        /// <param name="normals">The normal data</param>

        /// <returns>Generated UV data</returns>

        public static VertexElementUV GenerateUV(Mesh mesh, VertexElementNormal normals);

        /// <summary>

        /// Generate UV data from the given input mesh

        /// </summary>

        /// <param name="mesh">The input mesh</param>

        /// <returns>Generated UV data</returns>

        public static VertexElementUV GenerateUV(Mesh mesh);

{{< /highlight >}}




