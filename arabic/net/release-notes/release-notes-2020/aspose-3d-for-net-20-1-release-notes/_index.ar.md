---
title: Aspose.3D for .NET 20.1 tes elease ootes
type: docs
weight: 70
url: /ar/net/aspose-3d-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 20.1.

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-602|Add FBX 6100 Iدعم mport|New eature|
|THREEDNET-594 |Line وتقديم منحنى|Enhancement|
|THREEDNET-601 |Improof خوارزمية الجيل العادي|Enhancement|
|THREEDNET-603 |لا يمكن تقديم ome ome ome ome S S في Aspose.3D|Bug|
|THREEDNET-595 |Sأنذر خلق عند دمج مشهد|Bug|
|THREEDNET-605|مشهد erge Mفي شبكة قد تفشل.|Bug|
|THREEDNET-608 |Aving يلوحون Lالمشهد هو في بعض الأحيان فقدان الأشياء|Bug|
## **Hangublic API و ackackward hangمتوافق مع hangمعلقة**
### **New Classes**
Added فئة جديدة Aspose.ThreeD.**PushConstant**

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

**Uسيج**

Tله يبسط إعداد دفع ثابت في تقديم كما هو موضح أدناه.

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


### **New emالجمر**
- أعضاء Added إلى الفئة Aspose.ThreeD. nntities. Line

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

- أعضاء Added إلى الفئة Aspose.ThreeD. nntities. ururbsCurve
- أعضاء Added إلى الفئة Aspose.ThreeD.FileFormat
- أعضاء Added إلى الفئة Aspose.ThreeD.
- أعضاء Added إلى الفئة Aspose.ThreeD.
- أعضاء Added إلى الفئة Aspose.ThreeD.
### **Rالرموز التعبيرية emالجمر**
- ` ` أعضاء عاطفي من الفئة Aspose.ThreeD. nntities. Line
