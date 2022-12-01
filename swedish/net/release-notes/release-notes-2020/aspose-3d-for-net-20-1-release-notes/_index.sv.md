---
title: Aspose.3D for .NET 20,1 Utgivning
type: docs
weight: 70
url: /sv/net/aspose-3d-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgivningsnoteringar information om Aspose.3D for .NET 20.1.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-602|Lägg till FBX 6100 Importstöd|Ny funktion|
|THREEDNET-594 |Linje- och kurvorgivning|Förbättring|
|THREEDNET-601 |Förbättra normal genereringsalgoritm|Förbättring|
|THREEDNET-603 |Vissa NURBS kan inte göras i Aspose.3D|FelComment|
|THREEDNET-595 |Skugga skapad när en scen slås ihop|FelComment|
|THREEDNET-605|Sammanfoga scen i mesh kan misslyckas.|FelComment|
|THREEDNET-608 |Att spara och ladda scen är ibland att förlora föremål|FelComment|
## **Offentlig API och bakåtkompatibla förändringar**
### **Nya klasser**
Lagt till ny klass Aspose.ThreeD.Render.**Push Konstanta**

{{< highlight "java" >}}

 /// <summary>

    /// A utility to provide data to shader through push constant.

    /// </summary>

    public class PushConstant

    {

        /// <summary>

        /// Constructor of the <see cref="PushConstant"/>

        /// </summary>

        public PushConstant();

        /// <summary>

        /// Write the matrix to the constant

        /// </summary>

        /// <param name="mat">The matrix to write</param>

        public PushConstant Write(FMatrix4 mat);

        /// <summary>

        /// Write a int value to the constant

        /// </summary>

        /// <param name="n"></param>

        public PushConstant Write(int n);


        /// <summary>

        /// Write a float value to the constant

        /// </summary>

        /// <param name="f"></param>

        public PushConstant Write(float f);

        /// <summary>

        /// Write a 4-component vector to the constant

        /// </summary>

        /// <param name="vec"></param>

        public PushConstant Write(FVector4 vec);

        /// <summary>

        /// Write a 3-component vector to the constant

        /// </summary>

        /// <param name="vec"></param>

        public PushConstant Write(FVector3 vec);

        /// <summary>

        /// Write a 4-component vector to the constant

        /// </summary>

        /// <param name="x"></param>

        /// <param name="y"></param>

        /// <param name="z"></param>

        /// <param name="w"></param>

        public PushConstant Write(float x, float y, float z, float w);


        /// <summary>

        /// Commit prepared data to graphics pipeline.

        /// </summary>

        /// <param name="stage"></param>

        /// <param name="commandList"></param>

        public PushConstant Commit(ShaderStage stage, ICommandList commandList);

    }

{{< /highlight >}}

**Användning**

Detta förenklar förberedelsen av push konstant i rendering som visas nedan.

{{< highlight "java" >}}

 //The old code in Background.cs in AssetBrowser to prepare data for background shader:

  /*

            float[]data =

            {

                1000, 0, 0, 0,//height

                0.22f, 0.2f, 0.13f, 1.0f,//upper color

                0.2f, 0.3f, 0.3f, 1.0f//lower color

            };

            var constants = new byte[data.Length * 4];

            Buffer.BlockCopy(data, 0, constants, 0, constants.Length);

            commandList.PushConstants(ShaderStage.FragmentShader, constants)

  */

//The new code by using PushConstant, you don't need to calculate the data's alignment manually:





//Push the height/upper color/lower color to the fragment shader

pushConstant

     .Write(1000.0f)

     .Write(0.22f, 0.2f, 0.13f, 1.0f)

     .Write(0.2f, 0.3f, 0.3f, 1.0f)

     .Commit(ShaderStage.FragmentShader, commandList);

{{< /highlight >}}


### **Nya ledamöter**
- Lagt till medlemmar i klass Aspose.ThreeD Enheter.Linje

{{< highlight "java" >}}

 /// <summary>

        /// Gets the segments of the line

        /// </summary>

        public System.Collections.Generic.IList<int[]> Segments{ get;}



        /// <summary>

        /// Gets or sets the color of the line, default value is white(1, 1, 1)

        /// </summary>

        public Aspose.ThreeD.Utilities.Vector3 Color{ get;set;}

{{< /highlight >}}

- Lagt till medlemmar i klass Aspose.ThreeD Enheter.NurbsCurve
- Lagt till medlemmar i klass Aspose.ThreeD.FileFormatt
- Lagt till medlemmar i klass Aspose.ThreeD.Render.ICommandList.
- Lagt till medlemmar i klass Aspose.ThreeD.Render.RendererVariableManager
- Lagt till medlemmar i klass Aspose.ThreeD.Utilities.FMatrix4
### **Avlägsnade medlemmar**
- ` ` Avlägsnade medlemmar från klass Aspose.ThreeD Enheter.Linje
