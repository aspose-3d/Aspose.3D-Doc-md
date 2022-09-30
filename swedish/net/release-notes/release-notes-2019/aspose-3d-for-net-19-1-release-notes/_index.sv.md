---
title: Aspose.3D for .NET 19,1 Utgivning
type: docs
weight: 120
url: /sv/net/aspose-3d-for-net-19-1-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 19,1](https://www.nuget.org/packages/Aspose.3D/19.1.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-346|UV-atlasalgoritm|Ny funktion|
|THREEDNET-467|AMF Exportör|Ny funktion|
|THREEDNET-469|Arkivbaserat filformat|Ny funktion|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
#### **Lagt till klass Aspose.ThreeD.Formats.AMFSaveOptions.**


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
#### **Ny medlem lagt till i klassen Aspose.ThreeD Enheter.PolygonModifier:**
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




